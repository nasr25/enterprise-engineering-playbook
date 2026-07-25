# Architecture Review Checklist

Use this checklist for new systems, major enhancements, material integrations, and significant topology or data changes.

## Business and Scope

- Business capability, users, criticality, and service owner are identified.
- Functional boundaries and out-of-scope responsibilities are explicit.
- Quality attributes have measurable priorities and acceptance criteria.

## Structure and Dependencies

- Module or service boundaries follow business ownership and change patterns.
- Dependencies are explicit, directional, replaceable where appropriate, and free of cycles.
- Build-versus-buy and reuse decisions are documented.

## Data

- Systems of record and data owners are named.
- Classification, retention, residency, deletion, backup, and recovery are addressed.
- Schema evolution, migration, reconciliation, and data-quality controls are defined.

## Integration

- Contracts, versions, compatibility, timeouts, retry limits, idempotency, and failure behavior are specified.
- Synchronous chains and shared databases have been challenged.
- Events, queues, dead letters, replay, and reconciliation are governed.

## Security

- Trust boundaries and threat model are current.
- Authentication, authorization, service identity, secrets, encryption, audit, and privileged access are designed.
- Tenant isolation and privacy risks are tested where applicable.

## Reliability and Operations

- Availability, RTO, RPO, degradation, failover, backup, restore, and DR are approved.
- Capacity, scaling, resource limits, quotas, and backpressure are defined.
- Logs, metrics, traces, dashboards, alerts, ownership, and runbooks exist.

## Delivery and Evolution

- Environments, configuration, deployment, rollback, migration, and feature-release controls are documented.
- Architecture decisions, exceptions, risks, and technical debt are traceable.
- Decommissioning, portability, and exit considerations are addressed.

## Decision Outcome

The review must record one of:

- Approved
- Approved with conditions
- Rework required
- Exception required
- Rejected

## Mandatory Rules

- **ARC-203** — Architecture reviews must record participants, evidence considered, decisions, conditions, risks, and owners.
- **ARC-204** — Approval conditions must be measurable and tracked to closure before the relevant production milestone.
- **ARC-205** — Material deviations discovered after approval must trigger reassessment rather than being treated as implementation detail.
- **ARC-206** — Review depth must be proportional to business criticality, security exposure, data sensitivity, operational complexity, and cost of reversal.
- **ARC-207** — No architecture may be approved solely from a presentation; reviewable diagrams, decisions, contracts, and operational evidence are required.
- **ARC-208** — Unresolved high-risk findings require explicit risk acceptance by the authorized owner before production.
