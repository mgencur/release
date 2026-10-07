# Plan: auxiliary vSphere lease sized for hosted workers

## Goal

Refactor the VCM setup and cleanup steps so a future MCE/Agent job can keep its management-cluster profile and acquire vSphere capacity independently for hosted-cluster worker VMs. Add a worker-only capacity mode that requests only the CPU, memory, and network needed by those workers. Preserve current standalone vSphere installation behavior.

This change does **not** wire the mode into an HCP workflow or job. Workflow adoption is a later, optional follow-up.

## Current behavior

- A multi-stage job's `cluster_profile` automatically contributes a Boskos lease exposed as `LEASED_RESOURCE`. The management workflow uses it for its management infrastructure.
- CI can acquire additional leases declared in the job's `steps.leases`; each lease is exposed in the requested environment variable and released by CI when the job finishes.
- `ipi-conf-vsphere-check-vcm` currently returns early unless `CLUSTER_PROFILE_NAME=vsphere-elastic`. It then uses `LEASED_RESOURCE` as the VCM lease group/ID.
- That step calculates standalone-cluster capacity from the vault `vm-specs.json`: control-plane replicas, compute replicas, and one additional control-plane-sized bootstrap VM. It creates VCM Lease resources for the resulting CPU, memory, network, and pool requirements.
- `ipi-deprovision-vsphere-lease` also gates on `CLUSTER_PROFILE_NAME=vsphere-elastic` and deletes VCM Lease resources using the `LEASED_RESOURCE` group label.
- The existing vSphere Agent provision step currently creates VMs with a fixed 32 GiB memory setting and a CPU setting chosen by its standalone-cluster logic. VCM's requested worker size must be checked against the actual worker VM size before reusing that provision logic.

Relevant implementation:

- [VCM setup step](ci-operator/step-registry/ipi/conf/vsphere/check/vcm/ipi-conf-vsphere-check-vcm-commands.sh)
- [VCM setup step definition and credential mounts](ci-operator/step-registry/ipi/conf/vsphere/check/vcm/ipi-conf-vsphere-check-vcm-ref.yaml)
- [VCM lease cleanup step](ci-operator/step-registry/ipi/deprovision/vsphere/lease/ipi-deprovision-vsphere-lease-commands.sh)
- [Existing vSphere Agent VM provisioner](ci-operator/step-registry/cucushift/agent/vsphere/provision/cucushift-agent-vsphere-provision-commands.sh)
- [CI lease aggregation behavior](https://github.com/openshift/ci-tools/blob/master/pkg/api/leases.go)

## Proposed lease identities

Keep the primary profile lease for management. When a future workflow is wired, it can request a second CI/Boskos quota lease for vSphere and expose it as `VSPHERE_LEASED_RESOURCE`:

```yaml
# Illustrative future job configuration; do not add this in this refactor.
steps:
  cluster_profile: equinix-ocp-hcp
  leases:
  - env: VSPHERE_LEASED_RESOURCE
    resource_type: vsphere-elastic-quota-slice
```

The exact management profile depends on the agreed management-cluster topology. `VSPHERE_LEASED_RESOURCE` is a proposed name; use a different distinct name if needed, but do not repurpose `LEASED_RESOURCE`. For this refactor, the VCM step and cleanup should support this input when provided; adding the job-level lease declaration is deferred.

Keep the identities distinct throughout the job:

| Resource | Identifier | Owner/lifecycle |
| --- | --- | --- |
| Management CI resource | `LEASED_RESOURCE` | Existing management workflow and CI lease handling |
| vSphere CI quota slot | `VSPHERE_LEASED_RESOURCE` | CI lease handling; held through job completion |
| VCM allocation for hosted workers | VCM Lease(s) labeled with the vSphere ID/group | New VCM setup and explicit VCM cleanup |

The CI quota slot reserves a CI concurrency/resource unit; it is not itself the vSphere network or capacity allocation. The VCM Lease requests and returns the concrete network, vCenter, and connection details.

## Implementation steps

### 1. Add an explicit auxiliary-allocation mode

Add an opt-in VCM input such as `VCM_ALLOCATION_MODE=guest-workers` and a positive `VSPHERE_GUEST_WORKER_COUNT` input. The VCM setup script should select its lease identity as follows:

1. If `VSPHERE_LEASED_RESOURCE` is set, use it as the VCM group/ID and allow execution even when the primary profile is not `vsphere-elastic`.
2. Otherwise, if the primary profile is `vsphere-elastic`, use `LEASED_RESOURCE` exactly as today.
3. Otherwise, preserve the current early-exit behavior.

Fail clearly if auxiliary mode is requested without its separate lease ID, credentials, or required inputs. Preserve the existing `VSPHERE_BASTION_LEASED_RESOURCE` behavior and do not change the primary management `LEASED_RESOURCE`.

Parameterize the setup step rather than cloning the entire VCM implementation, if practical. Keep all existing vSphere profile paths and generated outputs unchanged.

### 2. Calculate worker-only capacity

Add a distinct capacity branch for `guest-workers`. Do not implement it by merely setting `CONTROL_PLANE_REPLICAS=0` in the current formula: that formula still adds one control-plane-sized bootstrap VM.

For a fixed-size Agent NodePool, request:

```text
vCPUs = guest worker count × vCPUs per worker VM
memory = guest worker count × memory per worker VM
```

Use the worker VM sizing that the provisioner will actually apply. Prefer deriving the VCM request and VM configuration from the same source. If the existing provisioner remains fixed at 4 vCPUs and 32 GiB per worker, request exactly those values per worker; if VM sizing is parameterized, use those same parameters in both places.

For a Vault `vm-specs.json` based implementation, use `.spec.compute.cpus` and `.spec.compute.memoryMB` only after confirming they match the Agent worker VM size. Convert requested memory from MB to VCM's GB units with rounding up so fractional GiB cannot under-request. Validate the worker count and sizing values before creating a lease.

Do not include control-plane replicas, bootstrap capacity, or standalone-cluster fallback values (24 cores/96 GiB) in this mode. Preserve the existing standalone formula and its override behavior for all current users. When a later HCP workflow uses this mode, request one worker network and one vSphere pool unless its design explicitly requires more.

### 3. Create and reconcile the VCM allocation

- Create the VCM Lease with `vcpus` and `memory` from the worker-only calculation, the required network count/type, and the selected pool constraints.
- Label the lease with the vSphere Boskos ID/group, job identity, and a distinct hosted-worker purpose. Do not label it with the management lease ID.
- Wait for the VCM lease to reach `Fulfilled`; fail with the VCM object and status details if it fails or times out.
- Reuse the existing reconciliation that reads the fulfilled lease and writes `govc.sh`, `vsphere_context.sh`, network/subnet data, and lease metadata to `${SHARED_DIR}`.
- Ensure repeated executions and partial failures can identify which VCM leases belong to this job. Persist lease names/IDs early enough for cleanup.

### 4. Add matching VCM cleanup

Update or add a cleanup mode that uses `VSPHERE_LEASED_RESOURCE` when present, with the existing `vsphere-elastic`/`LEASED_RESOURCE` fallback for current jobs.

When the HCP workflow is wired in a later change, its cleanup order should be:

1. Gather diagnostics while the management cluster and VCM allocation still exist.
2. Destroy the hosted cluster and remove the run-owned worker VMs, folder, and uploaded ISO.
3. Delete the VCM Lease group associated with `VSPHERE_LEASED_RESOURCE`.
4. Let CI release the auxiliary Boskos quota slot at job completion.
5. Continue existing management teardown and CI lease handling.

Cleanup must be safe when VCM setup failed partway through or no VCM Lease was created. Do not delete by the management `LEASED_RESOURCE`.

### 5. Optional/informational follow-up: wire the HCP workflow

This section is informational and is **out of scope** for implementing this plan. Do not edit the HCP workflow, job configuration, or job lease declarations as part of this change.

- Declare the auxiliary `vsphere-elastic-quota-slice` lease in the job configuration.
- Mount the VCM/vCenter credentials needed by the vSphere setup and worker-provisioning steps through their step refs. The management cluster profile remains responsible for management credentials.
- Set worker-only allocation mode and the same worker count used for the Agent NodePool and VM provisioner.
- Run VCM setup before VM provisioning; pass the generated vSphere context and network data to the worker step.
- Run VCM cleanup after guest VMs and the HostedCluster are removed, before tearing down the management cluster.
- Do not run the legacy VCM sibling that parses the primary `LEASED_RESOURCE` as a vSphere router/datacenter/VLAN value.

## Compatibility requirements

- Existing jobs using `cluster_profile: vsphere-elastic` continue to use `LEASED_RESOURCE` and the current standalone formula, including bootstrap capacity.
- Existing VCM Lease naming/labels and the bastion lease path continue to work for those jobs.
- Non-vSphere-profile jobs continue to skip VCM setup unless they explicitly set the auxiliary mode and provide `VSPHERE_LEASED_RESOURCE`.
- Future HCP workflow wiring keeps management kubeconfig/profile data separate from vSphere data.

## Acceptance criteria for the VCM refactor

- [ ] The VCM setup code accepts an explicit auxiliary lease ID when the primary profile is not `vsphere-elastic`, without requiring a workflow/job change in this implementation.
- [ ] The worker-only capacity calculation can be exercised with an explicit worker count and sizing values. It requests worker CPU, memory, and network only, without control-plane or bootstrap capacity.
- [ ] The worker capacity values can be aligned with the VM provisioner's effective CPU and memory settings.
- [ ] The VCM setup code still generates the context and network data needed by a later provisioning step.
- [ ] VCM cleanup can target the auxiliary lease ID independently of the management `LEASED_RESOURCE`, including after partial setup failures.
- [ ] Existing standalone `vsphere-elastic` jobs retain their previous capacity calculation, lease identity, and cleanup behavior.
- [ ] Non-vSphere workflows continue to skip VCM setup unless the auxiliary allocation mode is explicitly requested.

No acceptance criterion requires adding or changing an HCP workflow or job. The optional workflow adoption can be planned and reviewed separately.

## Validation

- Confirm the VCM setup and cleanup scripts use the explicit auxiliary lease ID when provided, without depending on a job-level lease declaration.
- Exercise capacity calculation with multiple worker counts and assert CPU and memory scale linearly, with no control-plane/bootstrap contribution.
- Compare the requested worker sizing against the VM provisioner's effective CPU and memory settings.
- Rehearse normal allocation, VCM failure, timeout, partial setup, and cleanup; verify VCM Lease resources are released. Boskos quota lease acquisition/release belongs to the deferred workflow-wiring follow-up.
- Confirm a representative existing `vsphere-elastic` job still requests its prior standalone capacity, including bootstrap.
