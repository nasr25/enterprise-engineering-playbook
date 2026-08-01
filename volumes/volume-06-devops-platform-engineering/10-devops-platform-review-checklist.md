# DevOps and Platform Review Checklist

## Review Areas

### Governance and Source Control
- Ownership, support, classification, lifecycle, access, branch protection, review, and status checks are defined.
- Pipeline, infrastructure, configuration, scripts, and runbooks are version-controlled.

### CI/CD and Releases
- Builds are reproducible and artifacts are immutable, traceable, scanned, and promoted without rebuilding.
- Approvals, deployment controls, validation, rollback, and emergency change processes are evidenced.

### Environments and Secrets
- Environment separation, configuration validation, secret storage, certificate renewal, and drift detection are implemented.

### Infrastructure and Runtime
- IaC plans, state protection, policy checks, container hardening, RBAC, network controls, storage, and ingress are reviewed.

### Supply Chain and Security
- SBOM, provenance, signatures, vulnerability gates, runner isolation, dependency controls, and patch ownership are present.

### Reliability and Operations
- Telemetry, SLOs, alerts, on-call, incident response, backups, restore, DR, capacity, lifecycle, and decommissioning are ready.

## Mandatory Rules

- **DO-163** — Production readiness reviews must include application, platform, security, quality, data, and operational owners as appropriate to risk.
- **DO-164** — Review evidence must reflect the actual target environment and release, not only generic templates.
- **DO-165** — Critical delivery and recovery paths must be demonstrated or tested before production approval.
- **DO-166** — Unresolved critical or high-risk findings must block production unless accepted by authorized risk ownership.
- **DO-167** — Conditions of approval must be measurable, owned, dated, and tracked to closure.
- **DO-168** — Required operational documentation must identify owners, dependencies, commands, validation, rollback, and escalation.
- **DO-169** — Reviewers must verify that deployment identities and runtime identities are distinct and least-privileged.
- **DO-170** — Reviewers must verify artifact immutability and source-to-production traceability.
- **DO-171** — Reviewers must verify that secrets cannot be exposed through repositories, pipelines, images, logs, or support procedures.
- **DO-172** — Reviewers must verify vulnerability and policy gates, including how exceptions expire and are remediated.
- **DO-173** — Reviewers must verify environment and infrastructure drift controls.
- **DO-174** — Reviewers must verify post-deployment detection, validation, stop, and rollback capabilities.
- **DO-175** — Reviewers must verify backup scope, restore evidence, recovery sequencing, and business-approved objectives.
- **DO-176** — Reviewers must verify actionable monitoring, ownership, and incident escalation before launch.
- **DO-177** — Reviewers must verify capacity limits, quotas, scaling behavior, and downstream constraints.
- **DO-178** — Reviewers must verify supported versions, patch obligations, and platform lifecycle plans.
- **DO-179** — The review outcome must be recorded as approved, approved with conditions, rework required, exception required, or rejected.
- **DO-180** — Material post-approval changes to topology, identity, persistence, exposure, pipelines, or recovery design require reassessment.

## Required Review Record

- Scope and release identifier
- Participants and approvers
- Evidence reviewed
- Findings and conditions
- Accepted risks and expiry dates
- Final decision and closure evidence