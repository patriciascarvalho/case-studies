# Control Mapping Matrix — IAM Governance Normatives

**Companion artifact to:** *Closing the Governance Gap: Rebuilding IAM Policy for Human and Non-Human Access in Public Cloud*

This matrix maps each internal normative control to the market framework(s) it is grounded in, making the governance standard auditable and traceable rather than only narrative. Control IDs use a generic naming convention (`IAM-NORM-##`) so the matrix can be reused or adapted across organizations.

| Control ID | Internal Control Area | Control Objective | Identity Scope | Framework Reference(s) |
|---|---|---|---|---|
| IAM-NORM-01 | Identity provisioning | Every identity (human or non-human) must be provisioned through an approved, auditable request process — no standing or pre-created accounts outside that process. | Human + NHI | NIST SP 800-53; ISO/IEC 27001 |
| IAM-NORM-02 | Least privilege | Access granted must be the minimum required for the identity's role or task, validated at provisioning and on every material change. | Human + NHI | NIST SP 800-53; NIST SP 800-207; CIS Controls |
| IAM-NORM-03 | Non-human identity lifecycle | Service accounts, API keys, and workload identities follow a defined lifecycle distinct from human accounts: ownership assignment, credential rotation interval, scope boundary, and deprovisioning trigger. | NHI | CSA CCM; NIST SP 800-53 |
| IAM-NORM-04 | Credential rotation | Non-human credentials (API keys, secrets, service account keys) are rotated on a defined interval or upon a triggering event (role change, suspected exposure). | NHI | CSA CCM; NIST SP 800-63 |
| IAM-NORM-05 | On-prem-to-cloud boundary accountability | A named owner is accountable for any identity or trust relationship that crosses from on-premises directories into public cloud IAM systems. | Human + NHI | ISO/IEC 27001; CSA CCM |
| IAM-NORM-06 | Continuous verification | Access is re-validated based on context (identity, device, environment) rather than granted once and trusted indefinitely. | Human + NHI | NIST SP 800-207 |
| IAM-NORM-07 | Access certification / recertification | Access entitlements are reviewed on a defined cadence by a named approver; unreviewed or unowned access is treated as a finding. | Human + NHI | ISO/IEC 27001; CIS Controls |
| IAM-NORM-08 | Segregation of duties | No single identity holds conflicting privileges (e.g., request and approve the same access) across critical systems. | Human | ISO/IEC 27001; NIST SP 800-53 |
| IAM-NORM-09 | Digital identity assurance | Authentication strength (assurance level) is matched to the sensitivity of the resource being accessed. | Human | NIST SP 800-63 |
| IAM-NORM-10 | Audit logging and traceability | Every access event and identity lifecycle action (provisioning, modification, deprovisioning) is logged and attributable to a named owner. | Human + NHI | NIST SP 800-53; ISO/IEC 27001 |
| IAM-NORM-11 | Cloud configuration and secrets management | Secrets and credentials for cloud-native identities are stored and rotated through an approved vault/secrets manager, never embedded in code or configuration. | NHI | CSA CCM; CIS Controls |
| IAM-NORM-12 | Ownership assignment | Every identity — human or non-human — has a single named, accountable owner at all times. "No owner assigned" is treated as a governance finding, not an administrative gap. | Human + NHI | ISO/IEC 27001; CSA CCM |

## How to use this matrix

- **For audits:** each control row can be traced back to its originating framework, supporting audit evidence requests without re-deriving the mapping each time.
- **For adaptation:** the identity scope column flags which controls apply to human accounts, non-human identities, or both — useful when scoping a review or a new normative.
- **For extension:** as new identity types are brought into governed scope (e.g., agentic AI identities), add rows following the same ID convention rather than overwriting existing controls.

---
*This matrix is a sanitized, organization-agnostic template illustrating how internal IAM normatives can be mapped to recognized market frameworks (NIST SP 800-53, NIST SP 800-63, NIST SP 800-207, ISO/IEC 27001, CSA CCM, CIS Controls). Framework editions and clause numbers change over time — verify the current text of each standard before citing specific clauses. Control IDs and specific thresholds should be adapted to each organization's environment.*
