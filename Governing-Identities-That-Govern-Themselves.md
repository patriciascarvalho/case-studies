# Governing the Identities That Govern Themselves: A Framework for Agentic AI Identity Security

## The Problem

Agentic AI adoption was accelerating faster than the identity governance model built to control it. Agents were being provisioned to execute tasks, call APIs, and — increasingly — trigger other agents as part of multi-step workflows. Each of those interactions created a new identity relationship, often without a human in the loop and without any policy that had anticipated it.

Traditional IAM and IGA frameworks were not designed for this. They assume identities that are provisioned once, mapped to a stable role, and reviewed on a periodic cycle. Agentic AI breaks each of those assumptions:

- **Access control** could not rely on static, role-based models. An agent's appropriate scope of access depends on the task it is executing at that moment, not a fixed role assigned at provisioning.
- **Risk management** models built around static identity attributes failed to capture the real exposure: what an agent could reach, what it could trigger, and how far a compromised or misbehaving agent could propagate before detection.
- **Lifecycle management** had no clear anchor. Human lifecycles map to predictable events — hiring, role change, termination. Agent lifecycles don't: a single agent might exist for seconds to complete one workflow, or persist for months without ever passing through a formal access review.

Left unaddressed, this creates a governance blind spot at the exact point where most enterprise AI investment is now concentrated.

## Methodology

The approach treated agentic AI identity governance as its own discipline — not an extension of existing NHI or human IAM policy — while still anchoring it to established, auditable frameworks.

**1. Gap analysis against existing NHI and IAM governance**
Assessed where current non-human identity policy could extend to agentic AI and, more importantly, where it could not — particularly around dynamic identity creation and agent-to-agent delegation.

**2. Framework alignment**
Grounded the standard in principles already trusted across the industry, rather than building from scratch:
- **NIST SP 800-207 (Zero Trust Architecture)** — continuous verification and least privilege, applied to agent-to-agent interactions, not just human-to-system access
- **NIST SP 800-53 / 800-63** — access control and identity assurance baselines
- **CSA Cloud Controls Matrix** — cloud-native control objectives for dynamic, ephemeral identities
- **ISO/IEC 27001** — information security management alignment

**3. Scoped, task-level identity design**
Defined that every agent receives its own identity — never a shared or inherited credential — scoped to the specific task and environment (production vs. development), with access that expires by default rather than persisting indefinitely.

**4. Delegation and chain-of-trust rules**
Established explicit rules for what happens when one agent triggers another: whether it inherits permissions, must request new ones, or is restricted to operating strictly within its own granted scope. This closed the most significant gap in the prior model — delegation chains that previously created access with no review and no owner.

**5. Ownership and accountability**
Required a named, accountable owner for every agent identity and every permission review. "No owner assigned" was redefined as a critical finding, not an administrative gap to resolve later.

**6. Behavior- and risk-based monitoring**
Extended risk management beyond static identity attributes to account for behavior and blast radius — what an agent could reach and propagate to, not just what role it held.

## What Was Resolved

- A governance standard for agentic AI identities covering access control, risk management, and lifecycle management — distinct from, but consistent with, existing human and NHI governance.
- Scoped, time-bound identity as the default for every agent, replacing shared credentials and open-ended access.
- Explicit rules governing agent-to-agent delegation, closing a chain-of-trust gap that previously existed with no policy coverage at all.
- Named ownership and full action attribution for every agent identity, enabling real accountability and auditability.
- Risk assessment criteria that account for agent behavior and potential blast radius, not just static role or classification.

## Business Impact

- **Closed a real, active blind spot:** agent-to-agent delegation — previously ungoverned — now has explicit ownership and control.
- **Scope defined by design:** the standard was scoped to cover 5 distinct agentic AI workflows/use cases and 4 agent identity types (task-scoped, persistent, orchestrator/sub-agent, etc.).
- **Delegation chains mapped by design:** 4 agent-to-agent delegation patterns identified and mapped to explicit inheritance/scoping rules, closing a chain-of-trust gap that previously had zero policy coverage.
- **Ownership as a design requirement:** the framework mandates a named, accountable owner for every agent identity in scope, with a target of 100% ownership coverage as adoption rolls out — replacing a previously undefined baseline.
- **Audit-ready governance for a fast-moving area:** documentation and control objectives aligned to NIST, CSA CCM, and ISO/IEC 27001 provide a defensible position as regulatory attention on AI governance increases.
- **Reduced exposure from autonomous processes:** default-expiring, task-scoped access limits how much an agent can accumulate or retain beyond what a workflow actually requires.
- **A framework built to scale, not to be rebuilt:** because the standard was designed as its own governance discipline from the start, it extends as agentic AI adoption grows, rather than requiring a rework each time the environment changes.
- **Positions security as an enabler of AI adoption**, not a constraint discovered after the fact — allowing organizations to move forward on agentic AI initiatives with a governance foundation already in place.

---

*This case study reflects a governance framework designed for cloud identity governance and Non-Human Identity (NHI) programs, focused on agentic AI ecosystems and Zero Trust principles.*
