# Deployment Strategies and Release Safety

## Mandatory Rules

- **DO-091** — Deployment strategy must be selected according to risk, state, compatibility, traffic control, and rollback capability.
- **DO-092** — Rolling deployments must preserve compatibility between old and new application instances.
- **DO-093** — Blue/green deployments must define data migration, traffic switching, validation, and environment retirement behavior.
- **DO-094** — Canary releases must use measurable success criteria, controlled cohorts, automated observation, and stop conditions.
- **DO-095** — Database changes must use backward-compatible expand-and-contract techniques when zero-downtime deployment is required.
- **DO-096** — Rollback must include application, schema, configuration, infrastructure, queues, caches, and external contracts where affected.
- **DO-097** — A rollback plan must not rely on restoring incompatible data without a tested recovery path.
- **DO-098** — Post-deployment verification must test technical health, critical user journeys, security controls, and business outcomes.
- **DO-099** — Deployment failures must stop further promotion and produce actionable evidence.
- **DO-100** — Feature flags must separate deployment from release when progressive exposure materially reduces risk.
- **DO-101** — Kill switches must exist for high-risk integrations, background processes, or features where rapid containment is required.
- **DO-102** — Change windows must reflect business impact, staffing, dependency availability, and recovery time.
- **DO-103** — Emergency changes must retain traceability, minimum testing, authorization, monitoring, and retrospective review.
- **DO-104** — Production deployments must identify decision authority, communication channels, validation owner, and rollback authority.
- **DO-105** — Stateful deployments must explicitly control ordering, draining, concurrency, and data consistency.
- **DO-106** — Release automation must prevent deployment to an unintended account, cluster, server, tenant, or environment.
- **DO-107** — Deployment credentials must be scoped to the target and operation required.
- **DO-108** — Repeated rollback or hotfix patterns must trigger problem investigation and corrective improvement.

## Evidence

- Deployment plan
- Automated validation results
- Rollback test evidence
- Release decision record
- Post-deployment report