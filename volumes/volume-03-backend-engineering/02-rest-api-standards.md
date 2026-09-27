# REST API Standards

## Mandatory Rules

- **BE-013** — Application and integration HTTP APIs MUST use only `GET` and `POST` methods unless a formally approved exception exists. `PUT`, `PATCH`, and `DELETE` MUST NOT be exposed or consumed by default.
- **BE-014** — `GET` MUST be safe and read-only. It MUST NOT create, update, delete, approve, submit, trigger, or otherwise change server-side business state.
- **BE-015** — `POST` MUST be used for creation and every operation that changes server-side state, including updates, deletions, workflow commands, approvals, submissions, and other mutations.
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

## GET/POST-Only HTTP Policy

The enterprise default is intentionally narrower than general REST conventions:

- Read/query: `GET /api/users/123`
- Create: `POST /api/users`
- Update: `POST /api/users/123/update`
- Delete: `POST /api/users/123/delete`
- Business command: `POST /api/requests/123/approve`

Clients, including web and mobile applications, MUST follow the same restriction when calling enterprise APIs. Routing, CORS, WAF/API gateway rules, API documentation, generated clients, and automated tests SHOULD reject or detect unintended `PUT`, `PATCH`, and `DELETE` usage.

A required third-party API that only supports another HTTP method MAY be handled as a documented integration exception. The exception MUST be limited to that external contract and MUST NOT silently change the enterprise API convention.

State-changing `POST` operations MUST still implement appropriate authorization, validation, CSRF protection where cookie-based browser authentication applies, idempotency/concurrency controls where needed, and audit logging. Using `POST` does not by itself provide security.

## URI Guidance

Prefer stable identifiers and shallow paths. Use nested paths only when the child is meaningfully scoped by the parent. Avoid embedding actions in paths when standard resource semantics are sufficient; model true business commands explicitly when they are not.
