# HyperShift Jobs in openshift-tests-private

**Total: 1228 jobs** across 11 versions

## Summary

| Version | Total | AWS | Agent (BareMetal) | Azure | KubeVirt | KubeVirt (BareMetal) | Other |
|---|---|---|---|---|---|---|---|
| 4.14 | 69 | 46 | 10 | — | 3 | 10 | — |
| 4.15 | 120 | 84 | 22 | — | — | 14 | — |
| 4.16 | 123 | 57 | 18 | — | 12 | 12 | 24 |
| 4.17 | 102 | 65 | 15 | — | 3 | 3 | 16 |
| 4.18 | 148 | 91 | 19 | — | 8 | 8 | 22 |
| 4.19 | 172 | 98 | 13 | 27 | 9 | 11 | 14 |
| 4.20 | 175 | 100 | 15 | 27 | 9 | 8 | 16 |
| 4.21 | 173 | 97 | 10 | 34 | 9 | 8 | 15 |
| 4.22 | 95 | 59 | 1 | 30 | 2 | 2 | 1 |
| 4.23 | 2 | 2 | — | — | — | — | — |
| 5.0 | 49 | 41 | — | 8 | — | — | — |

## Version 4.14 (69 jobs)

### AWS (46 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.14-amd64-nightly-4.14-upgrade-from-stable-4.14-aws-ipi-ovn-hypershift-mce-inplace-f60` |
| amd64 | MCE, Upgrade, Private | `release-4.14-amd64-nightly-4.14-upgrade-from-stable-4.14-aws-ipi-ovn-hypershift-mce-replace-f60` |
| arm64 | Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-f28` |
| arm64 | Private, Destructive | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-f28-destructive` |
| arm64 | Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-f60` |
| arm64 | Private, Destructive | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-f60-destructive` |
| arm64 | Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f28` |
| arm64 | Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f60` |
| amd64 | FIPS, Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f28` |
| amd64 | FIPS, Private, Destructive | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f28-destructive` |
| amd64 | FIPS, Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f60` |
| amd64 | FIPS, Private, Destructive | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f60-destructive` |
| amd64 | FIPS, Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-fips-mgmt-f28` |
| amd64 | FIPS, Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-fips-mgmt-f60` |
| amd64 | Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-guest-critical-f28` |
| amd64 | Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-guest-critical-f60` |
| amd64 | Private, LongDuration | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-install-f28-longduration` |
| amd64 | Private, LongDuration | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-install-f60-longduration` |
| amd64 | MCE, Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28` |
| amd64 | MCE, Private, Destructive | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-destructive` |
| amd64 | MCE, Private, LongDuration | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-longduration` |
| s390x | MCE, Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-mce-ibmz-guest-critical-f28` |
| s390x | MCE, Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-mce-ibmz-mgmt-critical-f28` |
| amd64 | MCE, Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-mce-mgmt-f28` |
| amd64 | MCE, Private, LongDuration | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-mce-mgmt-f28-longduration` |
| ppc64le | MCE, Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-mce-power-guest-critical-f28` |
| ppc64le | MCE, Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-mce-power-mgmt-critical-f28` |
| amd64 | Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f28` |
| amd64 | Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f60` |
| amd64 | Private, Destructive | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-pub-private-guest-f28-destructive` |
| amd64 | Private, Destructive | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-pub-private-guest-f60-destructive` |
| amd64 | Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-public-private-guest-f28` |
| amd64 | Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-public-private-guest-f60` |
| amd64 | Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-public-private-mgmt-f28` |
| amd64 | Private | `release-4.14-amd64-nightly-aws-ipi-ovn-hypershift-public-private-mgmt-f60` |
| amd64 | Private | `release-4.14-amd64-nightly-aws-rosa-hcp-byo-kms-oidc-auditlog-stage-full-f28` |
| amd64 | Private, Proxy | `release-4.14-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f28` |
| amd64 | Private, Proxy | `release-4.14-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f28` |
| amd64 | Private | `release-4.14-amd64-nightly-aws-rosa-hcp-stage-full-f28` |
| amd64 | Private | `release-4.14-amd64-stable-aws-rosa-hcp-byo-kms-oidc-auditlog-stage-critical-f28` |
| amd64 | Private, Proxy | `release-4.14-amd64-stable-aws-rosa-hcp-private-proxy-stage-critical-f28` |
| amd64 | Private | `release-4.14-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f28` |
| amd64 | Private, Proxy | `release-4.14-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f28` |
| amd64 | Private | `release-4.14-amd64-stable-aws-rosa-hcp-sector-prod-critical-f28` |
| amd64 | Private | `release-4.14-amd64-stable-aws-rosa-hcp-sector-prod-stable-critical-f28` |
| amd64 | Private | `release-4.14-amd64-stable-aws-rosa-hcp-stage-critical-f28` |

### Agent (BareMetal) (10 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.14-amd64-nightly-4.14-upgrade-from-stable-4.14-baremetalds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.14-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f28` |
| amd64 | MCE, Disconnected, Private | `release-4.14-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f28-des` |
| amd64 | MCE, Disconnected, Private | `release-4.14-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-mgmt-f28` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.14-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f28` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.14-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f28-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.14-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-mgmt-f28` |
| amd64 | MCE, Private | `release-4.14-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f28` |
| amd64 | MCE, Private | `release-4.14-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f28-des` |
| amd64 | MCE, Private | `release-4.14-amd64-nightly-baremetalds-hypershift-agent-mce-mgmt-f28` |

### KubeVirt (3 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | Private | `release-4.14-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-guest-f60` |
| amd64 | Private | `release-4.14-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-guest-f60-destr` |
| amd64 | Private | `release-4.14-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mgmt-f60` |

### KubeVirt (BareMetal) (10 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.14-amd64-nightly-4.14-upgrade-from-stable-4.14-baremetalds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | Private | `release-4.14-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-guest-f28` |
| amd64 | Private | `release-4.14-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-guest-f28-destr` |
| amd64 | Private | `release-4.14-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-guest-f60` |
| amd64 | Private | `release-4.14-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-guest-f60-destr` |
| amd64 | MCE, Private | `release-4.14-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f28` |
| amd64 | MCE, Private | `release-4.14-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f28-des` |
| amd64 | MCE, Private | `release-4.14-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-mgmt-f28` |
| amd64 | Private | `release-4.14-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mgmt-f28` |
| amd64 | Private | `release-4.14-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mgmt-f60` |

## Version 4.15 (120 jobs)

### AWS (84 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-aws-ipi-ovn-hypershift-mce-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-aws-ipi-ovn-hypershift-mce-mceupgrade-full-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-aws-ipi-ovn-hypershift-mce-mceupgrade-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-aws-ipi-ovn-hypershift-mce-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.15-aws-ipi-ovn-hypershift-mce-inplace-f60` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.15-aws-ipi-ovn-hypershift-mce-replace-f60` |
| arm64 | Private, EFS | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f14` |
| arm64 | Private, EFS, Destructive | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f14-destructive` |
| arm64 | Private, EFS | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f28` |
| arm64 | Private, EFS | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f60` |
| arm64 | Private, EFS, Destructive | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f60-destructive` |
| arm64 | Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f14` |
| arm64 | Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f28` |
| arm64 | Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f60` |
| amd64 | FIPS, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f14` |
| amd64 | FIPS, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f28` |
| amd64 | FIPS, Private, Destructive | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f28-destructive` |
| amd64 | FIPS, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f60` |
| amd64 | FIPS, Private, Destructive | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f60-destructive` |
| amd64 | FIPS, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-fips-mgmt-f14` |
| amd64 | FIPS, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-fips-mgmt-f28` |
| amd64 | FIPS, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-fips-mgmt-f60` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-guest-critical-f28` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-guest-critical-f60` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-guest-ext-oidc-f14` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-guest-ext-oidc-f28` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-guest-ext-oidc-f60` |
| amd64 | Private, LongDuration | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-install-f28-longduration` |
| amd64 | Private, LongDuration | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-install-f60-longduration` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f14` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28` |
| amd64 | MCE, Private, Destructive | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-destructive` |
| amd64 | MCE, Private, LongDuration | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-longduration` |
| s390x | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-ibmz-guest-critical-f14` |
| s390x | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-ibmz-guest-critical-f28` |
| s390x | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-ibmz-mgmt-critical-f14` |
| s390x | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-ibmz-mgmt-critical-f28` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-mgmt-f28` |
| amd64 | MCE, Private, LongDuration | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-mgmt-f28-longduration` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-n1minor-guest-f28` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-n1minor-mgmt-f28` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-n1minor-mgmt-f60` |
| ppc64le | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-power-guest-critical-f14` |
| ppc64le | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-power-mgmt-critical-f14` |
| ppc64le | MCE, Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mce-power-mgmt-critical-f28` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f28` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f60` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-byo-kms-oidc-auditlog-int-full-f28` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-byo-kms-oidc-auditlog-int-full-f60` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-byo-kms-oidc-auditlog-stage-full-f28` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-byo-kms-oidc-auditlog-stage-full-f60` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-capi-private-stage-f60` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-capi-stage-f28` |
| amd64 | Private, Cilium | `release-4.15-amd64-nightly-aws-rosa-hcp-cilium-stage-full-f14` |
| amd64 | Private, Cilium | `release-4.15-amd64-nightly-aws-rosa-hcp-cilium-stage-full-f28` |
| amd64 | Private, Cilium | `release-4.15-amd64-nightly-aws-rosa-hcp-cilium-stage-full-f60` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-int-full-f28` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-int-full-f60` |
| amd64 | Private, Proxy | `release-4.15-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f28` |
| amd64 | Private, Proxy | `release-4.15-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f60` |
| amd64 | Private, Proxy | `release-4.15-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f28` |
| amd64 | Private, Proxy | `release-4.15-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f60` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-security-group-private-stage-full-f28` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-security-group-private-stage-full-f60` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-security-group-stage-full-f28` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-security-group-stage-full-f60` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-stage-full-f28` |
| amd64 | Private | `release-4.15-amd64-nightly-aws-rosa-hcp-stage-full-f60` |
| amd64 | Private | `release-4.15-amd64-stable-aws-rosa-hcp-byo-kms-oidc-auditlog-stage-critical-f28` |
| amd64 | Private, Proxy | `release-4.15-amd64-stable-aws-rosa-hcp-private-proxy-stage-critical-f28` |
| amd64 | Private | `release-4.15-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f14` |
| amd64 | Private | `release-4.15-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f28` |
| amd64 | Private | `release-4.15-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f60` |
| amd64 | Private, Proxy | `release-4.15-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f14` |
| amd64 | Private, Proxy | `release-4.15-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f28` |
| amd64 | Private, Proxy | `release-4.15-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f60` |
| amd64 | Private, Proxy | `release-4.15-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-stable-critical-f28` |
| amd64 | Private, Proxy | `release-4.15-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-stable-critical-f60` |
| amd64 | Private | `release-4.15-amd64-stable-aws-rosa-hcp-sector-prod-critical-f14` |
| amd64 | Private | `release-4.15-amd64-stable-aws-rosa-hcp-sector-prod-critical-f60` |
| amd64 | Private | `release-4.15-amd64-stable-aws-rosa-hcp-security-group-f28` |
| amd64 | Private | `release-4.15-amd64-stable-aws-rosa-hcp-security-group-private-f28` |
| amd64 | Private | `release-4.15-amd64-stable-aws-rosa-hcp-stage-critical-f28` |

### Agent (BareMetal) (22 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-baremetalds-agent-hypershift-mce-compact-full-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-baremetalds-agent-hypershift-mce-compact-full-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-baremetalds-agent-hypershift-mce-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-baremetalds-agent-hypershift-mce-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-baremetalds-agent-hypershift-mce-mceupgrade-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-baremetalds-agent-hypershift-mce-mceupgrade-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.15-baremetalds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f14` |
| amd64 | MCE, Disconnected, Private | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f28` |
| amd64 | MCE, Disconnected, Private | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f28-des` |
| amd64 | MCE, Disconnected, Private | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-mgmt-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f28` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f28-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-mgmt-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-mgmt-f60` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f14-destructive` |
| amd64 | MCE, Private, Destructive | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f28-destructive` |
| amd64 | MCE, Private, Destructive | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f60-destructive` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-baremetalds-hypershift-agent-mce-mgmt-f28` |

### KubeVirt (BareMetal) (14 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-baremetalds-kubevirt-hypershift-mce-mceupgrade-replace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-baremetalds-kubevirt-hypershift-mce-mceupgrade-replace-f60` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-baremetalds-kubevirt-hypershift-mce-replace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.14-baremetalds-kubevirt-hypershift-mce-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.15-amd64-nightly-4.15-upgrade-from-stable-4.15-baremetalds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f14` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f14-des` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f28` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f28-des` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f60-des` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-mgmt-f28` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n1minor-guest-f28` |
| amd64 | MCE, Private | `release-4.15-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n1minor-mgmt-f28` |

## Version 4.16 (123 jobs)

### AWS (57 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-aws-ipi-ovn-hypershift-mce-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-aws-ipi-ovn-hypershift-mce-mceupgrade-full-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-aws-ipi-ovn-hypershift-mce-mceupgrade-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-aws-ipi-ovn-hypershift-mce-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-aws-ipi-ovn-hypershift-mce-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-aws-ipi-ovn-hypershift-mce-mceupgrade-full-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-aws-ipi-ovn-hypershift-mce-mceupgrade-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-aws-ipi-ovn-hypershift-mce-replace-f28` |
| amd64 | Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-aws-ipi-ovn-rosa-hcp-upgrade-cp-stage-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.16-aws-ipi-ovn-hypershift-mce-inplace-f60` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.16-aws-ipi-ovn-hypershift-mce-replace-f60` |
| arm64 | Private, EFS | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f14` |
| arm64 | Private, EFS, Destructive | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f28-destructive` |
| arm64 | Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f14` |
| amd64 | FIPS, Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f14` |
| amd64 | FIPS, Private, Destructive | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f28-destructive` |
| amd64 | FIPS, Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-fips-mgmt-f14` |
| amd64 | Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-guest-critical-f28` |
| amd64 | Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-guest-ext-oidc-f14` |
| amd64 | Private, LongDuration | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-install-f28-longduration` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-destructive` |
| amd64 | MCE, Private, LongDuration | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-longduration` |
| s390x | MCE, Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-mce-ibmz-guest-critical-f14` |
| s390x | MCE, Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-mce-ibmz-mgmt-critical-f14` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private, LongDuration | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-mce-mgmt-f28-longduration` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-mce-n2minor-mgmt-f28` |
| ppc64le | MCE, Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-mce-power-guest-critical-f14` |
| ppc64le | MCE, Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-mce-power-mgmt-critical-f14` |
| amd64 | Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f28` |
| amd64 | Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-private-guest-f14` |
| amd64 | Private | `release-4.16-amd64-nightly-aws-ipi-ovn-hypershift-private-mgmt-f14` |
| amd64 | Private | `release-4.16-amd64-nightly-aws-rosa-hcp-byo-kms-oidc-auditlog-int-full-f28` |
| amd64 | Private | `release-4.16-amd64-nightly-aws-rosa-hcp-byo-kms-oidc-auditlog-stage-full-f28` |
| amd64 | Private | `release-4.16-amd64-nightly-aws-rosa-hcp-external-auth-stage-full-f28` |
| amd64 | Private | `release-4.16-amd64-nightly-aws-rosa-hcp-int-full-f28` |
| amd64 | Private, Proxy | `release-4.16-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f28` |
| amd64 | Private | `release-4.16-amd64-nightly-aws-rosa-hcp-security-group-private-stage-full-f28` |
| amd64 | Private | `release-4.16-amd64-nightly-aws-rosa-hcp-security-group-stage-full-f28` |
| amd64 | Private | `release-4.16-amd64-nightly-aws-rosa-hcp-stage-full-f28` |
| amd64 | Private | `release-4.16-amd64-rollback-nightly-aws-ipi-ovn-hypershift-inplace-f28` |
| amd64 | Private | `release-4.16-amd64-stable-aws-ipi-ovn-hypershift-to-multiarch-f14` |
| amd64 | Private | `release-4.16-amd64-stable-aws-rosa-hcp-byo-kms-oidc-auditlog-stage-critical-f28` |
| amd64 | Upgrade, Private | `release-4.16-amd64-stable-aws-rosa-hcp-capi-upgrade-f14` |
| amd64 | Private, Proxy | `release-4.16-amd64-stable-aws-rosa-hcp-private-proxy-stage-critical-f28` |
| amd64 | Private | `release-4.16-amd64-stable-aws-rosa-hcp-sector-advanced-prod-stable-critical-f28` |
| amd64 | Private | `release-4.16-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f14` |
| amd64 | Private, Proxy | `release-4.16-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f14` |
| amd64 | Private | `release-4.16-amd64-stable-aws-rosa-hcp-sector-prod-critical-f14` |
| amd64 | Private | `release-4.16-amd64-stable-aws-rosa-hcp-security-group-f28` |
| amd64 | Private | `release-4.16-amd64-stable-aws-rosa-hcp-security-group-private-f28` |
| amd64 | Private | `release-4.16-amd64-stable-aws-rosa-hcp-stage-critical-f28` |
| multi | Private | `release-4.16-multi-nightly-aws-ipi-ovn-hypershift-guest-f14` |
| multi | Private, Destructive | `release-4.16-multi-nightly-aws-ipi-ovn-hypershift-guest-f28-destructive` |
| multi | Private | `release-4.16-multi-nightly-aws-ipi-ovn-hypershift-mgmt-f14` |

### Agent (BareMetal) (18 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-baremetalds-agent-hypershift-mce-compact-full-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-baremetalds-agent-hypershift-mce-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-baremetalds-agent-hypershift-mce-mceupgrade-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-baremetalds-agent-hypershift-mce-compact-full-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-baremetalds-agent-hypershift-mce-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-baremetalds-agent-hypershift-mce-mceupgrade-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.16-baremetalds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.16-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f14` |
| amd64 | MCE, Disconnected, Private | `release-4.16-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f14-des` |
| amd64 | MCE, Disconnected, Private | `release-4.16-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-mgmt-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.16-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.16-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f14-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.16-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-mgmt-f14` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.16-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f28-destructive` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-baremetalds-hypershift-agent-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-baremetalds-hypershift-agent-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-baremetalds-hypershift-agent-mce-n2minor-mgmt-f28` |

### KubeVirt (12 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-metal-ds-kubevirt-hypershift-mce-mceupgrade-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-metal-ds-kubevirt-hypershift-mce-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-metal-ds-kubevirt-hypershift-mce-mceupgrade-replace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-metal-ds-kubevirt-hypershift-mce-replace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.16-metal-ds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hcp-mce-multinet-guest-f14` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hcp-mce-multinet-mgmt-f14` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-guest-f14` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-guest-f14-des` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n2minor-mgmt-f28` |

### KubeVirt (BareMetal) (12 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-baremetalds-kubevirt-hypershift-mce-mceupgrade-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-baremetalds-kubevirt-hypershift-mce-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-baremetalds-kubevirt-hypershift-mce-mceupgrade-replace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-baremetalds-kubevirt-hypershift-mce-replace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.16-baremetalds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hcp-mce-multinet-guest-f14` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hcp-mce-multinet-mgmt-f14` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f14` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f14-des` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n2minor-mgmt-f28` |

### Other (24 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-metal-ds-agent-hypershift-mce-compact-full-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-metal-ds-agent-hypershift-mce-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-eus-upgrade-from-4.14-metal-ds-agent-hypershift-mce-mceupgrade-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-metal-ds-agent-hypershift-mce-compact-full-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-metal-ds-agent-hypershift-mce-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.15-metal-ds-agent-hypershift-mce-mceupgrade-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.16-amd64-nightly-4.16-upgrade-from-stable-4.16-metal-ds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.16-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-guest-f14` |
| amd64 | MCE, Disconnected, Private | `release-4.16-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-guest-f14-des` |
| amd64 | MCE, Disconnected, Private | `release-4.16-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-mgmt-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.16-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-guest-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.16-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-guest-f14-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.16-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-mgmt-f14` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-metal-ds-hypershift-agent-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.16-amd64-nightly-metal-ds-hypershift-agent-mce-guest-f28-destructive` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-metal-ds-hypershift-agent-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-metal-ds-hypershift-agent-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.16-amd64-nightly-metal-ds-hypershift-agent-mce-n2minor-mgmt-f28` |
| s390x | MCE, Upgrade, Private | `release-4.16-multi-nightly-4.16-eus-upgrade-from-4.14-ibmz-hypershift-mce-replace-f28` |
| ppc64le | MCE, Upgrade, Private | `release-4.16-multi-nightly-4.16-eus-upgrade-from-4.14-power-hypershift-mce-replace-f28` |
| multi | Private | `release-4.16-multi-nightly-baremetal-compact-agent-ipv4-dhcp-day2-amd-mixarch-f28` |
| arm64 | Private | `release-4.16-multi-nightly-baremetal-compact-agent-ipv4-dhcp-day2-arm-mixarch-f28` |
| multi | Private | `release-4.16-multi-nightly-baremetal-compact-agent-ipv4-dhcp-disc-day2-amd-mixarch-f28` |
| arm64 | Private | `release-4.16-multi-nightly-baremetal-compact-agent-ipv4-dhcp-disc-day2-arm-mixarch-f28` |

## Version 4.17 (102 jobs)

### AWS (65 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | Upgrade, Private | `release-4.17-amd64-nightly-4.17-upgrade-from-stable-4.16-aws-ipi-ovn-hypershift-replace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.17-amd64-nightly-4.17-upgrade-from-stable-4.17-aws-ipi-ovn-hypershift-mce-inplace-f60` |
| amd64 | MCE, Upgrade, Private | `release-4.17-amd64-nightly-4.17-upgrade-from-stable-4.17-aws-ipi-ovn-hypershift-mce-replace-f60` |
| arm64 | Private, EFS | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f14` |
| arm64 | Private, EFS, Destructive | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f28-destructive` |
| arm64 | Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f14` |
| amd64 | FIPS, Private, Destructive | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f28-destructive` |
| amd64 | FIPS, Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-openldap-f14` |
| amd64 | FIPS, Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-fips-mgmt-f14` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-guest-advanced-f14` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-guest-ext-oidc-f14` |
| amd64 | Private, Destructive | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-guest-f28-destructive` |
| arm64 | MCE, Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-mce-arm-nodepool-guest-f14` |
| arm64 | MCE, Private, Destructive | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-mce-arm-nodepool-guest-f28-destructive` |
| arm64 | MCE, Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-mce-arm-nodepool-mgmt-f14` |
| arm64 | MCE, Private, LongDuration | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-mce-arm-nodepool-mgmt-f28-longduration` |
| arm64 | MCE, Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-mce-arm-nodepool-n1minor-guest-f28` |
| arm64 | MCE, Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-mce-arm-nodepool-n1minor-mgmt-f28` |
| s390x | MCE, Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-mce-ibmz-guest-critical-f14` |
| s390x | MCE, Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-mce-ibmz-mgmt-critical-f14` |
| ppc64le | MCE, Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-mce-power-guest-critical-f14` |
| ppc64le | MCE, Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-mce-power-mgmt-critical-f14` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f14` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-f14` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-private-guest-f14` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-ipi-ovn-hypershift-private-mgmt-f14` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-rosa-hcp-byo-kms-oidc-auditlog-int-full-f14` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-rosa-hcp-byo-kms-oidc-auditlog-int-full-f28` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-rosa-hcp-byo-kms-oidc-auditlog-stage-full-f14` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-rosa-hcp-byo-kms-oidc-auditlog-stage-full-f28` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-rosa-hcp-external-auth-stage-full-f28` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-rosa-hcp-int-full-f14` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-rosa-hcp-int-full-f28` |
| amd64 | Private, Proxy | `release-4.17-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f14` |
| amd64 | Private, Proxy | `release-4.17-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f28` |
| amd64 | Private, Proxy | `release-4.17-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f14` |
| amd64 | Private, Proxy | `release-4.17-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f28` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-rosa-hcp-security-group-private-stage-full-f14` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-rosa-hcp-security-group-private-stage-full-f28` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-rosa-hcp-security-group-stage-full-f14` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-rosa-hcp-security-group-stage-full-f28` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-rosa-hcp-stage-full-f14` |
| amd64 | Private | `release-4.17-amd64-nightly-aws-rosa-hcp-stage-full-f28` |
| amd64 | Private | `release-4.17-amd64-rollback-nightly-aws-ipi-ovn-hypershift-inplace-f28` |
| amd64 | Private | `release-4.17-amd64-stable-aws-rosa-hcp-advanced-stage-critical-f14` |
| amd64 | Private | `release-4.17-amd64-stable-aws-rosa-hcp-byo-kms-oidc-auditlog-stage-critical-f14` |
| amd64 | Private | `release-4.17-amd64-stable-aws-rosa-hcp-byo-kms-oidc-auditlog-stage-critical-f28` |
| amd64 | Private, Proxy | `release-4.17-amd64-stable-aws-rosa-hcp-private-proxy-stage-critical-f14` |
| amd64 | Private | `release-4.17-amd64-stable-aws-rosa-hcp-sector-advanced-prod-stable-critical-f28` |
| amd64 | Private | `release-4.17-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f14` |
| amd64 | Private | `release-4.17-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f7` |
| amd64 | Private, Proxy | `release-4.17-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f14` |
| amd64 | Private, Proxy | `release-4.17-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f7` |
| amd64 | Private | `release-4.17-amd64-stable-aws-rosa-hcp-sector-prod-critical-f14` |
| amd64 | Private | `release-4.17-amd64-stable-aws-rosa-hcp-sector-prod-critical-f7` |
| amd64 | Private | `release-4.17-amd64-stable-aws-rosa-hcp-security-group-f14` |
| amd64 | Private | `release-4.17-amd64-stable-aws-rosa-hcp-security-group-f28` |
| amd64 | Private | `release-4.17-amd64-stable-aws-rosa-hcp-security-group-private-f14` |
| amd64 | Private | `release-4.17-amd64-stable-aws-rosa-hcp-stage-critical-f14` |
| amd64 | Private | `release-4.17-amd64-stable-aws-rosa-hcp-stage-critical-f28` |
| arm64 | MCE, Private | `release-4.17-arm64-nightly-aws-ipi-ovn-hypershift-mce-guest-f14` |
| arm64 | MCE, Private, Destructive | `release-4.17-arm64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-destructive` |
| arm64 | MCE, Private, LongDuration | `release-4.17-arm64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-longduration` |
| arm64 | MCE, Private | `release-4.17-arm64-nightly-aws-ipi-ovn-hypershift-mce-mgmt-f14` |
| arm64 | MCE, Private, LongDuration | `release-4.17-arm64-nightly-aws-ipi-ovn-hypershift-mce-mgmt-f28-longduration` |

### Agent (BareMetal) (15 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.17-amd64-nightly-4.17-upgrade-from-stable-4.16-baremetalds-agent-hypershift-mce-compact-full-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.17-amd64-nightly-4.17-upgrade-from-stable-4.16-baremetalds-agent-hypershift-mce-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.17-amd64-nightly-4.17-upgrade-from-stable-4.16-baremetalds-agent-hypershift-mce-mceupgrade-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.17-amd64-nightly-4.17-upgrade-from-stable-4.17-baremetalds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.17-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f14` |
| amd64 | MCE, Disconnected, Private | `release-4.17-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f14-des` |
| amd64 | MCE, Disconnected, Private | `release-4.17-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-mgmt-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.17-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.17-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f14-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.17-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-mgmt-f14` |
| amd64 | MCE, Private | `release-4.17-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.17-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f28-destructive` |
| amd64 | MCE, Private | `release-4.17-amd64-nightly-baremetalds-hypershift-agent-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.17-amd64-nightly-baremetalds-hypershift-agent-mce-n1minor-guest-f28` |
| amd64 | MCE, Private | `release-4.17-amd64-nightly-baremetalds-hypershift-agent-mce-n1minor-mgmt-f28` |

### KubeVirt (3 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.17-amd64-nightly-4.17-upgrade-from-stable-4.17-metal-ds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | MCE, Private | `release-4.17-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n1minor-guest-f28` |
| amd64 | MCE, Private | `release-4.17-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n1minor-mgmt-f28` |

### KubeVirt (BareMetal) (3 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.17-amd64-nightly-4.17-upgrade-from-stable-4.17-baremetalds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | MCE, Private | `release-4.17-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n1minor-guest-f28` |
| amd64 | MCE, Private | `release-4.17-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n1minor-mgmt-f28` |

### Other (16 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.17-amd64-nightly-4.17-upgrade-from-stable-4.16-metal-ds-agent-hypershift-mce-compact-full-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.17-amd64-nightly-4.17-upgrade-from-stable-4.16-metal-ds-agent-hypershift-mce-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.17-amd64-nightly-4.17-upgrade-from-stable-4.16-metal-ds-agent-hypershift-mce-mceupgrade-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.17-amd64-nightly-4.17-upgrade-from-stable-4.17-metal-ds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.17-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-guest-f14` |
| amd64 | MCE, Disconnected, Private | `release-4.17-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-guest-f14-des` |
| amd64 | MCE, Disconnected, Private | `release-4.17-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-mgmt-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.17-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-guest-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.17-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-guest-f14-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.17-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-mgmt-f14` |
| amd64 | MCE, Private | `release-4.17-amd64-nightly-metal-ds-hypershift-agent-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.17-amd64-nightly-metal-ds-hypershift-agent-mce-guest-f28-destructive` |
| amd64 | MCE, Private | `release-4.17-amd64-nightly-metal-ds-hypershift-agent-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.17-amd64-nightly-metal-ds-hypershift-agent-mce-n1minor-guest-f28` |
| amd64 | MCE, Private | `release-4.17-amd64-nightly-metal-ds-hypershift-agent-mce-n1minor-mgmt-f28` |
| multi | Upgrade, Private | `release-4.17-multi-nightly-4.17-upgrade-from-stable-4.16-baremetal-compact-agent-ipv4-dhcp-day2-amd-mixarch-f28` |

## Version 4.18 (148 jobs)

### AWS (91 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-aws-ipi-ovn-hypershift-mce-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-aws-ipi-ovn-hypershift-mce-mceupgrade-full-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-aws-ipi-ovn-hypershift-mce-mceupgrade-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-aws-ipi-ovn-hypershift-mce-replace-f28` |
| amd64 | Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-aws-ipi-ovn-hypershift-replace-f28` |
| amd64 | Upgrade, Private | `release-4.18-amd64-nightly-4.18-upgrade-from-stable-4.17-aws-ipi-ovn-hypershift-replace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-upgrade-from-stable-4.18-aws-ipi-ovn-hypershift-mce-inplace-f60` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-upgrade-from-stable-4.18-aws-ipi-ovn-hypershift-mce-replace-f60` |
| arm64 | Private, EFS | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f14` |
| arm64 | Private, EFS, Destructive | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f28-destructive` |
| arm64 | Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f14` |
| amd64 | FIPS, Private, Destructive | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f28-destructive` |
| amd64 | FIPS, Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-openldap-f14` |
| amd64 | FIPS, Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-fips-mgmt-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-guest-advanced-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-guest-critical-f28` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-guest-ext-oidc-f14` |
| amd64 | Private, Destructive | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-guest-f28-destructive` |
| amd64 | Private, IPSec | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-guest-ipsec-f14` |
| amd64 | Private, LongDuration | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-guest-longduration-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-install-f14` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-destructive` |
| amd64 | MCE, Private, LongDuration | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-longduration` |
| s390x | MCE, Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-mce-ibmz-guest-critical-f14` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private, LongDuration | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-mce-mgmt-f28-longduration` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-mce-n2minor-mgmt-f28` |
| ppc64le | MCE, Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-mce-power-guest-critical-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-private-guest-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-private-mgmt-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-guest-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-mgmt-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-advanced-int-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-advanced-stage-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-advanced-stage-f7` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-byo-kms-oidc-auditlog-int-full-f7` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-byo-kms-oidc-auditlog-stage-full-f7` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-external-auth-stage-full-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-external-auth-stage-full-f7` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-external-auth-stage-full-int-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-int-full-f7` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-pl-int-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-pl-stage-f7` |
| amd64 | Private, Proxy | `release-4.18-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f14` |
| amd64 | Private, Proxy | `release-4.18-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f7` |
| amd64 | Private, Proxy | `release-4.18-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f14` |
| amd64 | Private, Proxy | `release-4.18-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f7` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-security-group-private-stage-full-f7` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-f7` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-int-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-stage-full-f7` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-zero-egress-int-f14` |
| amd64 | Private | `release-4.18-amd64-nightly-aws-rosa-hcp-zero-egress-stage-f7` |
| amd64 | Private | `release-4.18-amd64-rollback-nightly-aws-ipi-ovn-hypershift-inplace-f28` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-advanced-int-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-advanced-stage-critical-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-advanced-stage-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-external-auth-stage-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-external-auth-stage-full-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-external-auth-stage-full-int-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-pl-int-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-pl-stage-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-sector-advanced-prod-stable-critical-f28` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f7` |
| amd64 | Private, Proxy | `release-4.18-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f14` |
| amd64 | Private, Proxy | `release-4.18-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f7` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-sector-prod-critical-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-sector-prod-critical-f7` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-security-group-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-security-group-private-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-int-f14` |
| amd64 | Upgrade, Private | `release-4.18-amd64-stable-aws-rosa-hcp-upgrade-f28` |
| amd64 | Upgrade, Private | `release-4.18-amd64-stable-aws-rosa-hcp-upgrade-f999` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-zero-egress-int-f14` |
| amd64 | Private | `release-4.18-amd64-stable-aws-rosa-hcp-zero-egress-stage-f14` |
| arm64 | MCE, Private | `release-4.18-arm64-nightly-aws-ipi-ovn-hypershift-mce-guest-f14` |
| arm64 | MCE, Private, Destructive | `release-4.18-arm64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-destructive` |
| arm64 | MCE, Private, LongDuration | `release-4.18-arm64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-longduration` |
| multi | Private | `release-4.18-multi-nightly-aws-ipi-ovn-amd-hypershift-guest-mto-f14` |
| arm64 | Private | `release-4.18-multi-nightly-aws-ipi-ovn-arm-mixarch-mto-hypershift-arm-guest-f14` |
| arm64 | Private | `release-4.18-multi-nightly-aws-ipi-ovn-arm-mixarch-mto-hypershift-arm-mgmt-f14` |
| multi | Private | `release-4.18-multi-nightly-aws-ipi-ovn-hypershift-guest-f14` |
| multi | Private, Destructive | `release-4.18-multi-nightly-aws-ipi-ovn-hypershift-guest-f28-destructive` |
| multi | Private | `release-4.18-multi-nightly-aws-ipi-ovn-hypershift-mgmt-f14` |

### Agent (BareMetal) (19 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-baremetalds-agent-hypershift-mce-compact-full-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-baremetalds-agent-hypershift-mce-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-baremetalds-agent-hypershift-mce-mceupgrade-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-upgrade-from-stable-4.17-baremetalds-agent-hypershift-mce-compact-full-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-upgrade-from-stable-4.17-baremetalds-agent-hypershift-mce-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-upgrade-from-stable-4.17-baremetalds-agent-hypershift-mce-mceupgrade-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-upgrade-from-stable-4.18-baremetalds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.18-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f14` |
| amd64 | MCE, Disconnected, Private | `release-4.18-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f14-des` |
| amd64 | MCE, Disconnected, Private | `release-4.18-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-mgmt-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.18-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.18-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f14-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.18-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-mgmt-f14` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.18-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f28-destructive` |
| arm64 | MCE, Private | `release-4.18-amd64-nightly-baremetalds-hypershift-agent-mce-lab-arm-mgmt-f28` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-baremetalds-hypershift-agent-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-baremetalds-hypershift-agent-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-baremetalds-hypershift-agent-mce-n2minor-mgmt-f28` |

### KubeVirt (8 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-metal-ds-kubevirt-hypershift-mce-mceupgrade-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-metal-ds-kubevirt-hypershift-mce-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-upgrade-from-stable-4.18-metal-ds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-guest-f14` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-guest-f14-des` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n2minor-mgmt-f28` |

### KubeVirt (BareMetal) (8 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-baremetalds-kubevirt-hypershift-mce-mceupgrade-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-baremetalds-kubevirt-hypershift-mce-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-upgrade-from-stable-4.18-baremetalds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f14` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f14-des` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n2minor-mgmt-f28` |

### Other (22 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-metal-ds-agent-hypershift-mce-compact-full-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-metal-ds-agent-hypershift-mce-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-eus-upgrade-from-4.16-metal-ds-agent-hypershift-mce-mceupgrade-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-upgrade-from-stable-4.17-metal-ds-agent-hypershift-mce-compact-full-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-upgrade-from-stable-4.17-metal-ds-agent-hypershift-mce-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-upgrade-from-stable-4.17-metal-ds-agent-hypershift-mce-mceupgrade-inplace-f14` |
| amd64 | MCE, Upgrade, Private | `release-4.18-amd64-nightly-4.18-upgrade-from-stable-4.18-metal-ds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.18-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-guest-f14` |
| amd64 | MCE, Disconnected, Private | `release-4.18-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-guest-f14-des` |
| amd64 | MCE, Disconnected, Private | `release-4.18-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-mgmt-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.18-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-guest-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.18-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-guest-f14-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.18-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-mgmt-f14` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-metal-ds-hypershift-agent-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.18-amd64-nightly-metal-ds-hypershift-agent-mce-guest-f28-destructive` |
| arm64 | MCE, Private | `release-4.18-amd64-nightly-metal-ds-hypershift-agent-mce-lab-arm-mgmt-f28` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-metal-ds-hypershift-agent-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-metal-ds-hypershift-agent-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.18-amd64-nightly-metal-ds-hypershift-agent-mce-n2minor-mgmt-f28` |
| arm64 | Private | `release-4.18-amd64-nightly-metal3-agent-hypershift-arm-nodepool-guest-f28` |
| s390x | MCE, Upgrade, Private | `release-4.18-multi-nightly-4.18-eus-upgrade-from-4.16-ibmz-hypershift-mce-replace-f28` |
| ppc64le | MCE, Upgrade, Private | `release-4.18-multi-nightly-4.18-eus-upgrade-from-4.16-power-hypershift-mce-replace-f28` |

## Version 4.19 (172 jobs)

### AWS (98 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | Upgrade, Private | `release-4.19-amd64-nightly-4.19-upgrade-from-stable-4.17-aws-ipi-ovn-hypershift-replace-f28` |
| amd64 | Upgrade, Private | `release-4.19-amd64-nightly-4.19-upgrade-from-stable-4.18-aws-ipi-ovn-hypershift-replace-f14` |
| amd64 | Upgrade, Private | `release-4.19-amd64-nightly-4.19-upgrade-from-stable-4.18-aws-ipi-ovn-hypershift-replace-f7` |
| amd64 | MCE, Upgrade, Private | `release-4.19-amd64-nightly-4.19-upgrade-from-stable-4.19-aws-ipi-ovn-hypershift-mce-inplace-f60` |
| amd64 | MCE, Upgrade, Private | `release-4.19-amd64-nightly-4.19-upgrade-from-stable-4.19-aws-ipi-ovn-hypershift-mce-replace-f60` |
| amd64 | Private, Cilium | `release-4.19-amd64-nightly-aws-ipi-cilium-hypershift-guest-f14` |
| amd64 | Private, Cilium | `release-4.19-amd64-nightly-aws-ipi-cilium-hypershift-guest-f7` |
| arm64 | Private, EFS | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f14` |
| arm64 | Private, EFS, Destructive | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f14-destructive` |
| arm64 | Private, EFS | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f7` |
| arm64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f14` |
| arm64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f7` |
| amd64 | FIPS, Private, Destructive | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f28-destructive` |
| amd64 | FIPS, Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f999-compliance` |
| amd64 | FIPS, Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-openldap-f14` |
| amd64 | FIPS, Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-fips-mgmt-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-guest-dynamic-dns-advanced-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-guest-dynamic-dns-ondemand-advanced-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-guest-dynamicdns-ondemand-advanced-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-guest-ext-oidc-tp-f14` |
| amd64 | Private, Destructive | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-guest-f14-destructive` |
| amd64 | Private, IPSec | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-guest-ipsec-f14` |
| amd64 | Private, LongDuration | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-guest-longduration-f14` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-destructive` |
| amd64 | MCE, Private, LongDuration | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mce-guest-f28-longduration` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private, LongDuration | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mce-mgmt-f28-longduration` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mce-n1minor-guest-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mce-n1minor-mgmt-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mce-n2minor-mgmt-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mce-n3minor-guest-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mce-n3minor-mgmt-f28` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-f7` |
| amd64 | Private, LongDuration | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-longduration-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-private-guest-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-private-guest-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-private-mgmt-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-private-mgmt-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-guest-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-guest-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-mgmt-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-mgmt-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-advanced-int-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-advanced-int-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-advanced-stage-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-external-auth-int-full-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-external-auth-int-full-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-external-auth-stage-full-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-pl-int-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-pl-int-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-pl-stage-f7` |
| amd64 | Private, Proxy | `release-4.19-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f14` |
| amd64 | Private, Proxy | `release-4.19-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f7` |
| amd64 | Private, Proxy | `release-4.19-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f14` |
| amd64 | Private, Proxy | `release-4.19-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-int-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-int-f7` |
| amd64 | Upgrade, Private | `release-4.19-amd64-nightly-aws-rosa-hcp-upgrade-f999` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-zero-egress-int-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-zero-egress-int-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-aws-rosa-hcp-zero-egress-stage-f7` |
| amd64 | Private | `release-4.19-amd64-rollback-nightly-aws-ipi-ovn-hypershift-inplace-f28` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-advanced-int-f14` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-advanced-int-f7` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-advanced-stage-f14` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-advanced-stage-f7` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-external-auth-stage-full-f14` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-external-auth-stage-full-f7` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-external-auth-stage-full-int-f14` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-external-auth-stage-full-int-f7` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-pl-int-f14` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-pl-int-f7` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-pl-stage-f14` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-pl-stage-f7` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-sector-advanced-prod-stable-critical-f28` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f14` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f7` |
| amd64 | Private, Proxy | `release-4.19-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f14` |
| amd64 | Private, Proxy | `release-4.19-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f7` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-sector-prod-critical-f14` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-sector-prod-critical-f7` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-f14` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-f7` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-int-f14` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-int-f7` |
| amd64 | Upgrade, Private | `release-4.19-amd64-stable-aws-rosa-hcp-upgrade-f999` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-zero-egress-int-f14` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-zero-egress-int-f7` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-zero-egress-stage-f14` |
| amd64 | Private | `release-4.19-amd64-stable-aws-rosa-hcp-zero-egress-stage-f7` |
| arm64 | Private | `release-4.19-multi-nightly-aws-ipi-ovn-arm-mixarch-mto-hypershift-arm-guest-f14` |
| arm64 | Private | `release-4.19-multi-nightly-aws-ipi-ovn-arm-mixarch-mto-hypershift-arm-mgmt-f14` |

### Agent (BareMetal) (13 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.19-amd64-nightly-4.19-upgrade-from-stable-4.19-baremetalds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.19-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f14` |
| amd64 | MCE, Disconnected, Private | `release-4.19-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-mgmt-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.19-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.19-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f14-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.19-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-mgmt-f14` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f14` |
| arm64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-hypershift-agent-mce-lab-arm-mgmt-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-hypershift-agent-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-hypershift-agent-mce-n1minor-guest-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-hypershift-agent-mce-n1minor-mgmt-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-hypershift-agent-mce-n3minor-guest-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-hypershift-agent-mce-n3minor-mgmt-f28` |

### Azure (27 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | Upgrade, Private | `release-4.19-amd64-nightly-4.19-upgrade-from-stable-4.18-azure-aks-hypershift-byo-vnet-replace-guest-f28` |
| amd64 | Upgrade, Private | `release-4.19-amd64-nightly-4.19-upgrade-from-stable-4.18-azure-aks-hypershift-etcd-disk-encryption-replace-guest-f28` |
| amd64 | Upgrade, Private | `release-4.19-amd64-nightly-4.19-upgrade-from-stable-4.18-azure-aks-hypershift-registry-overrides-replace-guest-f28` |
| arm64 | Private | `release-4.19-amd64-nightly-azure-aks-hypershift-arm-nodepool-guest-f14` |
| arm64 | Private | `release-4.19-amd64-nightly-azure-aks-hypershift-arm-nodepool-guest-f7` |
| amd64 | FIPS, Private | `release-4.19-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f14` |
| amd64 | FIPS, Private, Destructive | `release-4.19-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f14-destructive` |
| amd64 | FIPS, Private, LongDuration | `release-4.19-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f14-longduration` |
| amd64 | FIPS, Private | `release-4.19-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f7` |
| amd64 | FIPS, Private | `release-4.19-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-mgmt-f14` |
| amd64 | Private, Cilium | `release-4.19-amd64-nightly-azure-aks-hypershift-cilium-guest-f14` |
| amd64 | Private, Cilium | `release-4.19-amd64-nightly-azure-aks-hypershift-cilium-guest-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-azure-aks-hypershift-disaster-recovery-infra-guest-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-global-ps-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-global-ps-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-azure-aks-hypershift-etcd-disk-encryption-guest-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-azure-aks-hypershift-etcd-disk-encryption-guest-f7` |
| amd64 | Private | `release-4.19-amd64-nightly-azure-aks-hypershift-ext-oidc-tp-guest-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-azure-aks-hypershift-full-cert-guest-f14` |
| amd64 | Private, LongDuration | `release-4.19-amd64-nightly-azure-aks-hypershift-install-f14-longduration` |
| amd64 | Private | `release-4.19-amd64-nightly-azure-aks-hypershift-registry-overrides-guest-f14` |
| amd64 | Private | `release-4.19-amd64-nightly-azure-aks-hypershift-registry-overrides-guest-f7` |
| amd64 | Private | `release-4.19-amd64-rollback-nightly-azure-aks-hypershift-byo-vnet-replace-guest-f28` |
| multi | Private | `release-4.19-multi-nightly-azure-aks-hypershift-guest-f14` |
| multi | Private | `release-4.19-multi-nightly-azure-aks-hypershift-guest-reversed-f14` |

### KubeVirt (9 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.19-amd64-nightly-4.19-upgrade-from-stable-4.19-metal-ds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | Private, IPv6/DualStack | `release-4.19-amd64-nightly-metal-ds-ipi-ovn-dualstack-kubevirt-hypershift-f14` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-guest-f14` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-guest-f14-des` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n1minor-guest-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n1minor-mgmt-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n3minor-guest-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n3minor-mgmt-f28` |

### KubeVirt (BareMetal) (11 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.19-amd64-nightly-4.19-upgrade-from-stable-4.19-baremetalds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | Private, IPv6/DualStack | `release-4.19-amd64-nightly-baremetalds-ipi-ovn-dualstack-kubevirt-hypershift-f14` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f14` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f14-des` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n1minor-guest-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n1minor-mgmt-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n2minor-mgmt-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n3minor-guest-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n3minor-mgmt-f28` |

### Other (14 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.19-amd64-nightly-4.19-upgrade-from-stable-4.19-metal-ds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.19-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-guest-f14` |
| amd64 | MCE, Disconnected, Private | `release-4.19-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-guest-f14-des` |
| amd64 | MCE, Disconnected, Private | `release-4.19-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-mgmt-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.19-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-guest-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.19-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-guest-f14-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.19-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-mgmt-f14` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-metal-ds-hypershift-agent-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.19-amd64-nightly-metal-ds-hypershift-agent-mce-guest-f28-destructive` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-metal-ds-hypershift-agent-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-metal-ds-hypershift-agent-mce-n1minor-guest-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-metal-ds-hypershift-agent-mce-n1minor-mgmt-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-metal-ds-hypershift-agent-mce-n3minor-guest-f28` |
| amd64 | MCE, Private | `release-4.19-amd64-nightly-metal-ds-hypershift-agent-mce-n3minor-mgmt-f28` |

## Version 4.20 (175 jobs)

### AWS (100 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-aws-ipi-ovn-hypershift-mce-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-aws-ipi-ovn-hypershift-mce-mceupgrade-full-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-aws-ipi-ovn-hypershift-mce-mceupgrade-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-aws-ipi-ovn-hypershift-mce-replace-f28` |
| amd64 | Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-aws-ipi-ovn-hypershift-replace-f28` |
| amd64 | Upgrade, Private | `release-4.20-amd64-nightly-4.20-upgrade-from-stable-4.19-aws-ipi-ovn-hypershift-replace-f14` |
| amd64 | Upgrade, Private | `release-4.20-amd64-nightly-4.20-upgrade-from-stable-4.19-aws-ipi-ovn-hypershift-replace-f7` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-upgrade-from-stable-4.20-aws-ipi-ovn-hypershift-mce-inplace-f60` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-upgrade-from-stable-4.20-aws-ipi-ovn-hypershift-mce-replace-f60` |
| amd64 | Private, Cilium | `release-4.20-amd64-nightly-aws-ipi-cilium-hypershift-guest-f14` |
| amd64 | Private, Cilium | `release-4.20-amd64-nightly-aws-ipi-cilium-hypershift-guest-f7` |
| arm64 | Private, EFS | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f14` |
| arm64 | Private, EFS, Destructive | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f14-destructive` |
| arm64 | Private, EFS | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f7` |
| arm64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f14` |
| arm64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f7` |
| amd64 | FIPS, Private, Destructive | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f28-destructive` |
| amd64 | FIPS, Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-openldap-f14` |
| amd64 | FIPS, Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-fips-mgmt-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-guest-disable-caps-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-guest-dynamic-dns-ondemand-adv-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-guest-dynamic-dns-ondemand-advanced-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-guest-ext-oidc-tp-f14` |
| amd64 | Private, Destructive | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-guest-f14-destructive` |
| amd64 | Private, IPSec | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-guest-ipsec-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-guest-ipv4-k8sconfig-advanced-f14` |
| amd64 | Private, LongDuration | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-guest-longduration-f14` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-mce-n2minor-mgmt-f28` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-global-ps-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-global-ps-f7` |
| amd64 | Private, LongDuration | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-longduration-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-private-guest-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-private-guest-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-private-mgmt-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-private-mgmt-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-guest-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-guest-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-mgmt-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-mgmt-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-advanced-int-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-advanced-int-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-advanced-stage-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-advanced-stage-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-external-auth-int-full-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-external-auth-int-full-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-external-auth-stage-full-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-external-auth-stage-full-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-pl-int-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-pl-int-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-pl-stage-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-pl-stage-f7` |
| amd64 | Private, Proxy | `release-4.20-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f14` |
| amd64 | Private, Proxy | `release-4.20-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f7` |
| amd64 | Private, Proxy | `release-4.20-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f14` |
| amd64 | Private, Proxy | `release-4.20-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-int-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-int-f7` |
| amd64 | Upgrade, Private | `release-4.20-amd64-nightly-aws-rosa-hcp-upgrade-f999` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-zero-egress-int-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-zero-egress-int-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-zero-egress-stage-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-aws-rosa-hcp-zero-egress-stage-f7` |
| amd64 | Private | `release-4.20-amd64-rollback-nightly-aws-ipi-ovn-hypershift-inplace-f28` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-advanced-int-f14` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-advanced-int-f7` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-advanced-stage-f14` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-advanced-stage-f7` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-external-auth-stage-full-f14` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-external-auth-stage-full-f7` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-external-auth-stage-full-int-f14` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-external-auth-stage-full-int-f7` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-pl-int-f14` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-pl-int-f7` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-pl-stage-f14` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-pl-stage-f7` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-sector-advanced-prod-stable-critical-f28` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f14` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f7` |
| amd64 | Private, Proxy | `release-4.20-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f14` |
| amd64 | Private, Proxy | `release-4.20-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f7` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-sector-prod-critical-f14` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-sector-prod-critical-f7` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-f14` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-f7` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-int-f14` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-int-f7` |
| amd64 | Upgrade, Private | `release-4.20-amd64-stable-aws-rosa-hcp-upgrade-f999` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-zero-egress-int-f14` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-zero-egress-int-f7` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-zero-egress-stage-f14` |
| amd64 | Private | `release-4.20-amd64-stable-aws-rosa-hcp-zero-egress-stage-f7` |
| arm64 | Private | `release-4.20-multi-nightly-aws-ipi-ovn-arm-mixarch-mto-hypershift-arm-guest-f14` |
| arm64 | Private | `release-4.20-multi-nightly-aws-ipi-ovn-arm-mixarch-mto-hypershift-arm-mgmt-f14` |

### Agent (BareMetal) (15 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-baremetalds-agent-hypershift-mce-compact-full-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-baremetalds-agent-hypershift-mce-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-baremetalds-agent-hypershift-mce-mceupgrade-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-upgrade-from-stable-4.20-baremetalds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.20-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f14` |
| amd64 | MCE, Disconnected, Private | `release-4.20-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f14-des` |
| amd64 | MCE, Disconnected, Private | `release-4.20-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-mgmt-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.20-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.20-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f14-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.20-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-mgmt-f14` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.20-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f28-destructive` |
| arm64 | MCE, Private | `release-4.20-amd64-nightly-baremetalds-hypershift-agent-mce-lab-arm-mgmt-f28` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-baremetalds-hypershift-agent-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-baremetalds-hypershift-agent-mce-n2minor-mgmt-f28` |

### Azure (27 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | Upgrade, Private | `release-4.20-amd64-nightly-4.20-upgrade-from-stable-4.19-azure-aks-hypershift-byo-vnet-inplace-guest-f28` |
| amd64 | Upgrade, Private | `release-4.20-amd64-nightly-4.20-upgrade-from-stable-4.19-azure-aks-hypershift-byo-vnet-replace-guest-f28` |
| amd64 | Upgrade, Private | `release-4.20-amd64-nightly-4.20-upgrade-from-stable-4.20-azure-aks-hypershift-byo-vnet-replace-guest-f28` |
| arm64 | Private | `release-4.20-amd64-nightly-azure-aks-hypershift-arm-nodepool-guest-f14` |
| arm64 | Private | `release-4.20-amd64-nightly-azure-aks-hypershift-arm-nodepool-guest-f7` |
| amd64 | FIPS, Private | `release-4.20-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f14` |
| amd64 | FIPS, Private, Destructive | `release-4.20-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f14-destructive` |
| amd64 | FIPS, Private, LongDuration | `release-4.20-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f14-longduration` |
| amd64 | FIPS, Private | `release-4.20-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f7` |
| amd64 | FIPS, Private | `release-4.20-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-mgmt-f14` |
| amd64 | Private, Cilium | `release-4.20-amd64-nightly-azure-aks-hypershift-cilium-guest-f14` |
| amd64 | Private, Cilium | `release-4.20-amd64-nightly-azure-aks-hypershift-cilium-guest-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-azure-aks-hypershift-disaster-recovery-infra-guest-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-global-ps-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-global-ps-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-azure-aks-hypershift-etcd-disk-encryption-guest-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-azure-aks-hypershift-etcd-disk-encryption-guest-f7` |
| amd64 | Private | `release-4.20-amd64-nightly-azure-aks-hypershift-ext-oidc-tp-guest-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-azure-aks-hypershift-full-cert-guest-f14` |
| amd64 | Private, LongDuration | `release-4.20-amd64-nightly-azure-aks-hypershift-install-f14-longduration` |
| amd64 | Private | `release-4.20-amd64-nightly-azure-aks-hypershift-registry-overrides-guest-f14` |
| amd64 | Private | `release-4.20-amd64-nightly-azure-aks-hypershift-registry-overrides-guest-f7` |
| amd64 | Private | `release-4.20-amd64-rollback-nightly-azure-aks-hypershift-byo-vnet-replace-guest-f28` |
| multi | Private | `release-4.20-multi-nightly-azure-aks-hypershift-guest-f14` |
| multi | Private | `release-4.20-multi-nightly-azure-aks-hypershift-guest-reversed-f14` |

### KubeVirt (9 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-metal-ds-kubevirt-hypershift-mce-mceupgrade-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-metal-ds-kubevirt-hypershift-mce-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-upgrade-from-stable-4.20-metal-ds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | Private, IPv6/DualStack | `release-4.20-amd64-nightly-metal-ds-ipi-ovn-dualstack-kubevirt-hypershift-f14` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-guest-f14` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-guest-f14-des` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n2minor-mgmt-f28` |

### KubeVirt (BareMetal) (8 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-baremetalds-kubevirt-hypershift-mce-mceupgrade-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-baremetalds-kubevirt-hypershift-mce-replace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-upgrade-from-stable-4.20-baremetalds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | Private, IPv6/DualStack | `release-4.20-amd64-nightly-baremetalds-ipi-ovn-dualstack-kubevirt-hypershift-f14` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f14` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f14-des` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n2minor-mgmt-f28` |

### Other (16 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-metal-ds-agent-hypershift-mce-compact-full-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-metal-ds-agent-hypershift-mce-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-eus-upgrade-from-4.18-metal-ds-agent-hypershift-mce-mceupgrade-inplace-f28` |
| amd64 | MCE, Upgrade, Private | `release-4.20-amd64-nightly-4.20-upgrade-from-stable-4.20-metal-ds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.20-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-guest-f14` |
| amd64 | MCE, Disconnected, Private | `release-4.20-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-guest-f14-des` |
| amd64 | MCE, Disconnected, Private | `release-4.20-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-mgmt-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.20-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-guest-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.20-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-guest-f14-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.20-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-mgmt-f14` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-metal-ds-hypershift-agent-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.20-amd64-nightly-metal-ds-hypershift-agent-mce-guest-f28-destructive` |
| arm64 | MCE, Private | `release-4.20-amd64-nightly-metal-ds-hypershift-agent-mce-lab-arm-mgmt-f28` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-metal-ds-hypershift-agent-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-metal-ds-hypershift-agent-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.20-amd64-nightly-metal-ds-hypershift-agent-mce-n2minor-mgmt-f28` |

## Version 4.21 (173 jobs)

### AWS (97 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | Upgrade, Private | `release-4.21-amd64-nightly-4.21-upgrade-from-stable-4.20-aws-ipi-ovn-hypershift-replace-f14` |
| amd64 | Upgrade, Private | `release-4.21-amd64-nightly-4.21-upgrade-from-stable-4.20-aws-ipi-ovn-hypershift-replace-f7` |
| amd64 | MCE, Upgrade, Private | `release-4.21-amd64-nightly-4.21-upgrade-from-stable-4.21-aws-ipi-ovn-hypershift-mce-inplace-f60` |
| amd64 | MCE, Upgrade, Private | `release-4.21-amd64-nightly-4.21-upgrade-from-stable-4.21-aws-ipi-ovn-hypershift-mce-replace-f60` |
| amd64 | Private, Cilium | `release-4.21-amd64-nightly-aws-ipi-cilium-hypershift-guest-f14` |
| amd64 | Private, Cilium | `release-4.21-amd64-nightly-aws-ipi-cilium-hypershift-guest-f7` |
| arm64 | Private, EFS | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f14` |
| arm64 | Private, EFS, Destructive | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f14-destructive` |
| arm64 | Private, EFS | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f7` |
| arm64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f14` |
| arm64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f7` |
| amd64 | FIPS, Private, Destructive | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f28-destructive` |
| amd64 | FIPS, Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-openldap-f14` |
| amd64 | FIPS, Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-fips-mgmt-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-guest-disable-caps-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-guest-dynamic-dns-ondemand-adv-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-guest-dynamic-dns-ondemand-advanced-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-guest-ext-oidc-tp-f14` |
| amd64 | Private, Destructive | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-guest-f14-destructive` |
| amd64 | Private, IPSec | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-guest-ipsec-f14` |
| amd64 | Private, LongDuration | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-guest-longduration-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-global-ps-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-global-ps-f7` |
| amd64 | Private, LongDuration | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-longduration-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-n1minor-guest-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-n1minor-mgmt-f28` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-n2minor-guest-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-n2minor-mgmt-f28` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-n3minor-guest-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-n3minor-mgmt-f28` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-private-guest-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-private-guest-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-private-mgmt-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-private-mgmt-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-guest-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-guest-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-mgmt-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-mgmt-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-advanced-int-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-advanced-int-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-advanced-stage-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-advanced-stage-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-external-auth-int-full-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-external-auth-int-full-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-external-auth-stage-full-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-external-auth-stage-full-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-pl-int-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-pl-int-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-pl-stage-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-pl-stage-f7` |
| amd64 | Private, Proxy | `release-4.21-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f14` |
| amd64 | Private, Proxy | `release-4.21-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f7` |
| amd64 | Private, Proxy | `release-4.21-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f14` |
| amd64 | Private, Proxy | `release-4.21-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-int-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-int-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-zero-egress-int-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-zero-egress-int-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-zero-egress-stage-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-aws-rosa-hcp-zero-egress-stage-f7` |
| amd64 | Private | `release-4.21-amd64-rollback-nightly-aws-ipi-ovn-hypershift-inplace-f28` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-advanced-int-f14` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-advanced-int-f7` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-advanced-stage-f14` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-advanced-stage-f7` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-external-auth-stage-full-f14` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-external-auth-stage-full-f7` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-external-auth-stage-full-int-f14` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-external-auth-stage-full-int-f7` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-pl-int-f14` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-pl-int-f7` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-pl-stage-f14` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-pl-stage-f7` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-sector-advanced-prod-stable-critical-f28` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f14` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f7` |
| amd64 | Private, Proxy | `release-4.21-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f14` |
| amd64 | Private, Proxy | `release-4.21-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f7` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-sector-prod-critical-f14` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-sector-prod-critical-f7` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-f14` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-f7` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-int-f14` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-int-f7` |
| amd64 | Upgrade, Private | `release-4.21-amd64-stable-aws-rosa-hcp-upgrade-f999` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-zero-egress-int-f14` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-zero-egress-int-f7` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-zero-egress-stage-f14` |
| amd64 | Private | `release-4.21-amd64-stable-aws-rosa-hcp-zero-egress-stage-f7` |
| arm64 | Private | `release-4.21-multi-nightly-aws-ipi-ovn-arm-mixarch-mto-hypershift-arm-guest-f14` |
| arm64 | Private | `release-4.21-multi-nightly-aws-ipi-ovn-arm-mixarch-mto-hypershift-arm-mgmt-f14` |

### Agent (BareMetal) (10 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.21-amd64-nightly-4.21-upgrade-from-stable-4.21-baremetalds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.21-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f14` |
| amd64 | MCE, Disconnected, Private | `release-4.21-amd64-nightly-baremetalds-hypershift-agent-mce-disconnected-guest-f14-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.21-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.21-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-guest-f14-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.21-amd64-nightly-baremetalds-hypershift-agent-mce-dualstack-mgmt-f14` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.21-amd64-nightly-baremetalds-hypershift-agent-mce-guest-f28-destructive` |
| arm64 | MCE, Private | `release-4.21-amd64-nightly-baremetalds-hypershift-agent-mce-lab-arm-mgmt-f28` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-baremetalds-hypershift-agent-mce-mgmt-f14` |

### Azure (34 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | Upgrade, Private | `release-4.21-amd64-nightly-4.21-upgrade-from-stable-4.20-azure-aks-hypershift-byo-vnet-inplace-guest-f28` |
| amd64 | Upgrade, Private | `release-4.21-amd64-nightly-4.21-upgrade-from-stable-4.20-azure-aks-hypershift-byo-vnet-replace-guest-f28` |
| amd64 | Upgrade, Private | `release-4.21-amd64-nightly-4.21-upgrade-from-stable-4.20-azure-aks-hypershift-etcd-disk-encryption-replace-guest-f28` |
| amd64 | Upgrade, Private | `release-4.21-amd64-nightly-4.21-upgrade-from-stable-4.20-azure-aks-hypershift-registry-overrides-replace-guest-f28` |
| amd64 | Upgrade, Private | `release-4.21-amd64-nightly-4.21-upgrade-from-stable-4.21-azure-aks-hypershift-byo-vnet-replace-guest-f28` |
| arm64 | Private | `release-4.21-amd64-nightly-azure-aks-hypershift-arm-nodepool-guest-f7` |
| amd64 | FIPS, Private | `release-4.21-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f14` |
| amd64 | FIPS, Private, Destructive | `release-4.21-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f14-destructive` |
| amd64 | FIPS, Private, LongDuration | `release-4.21-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f14-longduration` |
| amd64 | FIPS, Private | `release-4.21-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f7` |
| amd64 | FIPS, Private | `release-4.21-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-mgmt-f14` |
| amd64 | Private, Cilium | `release-4.21-amd64-nightly-azure-aks-hypershift-cilium-guest-f14` |
| amd64 | Private, Cilium | `release-4.21-amd64-nightly-azure-aks-hypershift-cilium-guest-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-aks-hypershift-disaster-recovery-infra-guest-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-global-ps-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-global-ps-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-aks-hypershift-etcd-disk-encryption-guest-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-aks-hypershift-ext-oidc-tp-guest-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-aks-hypershift-full-cert-guest-f14` |
| amd64 | Private, LongDuration | `release-4.21-amd64-nightly-azure-aks-hypershift-install-f14-longduration` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-ipi-ovn-hypershift-guest-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-ipi-ovn-hypershift-guest-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-ipi-ovn-hypershift-guest-n1minor-cli-f28` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-ipi-ovn-hypershift-guest-n2minor-cli-f28` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-ipi-ovn-hypershift-guest-n3minor-cli-f28` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-ipi-ovn-hypershift-image-generation-guest-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-ipi-ovn-hypershift-mgmt-f14` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-ipi-ovn-hypershift-mgmt-f7` |
| amd64 | Private | `release-4.21-amd64-nightly-azure-ipi-ovn-hypershift-no-marketplace-guest-f14` |
| amd64 | Private | `release-4.21-amd64-rollback-nightly-azure-aks-hypershift-byo-vnet-replace-guest-f28` |
| multi | Private | `release-4.21-multi-nightly-azure-aks-hypershift-guest-f14` |
| multi | Private | `release-4.21-multi-nightly-azure-aks-hypershift-guest-reversed-f14` |

### KubeVirt (9 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.21-amd64-nightly-4.21-upgrade-from-stable-4.21-metal-ds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | Private, IPv6/DualStack | `release-4.21-amd64-nightly-metal-ds-ipi-ovn-dualstack-kubevirt-hypershift-f14` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-guest-f14` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-guest-f14-des` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n1minor-guest-f28` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n1minor-mgmt-f28` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-ipi-ovn-kubevirt-hypershift-mce-n2minor-mgmt-f28` |

### KubeVirt (BareMetal) (8 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.21-amd64-nightly-4.21-upgrade-from-stable-4.21-baremetalds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | Private, IPv6/DualStack | `release-4.21-amd64-nightly-baremetalds-ipi-ovn-dualstack-kubevirt-hypershift-f14` |
| amd64 | Private, IPv6/DualStack | `release-4.21-amd64-nightly-baremetalds-ipi-ovn-dualstack-kubevirt-hypershift-f7` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f14` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-guest-f14-des` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n1minor-mgmt-f28` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-baremetalds-ipi-ovn-kubevirt-hypershift-mce-n2minor-guest-f28` |

### Other (15 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.21-amd64-nightly-4.21-upgrade-from-stable-4.21-metal-ds-agent-hypershift-mce-inplace-f60` |
| amd64 | MCE, Disconnected, Private | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-guest-f14` |
| amd64 | MCE, Disconnected, Private | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-guest-f14-des` |
| amd64 | MCE, Disconnected, Private | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-disconnected-mgmt-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-guest-f14` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-guest-f14-des` |
| amd64 | MCE, Private, IPv6/DualStack | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-dualstack-mgmt-f14` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-guest-f14` |
| amd64 | MCE, Private, Destructive | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-guest-f28-destructive` |
| arm64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-lab-arm-mgmt-f28` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-mgmt-f14` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-n1minor-guest-f28` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-n1minor-mgmt-f28` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-n2minor-guest-f28` |
| amd64 | MCE, Private | `release-4.21-amd64-nightly-metal-ds-hypershift-agent-mce-n2minor-mgmt-f28` |

## Version 4.22 (95 jobs)

### AWS (59 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | Upgrade, Private | `release-4.22-amd64-nightly-4.22-upgrade-from-stable-4.21-aws-ipi-ovn-hypershift-replace-f7` |
| amd64 | MCE, Upgrade, Private | `release-4.22-amd64-nightly-4.22-upgrade-from-stable-4.22-aws-ipi-ovn-hypershift-mce-inplace-f60` |
| amd64 | MCE, Upgrade, Private | `release-4.22-amd64-nightly-4.22-upgrade-from-stable-4.22-aws-ipi-ovn-hypershift-mce-replace-f60` |
| amd64 | Private, Cilium | `release-4.22-amd64-nightly-aws-ipi-cilium-hypershift-guest-f7` |
| arm64 | Private, EFS, Destructive | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f14-destructive` |
| arm64 | Private, EFS | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f7` |
| arm64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f7` |
| amd64 | FIPS, Private, Destructive | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f28-destructive` |
| amd64 | FIPS, Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-openldap-f14` |
| amd64 | FIPS, Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-fips-mgmt-f14` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-guest-disable-caps-f14` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-guest-dynamic-dns-ondemand-advanced-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-guest-ext-oidc-tp-f14` |
| amd64 | Private, Destructive | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-guest-f14-destructive` |
| amd64 | Private, IPSec | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-guest-ipsec-f14` |
| amd64 | Private, LongDuration | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-guest-longduration-f14` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-global-ps-f7` |
| amd64 | Private, LongDuration | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-longduration-f14` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-n1minor-guest-f14` |
| amd64 | Private | `release-4.22-amd64-nightly-    ` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-n2minor-guest-f14` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-n2minor-mgmt-f28` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-n3minor-guest-f14` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-n3minor-mgmt-f28` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-private-guest-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-private-mgmt-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-guest-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-mgmt-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-rosa-hcp-advanced-int-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-rosa-hcp-advanced-stage-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-rosa-hcp-external-auth-int-full-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-rosa-hcp-external-auth-stage-full-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-rosa-hcp-pl-int-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-rosa-hcp-pl-stage-f7` |
| amd64 | Private, Proxy | `release-4.22-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f7` |
| amd64 | Private, Proxy | `release-4.22-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-int-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-rosa-hcp-zero-egress-int-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-aws-rosa-hcp-zero-egress-stage-f7` |
| amd64 | Private | `release-4.22-amd64-rollback-nightly-aws-ipi-ovn-hypershift-inplace-f28` |
| amd64 | Private | `release-4.22-amd64-stable-aws-rosa-hcp-advanced-int-f7` |
| amd64 | Private | `release-4.22-amd64-stable-aws-rosa-hcp-advanced-stage-f7` |
| amd64 | Private | `release-4.22-amd64-stable-aws-rosa-hcp-external-auth-stage-full-f7` |
| amd64 | Private | `release-4.22-amd64-stable-aws-rosa-hcp-external-auth-stage-full-int-f7` |
| amd64 | Private | `release-4.22-amd64-stable-aws-rosa-hcp-pl-int-f7` |
| amd64 | Private | `release-4.22-amd64-stable-aws-rosa-hcp-pl-stage-f7` |
| amd64 | Private | `release-4.22-amd64-stable-aws-rosa-hcp-sector-advanced-prod-stable-critical-f28` |
| amd64 | Private | `release-4.22-amd64-stable-aws-rosa-hcp-sector-byo-kms-oidc-auditlog-prod-critical-f7` |
| amd64 | Private, Proxy | `release-4.22-amd64-stable-aws-rosa-hcp-sector-private-proxy-prod-critical-f7` |
| amd64 | Private | `release-4.22-amd64-stable-aws-rosa-hcp-sector-prod-critical-f7` |
| amd64 | Private | `release-4.22-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-f7` |
| amd64 | Private | `release-4.22-amd64-stable-aws-rosa-hcp-shared-vpc-advanced-int-f7` |
| amd64 | Private | `release-4.22-amd64-stable-aws-rosa-hcp-zero-egress-int-f7` |
| amd64 | Private | `release-4.22-amd64-stable-aws-rosa-hcp-zero-egress-stage-f7` |
| arm64 | Private | `release-4.22-multi-nightly-aws-ipi-ovn-arm-mixarch-mto-hypershift-arm-guest-f14` |
| arm64 | Private | `release-4.22-multi-nightly-aws-ipi-ovn-arm-mixarch-mto-hypershift-arm-mgmt-f14` |

### Agent (BareMetal) (1 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.22-amd64-nightly-4.22-upgrade-from-stable-4.22-baremetalds-agent-hypershift-mce-inplace-f60` |

### Azure (30 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | Upgrade, Private | `release-4.22-amd64-nightly-4.22-upgrade-from-stable-4.21-azure-aks-hypershift-byo-vnet-inplace-guest-f28` |
| amd64 | Upgrade, Private | `release-4.22-amd64-nightly-4.22-upgrade-from-stable-4.21-azure-aks-hypershift-byo-vnet-replace-guest-f28` |
| amd64 | Upgrade, Private | `release-4.22-amd64-nightly-4.22-upgrade-from-stable-4.21-azure-aks-hypershift-etcd-disk-encryption-replace-guest-f28` |
| amd64 | Upgrade, Private | `release-4.22-amd64-nightly-4.22-upgrade-from-stable-4.22-azure-aks-hypershift-byo-vnet-replace-guest-f28` |
| arm64 | Private | `release-4.22-amd64-nightly-azure-aks-hypershift-arm-nodepool-guest-f7` |
| amd64 | FIPS, Private, Destructive | `release-4.22-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f14-destructive` |
| amd64 | FIPS, Private, LongDuration | `release-4.22-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f14-longduration` |
| amd64 | FIPS, Private | `release-4.22-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-guest-f7` |
| amd64 | FIPS, Private | `release-4.22-amd64-nightly-azure-aks-hypershift-byo-vnet-fips-mgmt-f14` |
| amd64 | Private, Cilium | `release-4.22-amd64-nightly-azure-aks-hypershift-cilium-guest-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-aks-hypershift-disaster-recovery-infra-guest-f14` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-aks-hypershift-ephemeral-creds-guest-global-ps-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-aks-hypershift-etcd-disk-encryption-guest-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-aks-hypershift-ext-oidc-tp-guest-f14` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-aks-hypershift-full-cert-guest-f14` |
| amd64 | Private, LongDuration | `release-4.22-amd64-nightly-azure-aks-hypershift-install-f14-longduration` |
| arm64 | Private | `release-4.22-amd64-nightly-azure-ipi-ovn-hypershift-arm-nodepool-guest-f7` |
| arm64 | Private | `release-4.22-amd64-nightly-azure-ipi-ovn-hypershift-arm-nodepool-mgmt-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-ipi-ovn-hypershift-guest-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-ipi-ovn-hypershift-guest-n1minor-cli-f28` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-ipi-ovn-hypershift-guest-n2minor-cli-f28` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-ipi-ovn-hypershift-guest-n3minor-cli-f28` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-ipi-ovn-hypershift-image-generation-guest-f14` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-ipi-ovn-hypershift-mgmt-f7` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-ipi-ovn-hypershift-no-marketplace-guest-f14` |
| amd64 | Private | `release-4.22-amd64-nightly-azure-ipi-ovn-hypershift-productcli-f7` |
| amd64 | Private | `release-4.22-amd64-rollback-nightly-azure-aks-hypershift-byo-vnet-replace-guest-f28` |
| multi | Private | `release-4.22-multi-nightly-azure-aks-hypershift-guest-f14` |
| multi | Private | `release-4.22-multi-nightly-azure-aks-hypershift-guest-reversed-f14` |

### KubeVirt (2 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.22-amd64-nightly-4.22-upgrade-from-stable-4.22-metal-ds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | Private, IPv6/DualStack | `release-4.22-amd64-nightly-metal-ds-ipi-ovn-dualstack-kubevirt-hypershift-f7` |

### KubeVirt (BareMetal) (2 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.22-amd64-nightly-4.22-upgrade-from-stable-4.22-baremetalds-kubevirt-hypershift-mce-replace-f60` |
| amd64 | Private, IPv6/DualStack | `release-4.22-amd64-nightly-baremetalds-ipi-ovn-dualstack-kubevirt-hypershift-f7` |

### Other (1 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | MCE, Upgrade, Private | `release-4.22-amd64-nightly-4.22-upgrade-from-stable-4.22-metal-ds-agent-hypershift-mce-inplace-f60` |

## Version 4.23 (2 jobs)

### AWS (2 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | Private | `release-4.23-amd64-nightly-aws-ipi-ovn-hypershift-guest-disable-caps-f14` |
| amd64 | Private, Proxy | `release-4.23-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f7` |

## Version 5.0 (49 jobs)

### AWS (41 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | Private, Cilium | `release-5.0-amd64-nightly-aws-ipi-cilium-hypershift-guest-f7` |
| arm64 | Private, EFS, Destructive | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f14-destructive` |
| arm64 | Private, EFS | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-guest-efs-f7` |
| arm64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-arm-nodepool-mgmt-f7` |
| amd64 | FIPS, Private, Destructive | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-f28-destructive` |
| amd64 | FIPS, Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-fips-guest-openldap-f14` |
| amd64 | FIPS, Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-fips-mgmt-f14` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-guest-disable-caps-f14` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-guest-dynamic-dns-ondemand-advanced-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-guest-ext-oidc-tp-f14` |
| amd64 | Private, Destructive | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-guest-f14-destructive` |
| amd64 | Private, IPSec | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-guest-ipsec-f14` |
| amd64 | Private, LongDuration | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-guest-longduration-f14` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-critical-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-global-ps-f7` |
| amd64 | Private, LongDuration | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-mgmt-longduration-f14` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-n1minor-guest-f14` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-n1minor-mgmt-f28` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-n2minor-guest-f14` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-n2minor-mgmt-f28` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-n3minor-guest-f14` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-n3minor-mgmt-f28` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-private-guest-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-private-mgmt-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-guest-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-ipi-ovn-hypershift-shared-vpc-mgmt-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-rosa-hcp-advanced-int-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-rosa-hcp-advanced-stage-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-rosa-hcp-external-auth-int-full-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-rosa-hcp-external-auth-stage-full-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-rosa-hcp-pl-int-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-rosa-hcp-pl-stage-f7` |
| amd64 | Private, Proxy | `release-5.0-amd64-nightly-aws-rosa-hcp-private-proxy-int-full-f7` |
| amd64 | Private, Proxy | `release-5.0-amd64-nightly-aws-rosa-hcp-private-proxy-stage-full-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-rosa-hcp-shared-vpc-advanced-int-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-rosa-hcp-zero-egress-int-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-aws-rosa-hcp-zero-egress-stage-f7` |
| arm64 | Private | `release-5.0-multi-nightly-aws-ipi-ovn-arm-mixarch-mto-hypershift-arm-guest-f14` |
| arm64 | Private | `release-5.0-multi-nightly-aws-ipi-ovn-arm-mixarch-mto-hypershift-arm-mgmt-f14` |

### Azure (8 jobs)

| Arch | Features | Job Name |
|---|---|---|
| amd64 | Private, LongDuration | `release-5.0-amd64-nightly-azure-aks-hypershift-install-f14-longduration` |
| amd64 | Private | `release-5.0-amd64-nightly-azure-ipi-ovn-hypershift-guest-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-azure-ipi-ovn-hypershift-guest-n1minor-cli-f28` |
| amd64 | Private | `release-5.0-amd64-nightly-azure-ipi-ovn-hypershift-guest-n2minor-cli-f28` |
| amd64 | Private | `release-5.0-amd64-nightly-azure-ipi-ovn-hypershift-guest-n3minor-cli-f28` |
| amd64 | Private | `release-5.0-amd64-nightly-azure-ipi-ovn-hypershift-image-generation-guest-f14` |
| amd64 | Private | `release-5.0-amd64-nightly-azure-ipi-ovn-hypershift-mgmt-f7` |
| amd64 | Private | `release-5.0-amd64-nightly-azure-ipi-ovn-hypershift-no-marketplace-guest-f14` |
