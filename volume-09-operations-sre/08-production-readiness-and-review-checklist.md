# Production Readiness and Review Checklist

- **SRE-161 — Ownership Gate:** Confirm named owners, support coverage, service catalog entry, escalation path, and lifecycle state.
- **SRE-162 — Reliability Objective Gate:** Confirm criticality, SLI definitions, SLO targets, SLA commitments where applicable, and error-budget policy.
- **SRE-163 — Dependency Gate:** Confirm critical upstream, downstream, identity, network, data, and vendor dependencies are documented.
- **SRE-164 — Observability Gate:** Confirm logs, metrics, traces, dashboards, synthetic checks, and correlation are sufficient for diagnosis.
- **SRE-165 — Alerting Gate:** Confirm critical alerts are actionable, owned, tested, severity-mapped, deduplicated, and linked to runbooks.
- **SRE-166 — Capacity Gate:** Confirm expected peak load, headroom, saturation thresholds, queues, connections, and scaling limits are validated.
- **SRE-167 — Resilience Gate:** Confirm timeout, retry, backpressure, circuit-breaking, graceful degradation, and overload behavior as applicable.
- **SRE-168 — Data Protection Gate:** Confirm backup scope, frequency, retention, encryption, protected copies, and restore evidence.
- **SRE-169 — Recovery Gate:** Confirm RTO, RPO, dependency-aware restore order, failover, failback, reconciliation, and DR exercise evidence.
- **SRE-170 — Incident Readiness Gate:** Confirm severity criteria, incident roles, communication channels, evidence capture, and escalation procedures.
- **SRE-171 — Runbook Gate:** Confirm critical operational and failure procedures have current, tested, executable runbooks.
- **SRE-172 — Change Safety Gate:** Confirm rollback, stop conditions, validation, monitoring, and appropriate staged rollout for high-risk changes.
- **SRE-173 — Security Operations Gate:** Confirm privileged access, emergency access, telemetry protection, credential rotation, and audit requirements.
- **SRE-174 — Certificate and Dependency Expiry Gate:** Confirm certificates, licenses, credentials, and critical third-party expiry conditions are monitored where relevant.
- **SRE-175 — Performance Gate:** Confirm critical latency, throughput, saturation, and long-running behavior have representative evidence.
- **SRE-176 — Operational Automation Gate:** Confirm automated operational actions are bounded, observable, reversible where possible, and safe on failure.
- **SRE-177 — Business Continuity Gate:** Confirm business workarounds and stakeholder communication are aligned with technical continuity plans.
- **SRE-178 — Known Risk Gate:** Confirm unresolved production risks, known errors, technical debt, and accepted exceptions have explicit owners and dates.
- **SRE-179 — Launch Decision:** Production launch MUST result in Approved, Approved with time-bound conditions, or Rejected pending remediation.
- **SRE-180 — Evidence Gate:** Production approval MUST reference objective evidence for monitoring, testing, recovery, security, capacity, rollback, and operational ownership.

## Production Readiness Outcome

Approval is evidence-based. A service is not production-ready merely because deployment succeeds; it must also be supportable, observable, recoverable, secure, and capable of failing safely.
