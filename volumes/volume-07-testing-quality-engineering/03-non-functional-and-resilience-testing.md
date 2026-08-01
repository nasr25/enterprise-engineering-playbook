# Non-Functional and Resilience Testing

## Mandatory Rules

- **TST-046** — Performance requirements must define measurable latency, throughput, concurrency, resource, and error objectives.
- **TST-047** — Performance tests must use representative data volumes, payloads, access patterns, and infrastructure.
- **TST-048** — Load tests must verify expected peak and sustained demand.
- **TST-049** — Stress tests must identify saturation points, degradation behavior, and recovery after overload.
- **TST-050** — Soak tests must detect leaks, queue growth, connection exhaustion, storage growth, and long-running instability.
- **TST-051** — Scalability tests must verify that scaling improves capacity without overloading downstream dependencies.
- **TST-052** — Performance baselines must be versioned and compared to detect material regressions.
- **TST-053** — Queries and endpoints handling large datasets must be tested for bounded memory, pagination, timeout, and index usage.
- **TST-054** — Rate limiting and quotas must be tested for fairness, reset behavior, distributed enforcement, and safe responses.
- **TST-055** — Resilience tests must cover dependency timeout, connection failure, partial outage, slow response, and malformed response.
- **TST-056** — Retry behavior must be tested for limits, backoff, jitter, retryable classification, and amplification risk.
- **TST-057** — Circuit breakers and bulkheads must be tested for opening, recovery, isolation, and observability.
- **TST-058** — Queue and stream tests must cover backlog, consumer lag, replay, dead letters, ordering, and duplicate delivery.
- **TST-059** — Failover tests must verify application correctness, security controls, secrets, data consistency, and telemetry.
- **TST-060** — Backup restoration must be tested to application-level correctness and measured against approved RTO and RPO.
- **TST-061** — Disaster recovery exercises must validate invocation, sequencing, dependencies, communications, and return to normal.
- **TST-062** — Degraded modes must be tested to ensure safe and understandable behavior.
- **TST-063** — Chaos experiments must have approved hypotheses, safeguards, abort conditions, owners, and evidence.
- **TST-064** — Resource limit tests must cover CPU, memory, disk, connections, file descriptors, threads, and queue depth where relevant.
- **TST-065** — Network tests must cover latency, packet loss, DNS failure, certificate failure, proxy failure, and connection interruption.
- **TST-066** — Compatibility tests must verify supported runtimes, database versions, browsers, operating systems, and dependent protocols.
- **TST-067** — Accessibility testing must combine automated checks with keyboard and assistive-technology verification for critical flows.
- **TST-068** — Localization testing must verify translation expansion, missing keys, formatting, Unicode, and bidirectional layout.
- **TST-069** — Capacity tests must produce documented bottlenecks, safe operating limits, and scaling recommendations.
- **TST-070** — Non-functional test results must state environment limitations and must not be generalized beyond the tested conditions.