# DevOps Foundations and Repository Governance

## Mandatory Rules

- **DO-001** — Delivery ownership is shared across product, engineering, security, quality, and operations; handoffs must not eliminate accountability.
- **DO-002** — Repetitive delivery and operational activities must be automated when automation reduces risk and remains maintainable.
- **DO-003** — Production changes must be traceable to an approved requirement, defect, risk treatment, or operational task.
- **DO-004** — Every repository must have an accountable owner, support contact, classification, lifecycle status, and documented purpose.
- **DO-005** — Source code, pipeline definitions, infrastructure definitions, operational scripts, and configuration templates must be version-controlled.
- **DO-006** — Default branches must be protected against unauthorized direct changes.
- **DO-007** — Material changes must use pull requests and independent review appropriate to risk.
- **DO-008** — Branching strategy must be documented, simple, and compatible with frequent integration.
- **DO-009** — Long-lived branches must be avoided unless their ownership, merge policy, and retirement criteria are explicit.
- **DO-010** — Commit history must identify the intent of change and must not contain secrets or sensitive operational data.
- **DO-011** — Commits should be cohesive, reviewable, and small enough to support diagnosis and rollback.
- **DO-012** — Pull requests must describe purpose, risk, testing, deployment impact, migration needs, and rollback considerations.
- **DO-013** — High-risk changes require reviewers with relevant security, architecture, database, or platform competence.
- **DO-014** — Required status checks must complete successfully before merge unless a formally recorded exception exists.
- **DO-015** — Force pushes and history rewrites on protected or release branches must be prohibited.
- **DO-016** — Repository access must follow least privilege and be reviewed periodically.
- **DO-017** — Dormant repositories must be archived, marked read-only, and assigned retention or disposal treatment.
- **DO-018** — Generated code and AI-assisted changes are subject to the same ownership, review, testing, and security requirements as human-written changes.

## Evidence

- Repository ownership record
- Branch-protection configuration
- Review and status-check policy
- Access-review evidence
- Repository lifecycle inventory