# Continuity, Capacity, Cost, and Platform Lifecycle

## Mandatory Rules

- **DO-145** — Critical platform services must define availability, RTO, RPO, maximum outage, and dependency assumptions.
- **DO-146** — Backup scope must include data, configuration, infrastructure state, certificates, pipeline definitions, and required metadata.
- **DO-147** — Backups must be protected from the same compromise or failure domain as primary systems.
- **DO-148** — Restore and disaster-recovery procedures must be tested and must verify application-level correctness.
- **DO-149** — Recovery exercises must record achieved objectives, failures, decisions, and corrective actions.
- **DO-150** — Capacity planning must cover compute, memory, storage, network, connections, queues, licenses, and external limits.
- **DO-151** — Resource requests, limits, quotas, and scaling policies must be based on measurement and forecast demand.
- **DO-152** — Saturation, growth, and exhaustion indicators must be monitored with sufficient lead time for action.
- **DO-153** — Performance and load tests must validate peak, sustained, burst, degradation, and recovery behavior.
- **DO-154** — Cost ownership and allocation metadata must be attached to managed resources where supported.
- **DO-155** — Cost anomalies, idle resources, overprovisioning, and inefficient retention must be reviewed regularly.
- **DO-156** — Cost reduction must not bypass security, resilience, backup, compliance, or service objectives without explicit risk acceptance.
- **DO-157** — Platform components must have supported-version policies, upgrade paths, and end-of-life dates.
- **DO-158** — Unsupported operating systems, runtimes, orchestrators, databases, and pipeline tools must not remain in production without approved exception.
- **DO-159** — Upgrade rehearsals must validate compatibility, rollback, data migration, integrations, and operational tooling.
- **DO-160** — Chaos or controlled-failure testing should be used for critical services where it can be performed safely.
- **DO-161** — Decommissioning must revoke access, remove secrets, preserve required evidence, dispose of data, and release resources.
- **DO-162** — Cloud and vendor portability requirements must be defined according to business risk rather than assumed universally.

## Evidence

- Recovery plans and test reports
- Capacity model
- Cost reports
- Technology lifecycle inventory
- Decommissioning records