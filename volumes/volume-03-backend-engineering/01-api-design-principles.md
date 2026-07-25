# API Design Principles

## Mandatory Rules

- **BE-001** — APIs must expose business capabilities and stable resource or operation semantics rather than mirroring database tables.
- **BE-002** — Every API must have an identified owner, consumers, lifecycle state, data classification, and support expectations.
- **BE-003** — Contracts must be specified before or with implementation and stored in version control.
- **BE-004** — Publicly consumed behavior includes status codes, schemas, headers, ordering, pagination, error structures, side effects, and timing assumptions.
- **BE-005** — Breaking changes require an explicit versioning and migration plan.
- **BE-006** — APIs must use consistent naming, casing, date-time, identifier, nullability, and enumeration conventions.
- **BE-007** — Server-side authorization and validation must occur before business side effects.
- **BE-008** — Requests that may be retried must define idempotency behavior.
- **BE-009** — Long-running work must not hold synchronous requests open beyond approved service limits; asynchronous execution must expose status and outcome.
- **BE-010** — APIs must define bounded payload sizes, timeouts, rate limits, and pagination limits.
- **BE-011** — Sensitive fields must not be returned merely because they exist in an internal model.
- **BE-012** — Generated documentation and examples must not include live secrets, production identifiers, or personal data.

## Required Evidence

- Machine-readable contract where applicable
- Consumer examples
- Error model
- Compatibility decision
- Ownership and support information
