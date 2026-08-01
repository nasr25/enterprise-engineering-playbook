# Test Data, Environments, and Reliability

## Mandatory Rules

- **TST-121** — Test data must be representative, controlled, reproducible, and appropriate to the tested risk.
- **TST-122** — Production data must not be used in testing unless explicitly approved, minimized, masked, protected, and auditable.
- **TST-123** — Synthetic data must preserve relevant distributions, relationships, boundaries, and edge cases.
- **TST-124** — Test data builders and fixtures must make scenario intent clear and avoid hidden dependencies.
- **TST-125** — Tests must create and clean up their own mutable data or use isolated disposable environments.
- **TST-126** — Shared test accounts must be avoided for authorization, audit, concurrency, and ownership scenarios.
- **TST-127** — Test credentials must be least-privileged, environment-specific, rotated, and centrally managed.
- **TST-128** — Test environments must document topology, versions, configuration, integrations, and known differences from production.
- **TST-129** — Environment drift must be detected and controlled through automation and configuration management.
- **TST-130** — Critical release tests must run in an environment representative of production trust boundaries and dependencies.
- **TST-131** — External dependencies must use approved sandboxes, controlled simulators, or contract-faithful stubs.
- **TST-132** — Service virtualization must model relevant latency, errors, limits, schemas, and state transitions.
- **TST-133** — Test doubles must not replace integration evidence for critical boundaries.
- **TST-134** — Environment provisioning and teardown should be automated, repeatable, and version-controlled.
- **TST-135** — Test environments must have monitoring sufficient to distinguish product defects from environment failures.
- **TST-136** — Unavailable or unstable test infrastructure must be tracked as an engineering reliability problem.
- **TST-137** — Test suites must fail clearly when prerequisites are missing rather than producing misleading product failures.
- **TST-138** — Time-dependent tests must control clocks, timezone, expiration, and scheduled execution.
- **TST-139** — Data-retention and cleanup processes must apply to test artifacts, logs, files, and databases.
- **TST-140** — Environment access must be role-based, logged, and separated from production privileges.
- **TST-141** — Test endpoints and debug features must not be enabled in production artifacts by default.
- **TST-142** — Test data must include null, empty, minimum, maximum, malformed, duplicate, historic, and future values as applicable.
- **TST-143** — Data migration tests must verify counts, reconciliation, transformations, integrity, and restart behavior.
- **TST-144** — Environment incidents and repeated instability must feed corrective actions and platform improvements.
- **TST-145** — Test evidence must identify the exact environment and configuration used.