# GraphQL and API Versioning

## Purpose

Define safe use of GraphQL and controlled evolution of public and internal API contracts.

## Mandatory Rules

- **BE-051** — GraphQL must be selected only when consumer-driven query flexibility provides material value over simpler resource-oriented APIs.
- **BE-052** — GraphQL schemas must use domain language, stable naming, explicit nullability, and documented ownership.
- **BE-053** — Resolver authorization must be enforced at the operation and object level; schema visibility is not authorization.
- **BE-054** — Query depth, complexity, aliases, batching, and payload size must be bounded to prevent resource exhaustion.
- **BE-055** — Resolver implementations must prevent uncontrolled N+1 access through batching, caching, or prefetching.
- **BE-056** — Mutations must define validation, idempotency expectations, concurrency behavior, and stable error semantics.
- **BE-057** — Schema introspection in production must follow the approved exposure model and must not reveal sensitive operational metadata.
- **BE-058** — Subscriptions must define authentication lifetime, authorization revalidation, backpressure, disconnect, and recovery behavior.
- **BE-059** — Breaking API changes require a new supported version or an approved compatibility strategy.
- **BE-060** — API versions must represent contract compatibility boundaries and must not be created for ordinary implementation releases.
- **BE-061** — Supported versions must have named owners, usage telemetry, security support, deprecation dates, and retirement criteria.
- **BE-062** — Deprecation must be communicated through machine-readable metadata where practical and through documented consumer channels.
- **BE-063** — Version routing must be explicit and consistently implemented across gateways, documentation, tests, and observability.
- **BE-064** — Backward-compatible additions must preserve existing field meaning, validation assumptions, ordering, and error behavior.
- **BE-065** — Consumer-driven contract tests or equivalent compatibility checks must protect high-impact integrations.

## Required Evidence

- Published schema or API contract
- Complexity and abuse limits
- Compatibility assessment
- Version support matrix
- Deprecation and migration plan