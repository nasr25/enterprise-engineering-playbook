# REST API Standards

## Mandatory Rules

- **BE-013** — Resource-oriented APIs must use nouns for resource paths and standard HTTP methods according to their defined semantics.
- **BE-014** — GET and HEAD must be safe; GET, PUT, DELETE, and other documented idempotent operations must remain idempotent.
- **BE-015** — POST must be used for non-idempotent creation or commands unless an idempotency mechanism is provided.
- **BE-016** — Successful creation should return `201 Created` with a stable resource location when one exists.
- **BE-017** — `202 Accepted` must include a way to query progress or final outcome.
- **BE-018** — APIs must distinguish authentication failure, authorization denial, missing resources, conflicts, validation errors, throttling, and server failure using appropriate status codes.
- **BE-019** — Collection endpoints must use bounded pagination and deterministic ordering.
- **BE-020** — Filtering and sorting fields must be allowlisted; client input must not be translated directly into unrestricted database expressions.
- **BE-021** — Partial updates must define merge semantics explicitly and prevent unauthorized modification of protected fields.
- **BE-022** — Concurrency-sensitive updates must use version checks, entity tags, or an equivalent optimistic concurrency mechanism.
- **BE-023** — Bulk endpoints must define atomicity, per-item results, maximum batch size, and retry behavior.
- **BE-024** — Cache headers must reflect data sensitivity, freshness, authorization, and invalidation behavior.
- **BE-025** — Hypermedia links may be used where they improve workflow discoverability but must not replace documented contracts.
- **BE-026** — Custom headers must be documented and must not duplicate standard HTTP semantics without justification.

## URI Guidance

Prefer stable identifiers and shallow paths. Use nested paths only when the child is meaningfully scoped by the parent. Avoid embedding actions in paths when standard resource semantics are sufficient; model true business commands explicitly when they are not.
