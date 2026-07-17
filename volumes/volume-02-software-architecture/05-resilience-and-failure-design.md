# Resilience and Failure Design

## Objective

Design systems to fail in controlled, observable, recoverable ways while protecting data integrity and essential business capabilities.

## Mandatory Rules

### ARC-043 — Failure Is a Design Input

Architectures **MUST** identify credible failures across applications, dependencies, networks, infrastructure, data stores, identities, certificates, quotas, and human operations.

### ARC-044 — Criticality Classification

Capabilities and dependencies **MUST** be classified by business criticality, availability target, recovery time objective, recovery point objective, and maximum tolerable disruption where applicable.

### ARC-045 — No Undocumented Single Point of Failure

A single point of failure affecting a required availability or recovery objective **MUST** be removed or explicitly risk-accepted.

### ARC-046 — Graceful Degradation

Systems **SHOULD** preserve safe essential functionality when noncritical dependencies or features are unavailable.

### ARC-047 — Bulkhead Isolation

Workloads, tenants, queues, connection pools, and dependencies **SHOULD** be isolated where resource exhaustion or failure could spread across unrelated capabilities.

### ARC-048 — Circuit Breaking

Repeated calls to an unavailable or unhealthy dependency **SHOULD** be interrupted using circuit breaking or equivalent load-shedding controls.

### ARC-049 — Capacity Protection

Systems **MUST** define concurrency, queue, connection, payload, rate, and resource limits that protect availability under load or abuse.

### ARC-050 — Recovery Is Tested

Backup, restoration, failover, rebuild, replay, and reconciliation procedures **MUST** be tested at a frequency proportional to system criticality.

### ARC-051 — Data Consistency During Failure

Transactions and workflows **MUST** define consistency boundaries, partial-failure behavior, compensation, reconciliation, and manual recovery where atomic completion is impossible.

### ARC-052 — Safe Startup and Shutdown

Services **MUST** handle startup, readiness, draining, shutdown, and in-flight work without silently losing or corrupting accepted operations.

### ARC-053 — Dependency Health Is Not Service Health

Health endpoints **MUST** distinguish process liveness, readiness to receive traffic, and degraded dependency state. A service must not report healthy when it cannot perform its critical function.

### ARC-054 — Chaos and Failure Testing

High-criticality systems **SHOULD** perform controlled failure injection or equivalent resilience tests for material failure scenarios.

## Failure Design Evidence

Architecture reviews should include:

- Failure-mode analysis
- Dependency criticality map
- Timeout and retry budgets
- Capacity and overload behavior
- Recovery and reconciliation workflows
- RTO and RPO evidence
- Backup and restore test results
- Degraded-mode behavior
- Operational runbooks