# Observability, SLOs, and Incident Operations

## Mandatory Rules

- **DO-127** — Platforms and delivery systems must emit structured logs, metrics, traces, and audit events appropriate to criticality.
- **DO-128** — Telemetry must identify service, environment, version, deployment, region or site, and correlation context.
- **DO-129** — Secrets and unnecessary sensitive data must be excluded or redacted from telemetry.
- **DO-130** — Dashboards must represent user-facing service health, deployment health, capacity, dependencies, and security-relevant conditions.
- **DO-131** — Alerts must be actionable, severity-classified, owned, deduplicated, and linked to response guidance.
- **DO-132** — Alert thresholds must be tested and tuned to reduce both missed incidents and chronic noise.
- **DO-133** — Critical services must define SLIs and SLOs aligned to user outcomes.
- **DO-134** — Error budgets must inform release pace and reliability investment where SLO practices are adopted.
- **DO-135** — SLAs must not promise service levels unsupported by measured SLOs and dependency capability.
- **DO-136** — Deployment events and configuration changes must be visible in operational telemetry.
- **DO-137** — On-call responsibilities, escalation paths, and handover procedures must be documented and current.
- **DO-138** — Incidents must use defined severity, command, communication, containment, recovery, and closure processes.
- **DO-139** — Incident response must preserve evidence and maintain an auditable timeline of decisions and actions.
- **DO-140** — Major incidents must receive blameless post-incident review focused on systemic causes and measurable actions.
- **DO-141** — Corrective actions must have owners, priorities, due dates, and closure evidence.
- **DO-142** — Recurring incidents must trigger problem management rather than repeated tactical recovery.
- **DO-143** — Operational runbooks must be version-controlled, tested, accessible during outages, and reviewed after use.
- **DO-144** — Monitoring failure must be detectable and must not silently remove visibility from critical services.

## Evidence

- SLI/SLO definitions
- Dashboard and alert inventory
- On-call and escalation records
- Incident reports
- Corrective-action tracking