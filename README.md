# UTM_NIST_800-171_Audit
# NIST 800-171 Audit: Virtual Sandbox (UTM)
## Objective

To perform high-risk security testing and execute "destructive" remediation scripts within an isolated, non-
production environment to prevent local hardware instability.

## Setup
* **Virtualization:** Apple Virtualization Framework via UTM.
* **OS:** macOS 15.x (Sequoia).
* **Resource Allocation:** 8GB RAM / 4 CPU Cores / 64GB Storage.
## Audit Steps
1. **Infrastructure:** Virtualized macOS Sequoia to establish an isolated testing node.
2. **Framework Setup:** Cloned the macOS Security Compliance Project (mSCP) and checked out the
`sequoia` branch.
3. **Baseline Generation:** Generated a NIST 800-171 technical baseline YAML.
4. **Execution:** Ran `800-171_compliance.sh` to identify failure points without risking host hardware.
## Findings
* **Initial Score:** 38.26%
* **Outcome:** Successfully identi!ed 92 control failures in a "safe-to-fail" environment. Validated that
remediation scripts do not cause kernel panics on Sequoia.
