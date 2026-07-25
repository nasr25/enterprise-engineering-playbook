# API Integration and Resilience

## Purpose

Make frontend communication with backend services consistent, bounded, secure, and recoverable.

## Mandatory Rules

- **FE-031** — API access must use approved client abstractions rather than scattered direct network calls.
- **FE-032** — Request construction, authentication headers, correlation identifiers, and error translation must be centralized where practical.
- **FE-033** — Clients must not assume every successful HTTP response contains usable business data.
- **FE-034** — Timeouts, cancellation, and navigation cleanup must prevent abandoned requests from updating obsolete views.
- **FE-035** — Automatic retries must be limited to safe operations and transient failures.
- **FE-036** — Mutation requests must prevent accidental duplicate submission.
- **FE-037** — Idempotency keys must be used when supported for high-impact retried operations.
- **FE-038** — Pagination, sorting, and filtering must follow the backend contract and avoid unbounded result retrieval.
- **FE-039** — API errors must be mapped to stable user-facing outcomes without exposing stack traces or sensitive details.
- **FE-040** — Authentication expiration must have one coordinated recovery path and must not trigger refresh storms.
- **FE-041** — Authorization failures must not be represented as generic network failures.
- **FE-042** — Offline or degraded behavior must be explicit for workflows that require continuity.
- **FE-043** — File uploads must validate type, size, cancellation, progress, and server rejection behavior.
- **FE-044** — File downloads must handle authorization, content type, filename safety, and large payload behavior.
- **FE-045** — Contract changes must be detected through automated tests or schema-driven validation where feasible.

## Minimum Evidence

- API client design
- Error mapping table
- Authentication refresh flow
- Retry and cancellation rules
- Representative contract tests