# Observability Architecture

## Purpose

Ensure systems expose enough evidence to understand health, performance, security, dependencies, and business outcomes.

## Mandatory Rules

- **ARC-163** — Every production service must emit structured logs, metrics, and trace context appropriate to its risk and criticality.
- **ARC-164** — Correlation identifiers must propagate across synchronous calls, asynchronous messages, scheduled jobs, and integration boundaries.
- **ARC-165** — Logs must identify timestamp, service, environment, severity, event, outcome, and correlation context without exposing secrets or unnecessary sensitive data.
- **ARC-166** — Metrics must cover traffic, errors, latency, saturation, dependency health, and critical business outcomes.
- **ARC-167** — Distributed tracing must be enabled for critical cross-service flows or an equivalent end-to-end diagnostic mechanism must exist.
- **ARC-168** — Health endpoints must distinguish liveness from readiness and must not report healthy when critical dependencies prevent safe operation.
- **ARC-169** — Alerts must be actionable, owned, prioritized, and tied to an operational response or runbook.
- **ARC-170** — Observability pipelines must be resilient enough that telemetry failure does not cause application failure or unbounded resource consumption.
- **ARC-171** — Audit events and diagnostic logs must remain logically distinct when retention, access, and integrity requirements differ.
- **ARC-172** — Telemetry retention and sampling must be risk-based, documented, and sufficient for incident investigation and capacity analysis.
- **ARC-173** — Dashboards must reflect user-facing service health and not only infrastructure status.
- **ARC-174** — New dependencies must include monitoring, ownership, timeout, and failure indicators before production use.

## Minimum Evidence

- Service-level dashboard
- Alert inventory and owners
- Log field specification
- Trace or correlation example
- Telemetry retention decision
