# Closing the Governance Gap: Rebuilding IAM Policy for Human and Non-Human Access in Public Cloud

## The Problem

Cloud adoption consistently outpaces identity governance. Normative frameworks written for on-premises realities are frequently silent on non-human identity (NHI) lifecycle, on the on-premises-to-cloud trust boundary, and on accountability when identities cross that boundary. This case study describes an approach to closing that gap in a hybrid, multi-cloud environment (Azure, GCP, IBM).

In organizations facing this challenge, existing policies are typically fragmented across legacy documentation, written for an on-premises-only reality, and silent on key questions that modern cloud adoption demands:

- How should access be granted, reviewed, and revoked for **human accounts** operating across hybrid on-prem/cloud boundaries?
- How should **non-human identities (NHIs)** — service accounts, API keys, workload identities, automation credentials — be provisioned, scoped, and monitored?
- Who owns accountability when an identity crosses from an on-premises directory into a public cloud IAM system?
- What baseline controls (least privilege, segregation of duties, periodic recertification) actually applied to cloud-native identity types?

In short: the business was moving to the cloud faster than governance was defining the rules for who — and what — could access it. This is a common and often underestimated risk: without clear, current, and enforceable normatives, identity governance becomes reactive, inconsistent across teams, and difficult to audit.

## Methodology

The work was structured as a governance-first initiative, not a purely technical one — because policy gaps require policy solutions before they require tooling.

**1. Current-state assessment**
Mapped the existing internal normatives against the actual identity landscape in use, identifying what was outdated, ambiguous, missing entirely, or inconsistent between on-premises and cloud contexts.

**2. Benchmarking against market reference frameworks**
Rather than drafting policy in isolation, the new normatives were built on established industry frameworks, including:
- **NIST SP 800-53 / NIST SP 800-63** — access control and digital identity guidelines
- **NIST SP 800-207 (Zero Trust Architecture)** — principles for continuous verification and least-privilege access across hybrid environments
- **CIS Controls** — baseline configuration and access management benchmarks
- **Cloud Security Alliance (CSA) Cloud Controls Matrix (CCM)** — cloud-specific control objectives
- **ISO/IEC 27001** — information security management system alignment

This ensured the resulting policy would not just close internal gaps, but hold up against recognized industry and regulatory expectations.

**3. Differentiated policy design for human and non-human identities**
A key methodological decision was to stop treating NHIs as an afterthought to human IAM policy. Separate, explicit lifecycle rules were defined for machine identities: provisioning criteria, ownership assignment, credential rotation, scope boundaries, and deprovisioning triggers — distinct from the human account lifecycle, which follows role-based, HR-linked triggers.

**4. Hybrid environment mapping**
Because identities move between on-premises directories and public cloud IAM systems, the normatives explicitly addressed the integration points: how trust is established, how access provisioned on-prem is translated (or must be re-evaluated) in cloud, and who is accountable at each handoff.

**5. Stakeholder validation**
Draft normatives were reviewed against real operational scenarios and refined for enforceability — a policy that cannot realistically be followed or audited is not a solution.

## What Was Resolved

- Replaced outdated, incomplete internal policy with a current, framework-aligned normative structure covering both human and non-human identity access in public cloud.
- Established explicit, differentiated governance rules for **non-human identities** — closing a gap that previously left service accounts and machine credentials governed by ambiguous or borrowed human-account policy.
- Defined clear accountability and control requirements at the **on-premises-to-cloud integration boundary**, an area previously left to informal or ad hoc handling.
- Aligned internal governance language and control objectives with recognized frameworks (NIST, CSA CCM, ISO 27001, CIS Controls), giving the organization defensible, auditable documentation.

## Business Impact

- **Audit readiness:** Current, framework-aligned documentation replaces outdated policy that could not withstand internal or external audit scrutiny.
- **Scope of the normative rebuild:** 2 internal normatives reviewed, consolidated, or newly created to close the gap.
- **Non-human identities brought into governed scope:** service accounts, API keys, workload identities, managed identities, and CI/CD pipeline credentials, among others — approximately 8 NHI types/categories previously governed by ambiguous or borrowed human-account policy.
- **Reach across the environment:** normatives applied across 3 public cloud platforms and adopted by 6 teams/business areas previously operating under inconsistent, team-by-team interpretation of access rules.
- **Reduced identity risk:** explicit lifecycle and least-privilege rules for NHIs close a blind spot that is increasingly exploited as automation and cloud adoption scale.
- **Foundation for scale:** as cloud and automation initiatives continue to expand, the governance foundation is now in place to extend rather than rebuild from scratch.

---

*This case study reflects a governance and IAM policy framework designed to address identity governance gaps in hybrid on-premises and public cloud environments (Azure, GCP, IBM), covering both human and non-human identity access.*

