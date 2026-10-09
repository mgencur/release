# Plan: network connectivity for Agent workers on vSphere

## Goal and scope

Define the DNS, proxy, routing, and firewall setup needed for vSphere VMs to boot as Assisted Installer agents and join an Agent-platform HostedCluster managed by MCE. This complements [the vSphere conformance workflow plan](hypershift-mce-agent-vsphere-conformance-plan.md); it does not wire a CI workflow or change the existing libvirt-based workflow.

For planning, assume the Squid proxy host is reachable from the vSphere worker network. That is an explicit unverified assumption, not a finding. The final section tracks it as a separate check.

The design has two network phases which need independent configuration:

1. **Discovery and installation:** the booted discovery agent must reach the management-cluster Assisted Service and any image/rootfs endpoints it uses, as well as the hosted ignition endpoint.
2. **Running guest nodes:** installed workers must reach the hosted API and Konnectivity endpoints, registries and other required egress destinations. Configure this phase through the HostedCluster proxy configuration as well as the discovery environment; setting a proxy only on the CI pod or only on the discovery ISO does not cover both phases.

## Existing behavior and constraints

- The MCE HostedCluster creation step reads the management cluster's `DNS.spec.baseDomain` and passes it to `hypershift create cluster agent`, with `api.<cluster>.<base-domain>` as the API server address. See [hosted-cluster creation](ci-operator/step-registry/hypershift/mce/agent/create/hostedcluster/hypershift-mce-agent-create-hostedcluster-commands.sh).
- HyperShift's Agent NodePort publishing maps the API, OAuth, OIDC, Konnectivity, and Ignition services to the configured API address, using separate NodePorts. DNS records map names to addresses; they do not encode these port numbers. See [HyperShift's NodePort mapping](https://github.com/openshift/hypershift/blob/main/cmd/cluster/core/create.go).
- The current [DNS setup step](ci-operator/step-registry/hypershift/agent/create/config-dns/hypershift-agent-create-config-dns-commands.sh) selects the first management worker's `InternalIP` and edits host dnsmasq and the libvirt `ostestbm` network, adding `api`, `api-int`, and guest ingress entries. It does not configure DNS for vSphere VMs; that IP and the libvirt ingress VIP must not be assumed reachable from the vSphere network.
- The current [manual-worker InfraEnv step](ci-operator/step-registry/hypershift/agent/create/add-worker-manual/hypershift-agent-create-add-worker-manual-commands.sh) does not set an InfraEnv proxy or worker DNS configuration.
- The current [Squid setup step](ci-operator/step-registry/baremetalds/devscripts/proxy/baremetalds-devscripts-proxy-commands.sh) creates a proxy on port `8213` and writes proxy variables for CI step containers. The [Agent proxy step](ci-operator/step-registry/hypershift/agent/create/proxy/hypershift-agent-create-proxy-commands.sh) adds selected HostedCluster hostnames and ports to the proxy ACL for CI-side access. Neither configures the discovery agent or proves vSphere-worker-to-Squid reachability.
- The Assisted Installer agent requires network access to the Assisted Service to register and obtain installation configuration. See [Assisted Installer troubleshooting](https://docs.redhat.com/en/documentation/assisted_installer_for_openshift_container_platform/2026/html/installing_openshift_container_platform_with_the_assisted_installer/assembly_troubleshooting).

## Plan

### 1. Inventory the real endpoints and choose direct versus proxied paths

Before changing DNS configuration or proxy ACLs, capture the values from the actual test environment rather than copying libvirt defaults:

- HostedCluster name and exact `spec.dns.baseDomain`.
- Management cluster worker/node addresses that can receive the hosted services' NodePort traffic, or a stable VIP/load balancer in front of them.
- The live NodePort for each service in `HostedCluster.spec.services` and the corresponding management-cluster Service. Include API server, Ignition, Konnectivity, OAuth, and OIDC when published. The current helper's collected port files do not establish that every published service, particularly OIDC, is represented.
- The Assisted Service URL and every image, rootfs, or agent-service URL embedded in or fetched by the generated discovery ISO. Inspect the generated InfraEnv status and discovery-agent configuration; the URL used by the CI pod to download the ISO is not necessarily a runtime URL used by the VM.
- Guest ingress address for `*.apps.<cluster>.<base-domain>`, if conformance tests require guest routes.
- vSphere worker VLAN/portgroup, address allocation (DHCP or static), gateway, MTU, resolver addresses, and any routing/firewall boundaries.
- For each destination, choose whether the worker connects directly or through Squid. For a proxied HTTPS destination, the worker resolves the proxy name only if the proxy is configured by hostname; Squid resolves the destination hostname. For a direct destination, the worker's configured resolver must resolve it and the worker network must route to its resolved address.

Record this as a source/destination/port matrix and keep direct and proxy paths explicit. Do not assume that a CI pod's successful connection proves either path from a vSphere VM.

### 2. Determine and configure worker-side DNS only where needed

Worker-side DNS is needed for direct or `noProxy` destinations, a proxy configured by hostname, and components that do not honor the proxy. When requests use Squid and the proxy URL contains a literal IP, destination name resolution happens on Squid; no worker-side DNS change or DNS record creation is required for that traffic. First identify the actual lookups required by the selected paths.

If worker-side DNS is needed, use this preference order:

1. **DHCP-provided DNS**, only if the DHCP server supplies resolver IPs reachable from the vSphere worker VLAN and those resolvers can resolve all direct-path names required by the worker.
2. **Per-worker static network configuration**, if DHCP cannot provide the required resolver or worker addressing. Create an `NMStateConfig` for each worker MAC (or a well-defined matching set), put the resolver IPs under its DNS resolver configuration, and select the resources from the InfraEnv using its NMStateConfig label selector. Include address, gateway, routes, and MTU in the same configuration where required. RHACM documents InfraEnv proxy and NMState-based host networking in its [cluster management documentation](https://docs.redhat.com/en/documentation/red_hat_advanced_cluster_management_for_kubernetes/2.14/html-single/clusters/clusters).

Do not point vSphere workers at the libvirt host's `127.0.0.1` resolver or assume they inherit the `ostestbm` forwarding rule. Configure only resolver addresses reachable from the VM. Permit both UDP and TCP DNS (port 53) from the worker VLAN to those resolvers; TCP is needed for some responses and fallback behavior. Do not add or modify DNS records simply to make the resolver configuration appear complete.

When worker-side DNS is required, validate the effective resolver inside a booted discovery VM and again on an installed worker (`/etc/resolv.conf`, resolver reachability, and actual lookups). DNS configuration on the InfraEnv/discovery image and proxy configuration on the HostedCluster are separate inputs.

### 3. Configure proxy and DNS behavior for discovery and guest traffic

Use the actual endpoint inventory from phase 1 and first test how each name resolves through the selected direct or proxy path. Creating or changing DNS records is not a baseline requirement: use existing DNS whenever it already provides the needed answer, and change DNS only when a specific required lookup is proven to be missing or incorrect.

Configure the discovery environment's `InfraEnv.spec.proxy` with the reachable Squid URL, for example `http://<squid-host-or-IP>:8213/`, in the HTTP/HTTPS fields that apply. If the proxy is configured by hostname, the worker resolver must resolve that proxy hostname; if configured with a literal IP, no worker-side DNS lookup is needed for the proxy itself. Derive `noProxy` from the real topology. Destinations intended to use Squid must not be listed in `noProxy`; include direct destinations and cluster-local names/CIDRs only when they are reachable without the proxy. See the [RHACM InfraEnv documentation](https://docs.redhat.com/en/documentation/red_hat_advanced_cluster_management_for_kubernetes/2.14/html-single/clusters/clusters).

Separately configure the HostedCluster's `spec.configuration.proxy` before or during creation so installed workers retain the intended proxy settings. Verify the generated worker configuration and rollout behavior; discovery-time proxy configuration alone does not configure installed nodes. Keep proxy and trust settings aligned across discovery and guest phases.

For proxied HTTP(S) requests, the worker connects to Squid and sends the destination hostname (for HTTPS, in the CONNECT request); Squid resolves and connects to that destination. Therefore, worker-side DNS for the destination is not needed on this path, but Squid must be able to resolve and route to it. Worker-side DNS is needed for direct traffic, entries in `noProxy`, the proxy hostname when a hostname is used, and any components that do not honor the proxy. Configure reachable DHCP-provided resolvers or `NMStateConfig` only for these demonstrated needs, as described in phase 2.

Verify resolution and connectivity for the actual Assisted Service, image/rootfs/agent, registry, proxy, HostedCluster API, and ingress endpoints. Check `api-int` only if a component in this topology actually queries it. In the current NodePort design, API, OAuth, OIDC, Ignition, and Konnectivity use the API hostname with distinct ports; DNS does not encode those ports, so do not create separate names just to represent each service. Inspect the generated InfraEnv and HostedCluster configuration rather than inventing service FQDNs.

If a required lookup is missing, identify the authoritative DNS service and its owner first, then make only the narrowest necessary change. Do not assume the zone is Route 53, write to a guessed/unowned zone, create duplicate records, or add speculative `A`, `AAAA`, `PTR`, or delegation records. If an existing private Route 53 zone is the relevant source, verify the worker resolver can reach it through the supported VPC association or hybrid DNS path; do not create a resolver endpoint or DNS record unless the observed gap requires it. Any run-owned DNS change must be narrowly scoped, recorded, idempotent, and safely cleaned up after the run.

For guest ingress, use the HostedCluster ingress operator's `HostNetwork` publishing strategy and a separately managed MetalLB `LoadBalancer` Service, following [the CI MetalLB step](ci-operator/step-registry/hypershift/agent/create/metallb/hypershift-agent-create-metallb-commands.sh). `HostNetwork` makes router pods listen on worker-node ports 80/443; it does not allocate a stable external VIP or create this Service. Configure an `IPAddressPool` for the reserved vSphere VIP, an `L2Advertisement`, and a Service in `openshift-ingress` selecting the default router pods. Verify the pool, Service endpoints, and Layer 2 reachability (or use a supported routed/BGP or external load-balancer design). If conformance requires guest routes, verify the existing `*.apps.<cluster>.<base-domain>` resolution points to that VIP; add or update DNS only if the required lookup is actually absent or wrong. Do not reuse the dev-scripts libvirt VIPs (`192.168.111.30` or its IPv6 counterpart). Track lifecycle and cleanup for run-owned MetalLB resources and any DNS changes separately from HyperShift API/NodePort publishing.

Update Squid's destination-domain ACL and TLS CONNECT port allowlist for only the observed destinations and live ports: Assisted Service and discovery image/rootfs endpoints, proxied NodePort services, registries, and other explicit test dependencies. The existing Squid setup has a limited CONNECT port allowlist, and the Agent proxy step may build an ACL from only a subset of service ports; verify both. Do not allow all domains or ports, and remove dynamically added entries during cleanup. Squid's [HTTPS CONNECT behavior](https://wiki.squid-cache.org/Features/HTTPS) tunnels TLS; retain normal certificate verification and do not use TLS interception as a shortcut.

If an endpoint uses a private CA, provide its trust bundle to both the discovery environment and HostedCluster/guest configuration. A proxy tunnel does not make an untrusted certificate valid.

### 4. Open and verify the network paths

Document the direction and enforcement point for each flow. At minimum, assess:

| Source | Destination | Protocol/port | Path |
| --- | --- | --- | --- |
| Discovery/worker VM | Configured DNS resolver (when needed) | UDP and TCP 53 | Direct from worker VLAN |
| Discovery/worker VM | Squid | TCP 8213 (or the configured listener) | Direct to proxy; reachability is still to be tested |
| Squid | Assisted Service and image/rootfs endpoints | Exact destination ports, normally TCP 443 | Proxy egress, with DNS resolution from Squid's resolver |
| Squid, or worker VM for direct mode | Management nodes/stable VIP hosting NodePorts | Exact live NodePorts for published HostedCluster services | Direct route from the chosen client; ensure ACL/firewall permits the selected path |
| Guest workers | Required registries and test dependencies | Usually TCP 443; verify exact endpoints | Via Squid or an approved direct route |
| Test runner / guest clients | Guest ingress VIP | TCP 80/443 as required | Route to the vSphere-side ingress address |

Use firewalls/security controls that permit the selected source and destination ranges, return traffic, and required ports. Check route symmetry, MTU, and any NAT behavior. Do not assume that permitting TCP 443 is enough if the NodePort services use dynamically allocated high ports. If routing is intentionally proxy-only, ensure the proxy host itself can reach the management NodePorts and guest service endpoints.

### 5. Validate from a real vSphere worker network

Run a disposable VM or the first discovery VM on the exact vSphere portgroup and validate before scaling the NodePool:

- Confirm DHCP/static address, gateway, MTU, resolver, and proxy settings.
- Query the actual required names from the path that will resolve them. For proxied requests, distinguish the worker's lookup of the proxy name (only if it is a hostname) from Squid's lookup of the destination; check `api-int` and guest ingress names only if required by the topology/tests.
- Test TCP/53 to DNS, TCP/8213 to Squid, and the selected direct/proxy endpoint paths. For the HTTPS proxy path, use a request through the proxy and confirm the CONNECT target and port are accepted in Squid logs.
- Verify TLS certificate chains and hostname validation for Assisted Service, image/rootfs, API, ignition, and Konnectivity endpoints.
- Confirm the discovery agent registers in the intended namespace and can retrieve its configuration; then confirm an installed worker becomes Ready and can maintain API/Konnectivity connectivity.
- Verify guest ingress resolution and reachability from the test runner if the chosen tests need it.

Capture DNS answers, resolved address, route, port, proxy result, and relevant logs as artifacts without including credentials or tokens. Test successful provisioning and cleanup of run-owned resources, including DNS changes only if the job had to make any.

## Separate follow-up check: vSphere worker to Squid reachability

This is intentionally unresolved and must be verified before treating the plan as viable:

- From a VM on the selected vSphere worker portgroup, test TCP connection to `<squid-host>:8213` (or the configured listener), then make a proxied HTTPS request to one approved endpoint.
- Confirm the return route and that intermediate firewalls permit the flow.
- Confirm Squid listens on an address reachable from that network, permits the worker source range, allows the target hostname and port, and logs the request.
- A successful request from a Prow pod, management node, or bastion is not proof of worker-network reachability.

If this check fails, stop and choose a supported direct route or a proxy located on/reachable from the vSphere network; do not proceed by assuming the CI proxy variables reach the worker.

## Other decisions to close before implementation

- [ ] Identify the resolver and authoritative DNS owner only for names that fail lookup or require a change; for private Route 53 used by the selected path, verify its association or hybrid resolver path.
- [ ] Select and reserve stable management NodePort target IP(s)/VIP and the guest ingress VIP; prove routing from the required clients.
- [ ] Inspect the generated InfraEnv/discovery ISO for the exact Assisted and image/rootfs URLs, ports, trust chain, and proxy handling.
- [ ] Decide direct versus proxy access for each HostedCluster NodePort service; confirm all live ports are included in both network policy/firewall and Squid ACLs.
- [ ] Verify whether `api-int` and per-node forward/reverse DNS are actually required for this Agent HostedCluster design; do not add records unless a concrete requirement or missing lookup is established.
- [ ] Verify the worker's DNS and proxy configuration survives the transition from discovery boot to the installed RHCOS node.

## Acceptance criteria

- [ ] A vSphere discovery VM resolves required direct-path names using its configured resolver and can reach the proxy endpoint (resolving its name only if configured by hostname).
- [ ] Assisted agents can reach and register with the Assisted Service and fetch all required images/rootfs.
- [ ] Hosted workers can reach API, Ignition, and Konnectivity over the documented direct or proxy path, using all actual NodePorts.
- [ ] TLS verification succeeds without disabling certificate checks.
- [ ] Guest ingress and required external registries are reachable from their intended clients.
- [ ] Existing DNS answers are reused; any DNS changes are limited to demonstrated gaps, made only in the verified authoritative service, and cleaned up safely if owned by the run.
- [ ] The separate worker-to-Squid reachability check is completed and recorded; it is not inferred from CI pod connectivity.
