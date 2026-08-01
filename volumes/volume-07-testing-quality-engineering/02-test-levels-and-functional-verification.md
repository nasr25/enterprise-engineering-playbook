# Test Levels and Functional Verification

## Mandatory Rules

- **TST-021** — Unit tests must verify isolated business logic, edge cases, and error behavior without unnecessary external dependencies.
- **TST-022** — Unit tests must be deterministic, fast, independently executable, and free from shared mutable state.
- **TST-023** — Integration tests must verify real boundaries such as databases, queues, files, identity systems, and external adapters.
- **TST-024** — Contract tests must verify provider and consumer compatibility for APIs, events, schemas, and message formats.
- **TST-025** — API tests must cover authentication, authorization, validation, status codes, pagination, concurrency, idempotency, and error contracts.
- **TST-026** — Object-level and tenant-level authorization must be tested using identities with differing permissions and ownership.
- **TST-027** — UI component tests must verify behavior, accessibility semantics, states, and user interaction rather than implementation details.
- **TST-028** — End-to-end tests must focus on critical user journeys and must not duplicate all lower-level tests.
- **TST-029** — System tests must validate integrated behavior across deployment topology and critical dependencies.
- **TST-030** — User acceptance testing must validate agreed business outcomes and must use representative scenarios and authorized users.
- **TST-031** — Regression suites must be risk-based, maintained, and executed at appropriate pipeline or release stages.
- **TST-032** — Smoke tests must verify deployment health, critical dependencies, authentication, and core transactions.
- **TST-033** — Database tests must verify constraints, migrations, transaction behavior, concurrency, indexing assumptions, and recovery-sensitive operations.
- **TST-034** — Mobile tests must cover supported devices, operating systems, permissions, lifecycle transitions, network changes, and offline behavior.
- **TST-035** — Browser tests must cover the supported compatibility matrix and responsive breakpoints.
- **TST-036** — File upload and download tests must cover type, size, malware controls, authorization, storage failure, and content-disposition behavior.
- **TST-037** — Date, time, timezone, locale, currency, and RTL behavior must be tested where applicable.
- **TST-038** — Concurrent update scenarios must test lost-update prevention, duplicate submission, and conflict handling.
- **TST-039** — Bulk operations must test partial failure, limits, retries, auditability, and rollback or compensation behavior.
- **TST-040** — Scheduled jobs and event consumers must be tested for retries, duplicate delivery, ordering, poison messages, and restart recovery.
- **TST-041** — Feature flags must be tested in enabled, disabled, partial-rollout, stale-flag, and rollback conditions.
- **TST-042** — External integrations must be tested for timeout, invalid response, throttling, certificate failure, unavailability, and recovery.
- **TST-043** — Error handling tests must verify safe user messages, stable error codes, correlation identifiers, and absence of sensitive leakage.
- **TST-044** — Critical workflows must include tests for cancellation, interruption, retry, and resume behavior.
- **TST-045** — Tests must assert persistent outcomes and side effects, not only HTTP responses or rendered text.