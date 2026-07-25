# Availability and Disaster Recovery Architecture

## Purpose

Align resilience, continuity, and recovery design with business impact and verified operational capability.

## Mandatory Rules

- **ARC-185** — Each critical service must define approved availability, recovery time objective, recovery point objective, and maximum tolerable outage.
- **ARC-186** — Availability targets must include all critical dependencies and must not exceed the capability of required downstream services without mitigation.
- **ARC-187** — Redundancy must remove meaningful failure modes; duplicate components in the same failure domain do not constitute high availability.
- **ARC-188** — Failover must preserve security, data integrity, configuration, secrets, observability, and administrative control.
- **ARC-189** — Backups must be encrypted where required, access-controlled, monitored, retained according to policy, and protected from the same failure or compromise as the primary data.
- **ARC-190** — Restore procedures must be tested using representative data and must verify application-level correctness, not only backup-file readability.
- **ARC-191** — Disaster recovery design must identify invocation authority, communication paths, dependencies, sequencing, and return-to-normal procedures.
- **ARC-192** — Recovery automation must be version-controlled, reviewed, and tested; undocumented manual knowledge must not be the sole recovery mechanism.
- **ARC-193** — Active-active designs must explicitly address conflict resolution, ordering, partition behavior, and data convergence.
- **ARC-194** — Recovery exercises must record achieved RTO and RPO, failures, decisions, and corrective actions.
- **ARC-195** — Critical services must define degraded operating modes when full service restoration cannot be immediate.
- **ARC-196** — Architecture changes affecting persistence, topology, identity, or dependencies must trigger review of continuity and recovery plans.

## Minimum Evidence

- Business-approved service targets
- Backup and restore evidence
- DR topology and runbook
- Exercise report
- Dependency recovery sequence
