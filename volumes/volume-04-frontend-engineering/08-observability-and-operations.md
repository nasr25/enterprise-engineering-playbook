# Observability and Operations

## Purpose

Expose user-facing failures, performance, release health, and business-impact signals without compromising privacy.

## Mandatory Rules

- **FE-106** — Production frontends must capture actionable client errors with release, route, environment, and correlation context.
- **FE-107** — Error reporting must remove secrets, tokens, personal data, and sensitive user-entered content unless explicitly approved.
- **FE-108** — Frontend telemetry must distinguish application defects, backend failures, network failures, and user-cancelled actions.
- **FE-109** — Client and server correlation identifiers must be connected for critical workflows.
- **FE-110** — Release identifiers and source-map resolution must support diagnosis of deployed code.
- **FE-111** — Real-user or synthetic measurements must cover critical loading and interaction performance where permitted.
- **FE-112** — Analytics events must have defined purpose, owner, schema, consent basis, retention, and validation.
- **FE-113** — Business analytics must not be used as a substitute for operational error and performance monitoring.
- **FE-114** — Alerting must focus on actionable user-impact changes and avoid alerting on isolated client noise.
- **FE-115** — Feature flags must have owners, safe defaults, auditability, failure behavior, and removal dates.
- **FE-116** — Runtime configuration failure must produce a safe and diagnosable state.
- **FE-117** — Support teams must have documented steps for identifying release, browser, route, correlation identifier, and affected workflow.
- **FE-118** — Frontend incidents must be included in service incident and post-incident processes.
- **FE-119** — Browser support telemetry may inform deprecation only when privacy and governance requirements are met.
- **FE-120** — Operational dashboards must represent user outcomes, not only page-view volume.

## Minimum Evidence

- Client error dashboard
- Release-health view
- Telemetry data dictionary
- Privacy review
- Support troubleshooting guide