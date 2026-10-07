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

Before creating DNS records or ACLs, capture the values from the actual test environment rather than copying libvirt defaults:

- HostedCluster name and exact `spec.dns.baseDomain`.
- Management cluster worker/node addresses that can receive the hosted services' NodePort traffic, or a stable VIP/load balancer in front of them.
- The live NodePort for each service in `HostedCluster.spec.services` and the corresponding management-cluster Service. Include API server, Ignition, Konnectivity, OAuth, and OIDC when published. The current helper's collected port files do not establish that every published service, particularly OIDC, is represented.
- The Assisted Service URL and every image, rootfs, or agent-service URL embedded in or fetched by the generated discovery ISO. Inspect the generated InfraEnv status and discovery-agent configuration; the URL used by the CI pod to download the ISO is not necessarily a runtime URL used by the VM.
- Guest ingress address for `*.apps.<cluster>.<base-domain>`, if conformance tests require guest routes.
- vSphere worker VLAN/portgroup, address allocation (DHCP or static), gateway, MTU, resolver addresses, and any routing/firewall boundaries.
- For each destination, choose whether the worker connects directly or through Squid. For a proxied HTTPS destination, the worker resolves the proxy name and Squid resolves the destination hostname. For a direct destination, the worker's configured resolver must resolve it and the worker network must route to its resolved address.

Record this as a source/destination/port matrix and keep direct and proxy paths explicit. Do not assume that a CI pod's successful connection proves either path from a vSphere VM.

### 2. Configure DNS resolution on the worker network

Use this preference order:

1. **DHCP-provided DNS**, only if the DHCP server supplies resolver IPs reachable from the vSphere worker VLAN and those resolvers can resolve all direct-path names required by the worker.
2. **Per-worker static network configuration**, if DHCP cannot provide the required resolver or worker addressing. Create an `NMStateConfig` for each worker MAC (or a well-defined matching set), put the resolver IPs under its DNS resolver configuration, and select the resources from the InfraEnv using its NMStateConfig label selector. Include address, gateway, routes, and MTU in the same configuration where required. RHACM documents InfraEnv proxy and NMState-based host networking in its [cluster management documentation](https://docs.redhat.com/en/documentation/red_hat_advanced_cluster_management_for_kubernetes/2.14/html-single/clusters/clusters).

Do not point vSphere workers at the libvirt host's `127.0.0.1` resolver or assume they inherit the `ostestbm` forwarding rule. Configure only resolver addresses reachable from the VM. Permit both UDP and TCP DNS (port 53) from the worker VLAN to those resolvers; TCP is needed for some responses and fallback behavior.

Validate the effective resolver inside a booted discovery VM and again on an installed worker (`/etc/resolv.conf`, resolver reachability, and actual lookups). DNS configuration on the InfraEnv/discovery image and proxy configuration on the HostedCluster are separate inputs.

### 3. Define the required DNS names and Route 53 records

First establish which DNS zone is authoritative for the HostedCluster's exact base domain. `DNS.spec.baseDomain` identifies the current management cluster's base domain, but does not prove that a Route 53 hosted zone exists for it or that the job owns that zone. If it is not a Route 53 zone controlled for this job, use the actual authoritative DNS service or delegate a run-specific subdomain; do not write records into a guessed or unrelated zone.

For the existing NodePort design, the intended query/record set is:

| Query name (per run) | Record and answer | Status / purpose |
| --- | --- | --- |
| `api.<cluster>.<base-domain>` | `A` to the worker-reachable management node IP(s) or stable VIP; add `AAAA` only if IPv6 is actually routed end-to-end | Required HostedCluster API address supplied to HyperShift. The same hostname is used for NodePort-published services, each on its own port. See AWS's [A and AAAA record types](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/ResourceRecordTypes.html). |
| `api-int.<cluster>.<base-domain>` | Same address(es) as `api...` (or a `CNAME` to it, if permitted by the selected DNS design) | The existing Agent DNS helper creates this for parity. Include initially, then verify whether clients in this topology query it; its necessity for Linux Agent workers is not established. |
| `*.apps.<cluster>.<base-domain>` | `A` to the reserved guest ingress VIP; `AAAA` only for a real, reachable IPv6 ingress address | Conditional: needed if conformance tests or other clients require guest application routes. The current dev-scripts MetalLB values (`192.168.111.30` and its IPv6 counterpart) are libvirt defaults and must not be reused for vSphere. |

For guest ingress, use the HostedCluster ingress operator's `HostNetwork` publishing strategy and add a separately managed MetalLB `LoadBalancer` Service, following the pattern in [the CI MetalLB step](ci-operator/step-registry/hypershift/agent/create/metallb/hypershift-agent-create-metallb-commands.sh). `HostNetwork` makes the router pods listen on worker-node ports 80/443; it does not allocate a stable external VIP or create this Service. Configure an `IPAddressPool` for the vSphere-reserved VIP, an `L2Advertisement` for that pool, and a Service in `openshift-ingress` of type `LoadBalancer` selecting the default router pods on ports 80/443. Associate the Service with the intended pool using the annotation/API supported by the deployed MetalLB version, and verify its endpoints match the router pods. The wildcard `*.apps` record above must resolve to this VIP. MetalLB's L2 mode requires the VIP to be reachable on the worker network's Layer 2 segment; if that is not true, use a supported routed/BGP or external-load-balancer design instead. The pool, Service, and DNS record are separate from the HyperShift API/NodePort publishing configuration and need explicit lifecycle and cleanup handling.

These are the HostedCluster API and ingress names to verify from the worker network. Also verify resolution of the actual Assisted Service, image/rootfs, registry, and proxy hostnames discovered in step 1. Add or delegate records for those service names **only if** they are not already resolvable from the worker's selected DNS path. Do not invent MCE service FQDNs or create duplicate records for existing management-cluster routes.

Do not create separate DNS names for API, OAuth, OIDC, Ignition, and Konnectivity merely to represent their different NodePorts: DNS has no port field, and the current NodePort mapping uses the same API hostname. If the final HostedCluster uses distinct publishing addresses, add records for those exact addresses instead. Per-node `A`/`PTR` records are not included by default; add them only if the selected static-addressing, installer, or test requirements demonstrate they are needed.

For records owned by the test, use run-scoped names, short TTLs (for example 60–300 seconds), narrowly scoped Route 53 change permissions, and an idempotent create/update plus post-job cleanup. Never delete records outside the current run's recorded ownership set.

**Route 53 visibility matters:** a private hosted zone answers only for associated VPCs or through an appropriate hybrid DNS design. If the vSphere network is outside that VPC, provide reachable Route 53 Resolver inbound endpoints over the existing network connection (or an equivalent forwarding resolver) and configure the workers to query that resolver. AWS documents [private hosted-zone behavior](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/hosted-zones-private.html) and [inbound Resolver endpoints](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver-forwarding-inbound-queries.html). A public record can be resolved by public DNS, but its answer still must be routable from the worker or proxy network.

### 4. Configure Squid for discovery and guest-node traffic

Configure the discovery environment's `InfraEnv.spec.proxy` with the proxy URL, for example `http://<squid-host>:8213/`, in the HTTP and HTTPS proxy fields as appropriate. Include a `noProxy` list derived from the actual topology. For endpoints intended to use Squid, do not put their hostnames or addresses in `noProxy`. Include cluster-local names/CIDRs and other destinations only when they should bypass the proxy and are directly reachable. The InfraEnv supports proxy configuration; see the [RHACM InfraEnv documentation](https://docs.redhat.com/en/documentation/red_hat_advanced_cluster_management_for_kubernetes/2.14/html-single/clusters/clusters).

Separately configure the HostedCluster's `spec.configuration.proxy` before or during creation so the generated worker configuration uses the intended proxy after installation. Confirm the resulting worker proxy configuration and rollout behavior; HyperShift propagates this configuration into NodePool machine configuration. Keep the proxy and trust settings aligned between discovery and the installed guest.

Update the Squid allowlist for the actual observed destinations:

- Assisted Service and every image/rootfs/agent URL the discovery agent contacts, normally HTTPS but verify from the generated environment.
- The API hostname and the exact NodePorts required for API, Ignition, Konnectivity, OAuth, and OIDC if those flows are proxied.
- Required image registries and any other explicit test dependencies.

The current Squid configuration has a limited TLS CONNECT port allowlist and the current Agent proxy step builds an ACL from only a subset of service ports. Review both the destination-domain ACL and allowed CONNECT ports. Do not broadly allow all domains or all ports: use the per-run hostnames and exact live ports, and remove stale dynamic entries during cleanup. Squid's [HTTPS CONNECT behavior](https://wiki.squid-cache.org/Features/HTTPS) tunnels TLS; retain normal certificate verification and do not add TLS interception as a shortcut.

If any endpoint is signed by a private CA, supply the correct CA trust bundle to the discovery environment and the HostedCluster/guest configuration. A proxy tunnel does not by itself make an untrusted endpoint certificate valid.

### 5. Open and verify the network paths

Document the direction and enforcement point for each flow. At minimum, assess:

| Source | Destination | Protocol/port | Path |
| --- | --- | --- | --- |
| Discovery/worker VM | Configured DNS resolver | UDP and TCP 53 | Direct from worker VLAN |
| Discovery/worker VM | Squid | TCP 8213 (or the configured listener) | Direct to proxy; reachability is still to be tested |
| Squid | Assisted Service and image/rootfs endpoints | Exact destination ports, normally TCP 443 | Proxy egress, with DNS resolution from Squid's resolver |
| Squid, or worker VM for direct mode | Management nodes/stable VIP hosting NodePorts | Exact live NodePorts for published HostedCluster services | Direct route from the chosen client; ensure ACL/firewall permits the selected path |
| Guest workers | Required registries and test dependencies | Usually TCP 443; verify exact endpoints | Via Squid or an approved direct route |
| Test runner / guest clients | Guest ingress VIP | TCP 80/443 as required | Route to the vSphere-side ingress address |

Use firewalls/security controls that permit the selected source and destination ranges, return traffic, and required ports. Check route symmetry, MTU, and any NAT behavior. Do not assume that permitting TCP 443 is enough if the NodePort services use dynamically allocated high ports. If routing is intentionally proxy-only, ensure the proxy host itself can reach the management NodePorts and guest service endpoints.

### 6. Validate from a real vSphere worker network

Run a disposable VM or the first discovery VM on the exact vSphere portgroup and validate before scaling the NodePool:

- Confirm DHCP/static address, gateway, MTU, resolver, and proxy settings.
- Query the required names (`api...`, `api-int...`, `*.apps...`, and the actual Assisted/image/rootfs/proxy hosts) from the relevant resolver. For proxied requests, distinguish the worker's lookup of the proxy name from Squid's lookup of the destination.
- Test TCP/53 to DNS, TCP/8213 to Squid, and the selected direct/proxy endpoint paths. For the HTTPS proxy path, use a request through the proxy and confirm the CONNECT target and port are accepted in Squid logs.
- Verify TLS certificate chains and hostname validation for Assisted Service, image/rootfs, API, ignition, and Konnectivity endpoints.
- Confirm the discovery agent registers in the intended namespace and can retrieve its configuration; then confirm an installed worker becomes Ready and can maintain API/Konnectivity connectivity.
- Verify guest ingress resolution and reachability from the test runner if the chosen tests need it.

Capture DNS answers, resolved address, route, port, proxy result, and relevant logs as artifacts without including credentials or tokens. Test both successful provisioning and cleanup of all run-owned DNS records and network resources.

## Separate follow-up check: vSphere worker to Squid reachability

This is intentionally unresolved and must be verified before treating the plan as viable:

- From a VM on the selected vSphere worker portgroup, test TCP connection to `<squid-host>:8213` (or the configured listener), then make a proxied HTTPS request to one approved endpoint.
- Confirm the return route and that intermediate firewalls permit the flow.
- Confirm Squid listens on an address reachable from that network, permits the worker source range, allows the target hostname and port, and logs the request.
- A successful request from a Prow pod, management node, or bastion is not proof of worker-network reachability.

If this check fails, stop and choose a supported direct route or a proxy located on/reachable from the vSphere network; do not proceed by assuming the CI proxy variables reach the worker.

## Other decisions to close before implementation

- [ ] Confirm whether the HostedCluster base domain is in a Route 53 public or private hosted zone, and who owns updates/cleanup.
- [ ] Confirm how the vSphere network reaches the chosen resolver; for private Route 53, verify VPC association or an inbound Resolver endpoint and its network path.
- [ ] Select and reserve stable management NodePort target IP(s)/VIP and the guest ingress VIP; prove routing from the required clients.
- [ ] Inspect the generated InfraEnv/discovery ISO for the exact Assisted and image/rootfs URLs, ports, trust chain, and proxy handling.
- [ ] Decide direct versus proxy access for each HostedCluster NodePort service; confirm all live ports are included in both network policy/firewall and Squid ACLs.
- [ ] Verify whether `api-int` and per-node forward/reverse DNS are actually required for this Agent HostedCluster design.
- [ ] Verify the worker's DNS and proxy configuration survives the transition from discovery boot to the installed RHCOS node.

## Acceptance criteria

- [ ] A vSphere discovery VM resolves all required direct-path names using its configured resolver and resolves the proxy endpoint.
- [ ] Assisted agents can reach and register with the Assisted Service and fetch all required images/rootfs.
- [ ] Hosted workers can reach API, Ignition, and Konnectivity over the documented direct or proxy path, using all actual NodePorts.
- [ ] TLS verification succeeds without disabling certificate checks.
- [ ] Guest ingress and required external registries are reachable from their intended clients.
- [ ] Route 53 records, if used, are created only in the verified authoritative zone, are run-scoped, and are removed safely after the job.
- [ ] The separate worker-to-Squid reachability check is completed and recorded; it is not inferred from CI pod connectivity.
