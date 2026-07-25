# Backend Review Checklist

Use this checklist for new backend services, major API changes, integrations, background workers, and security-sensitive backend modifications.

## API and Contracts

- API purpose, consumers, ownership, and lifecycle are documented.
- Request and response contracts are explicit, validated, and versioned.
- Pagination, filtering, sorting, concurrency, and idempotency are addressed where applicable.
- Breaking changes have migration and deprecation plans.

## Security

- Authentication is delegated to an approved identity provider.
- Authorization is enforced server-side at operation and object level.
- Tenant context is trusted, validated, and consistently applied.
- Secrets are externalized and access is least-privileged.
- Sensitive operations are auditable.

## Data and Transactions

- Data ownership and transaction boundaries are explicit.
- Queries are bounded, parameterized, indexed, and free of avoidable N+1 patterns.
- Concurrency, retries, isolation, rollback, and migration behavior are defined.
- External calls are not performed inside database transactions without justification.

## Reliability and Operations

- Timeouts, retry limits, backoff, circuit breaking, and idempotency are defined.
- Background jobs and consumers are observable, replay-safe, and failure-aware.
- Logs, metrics, traces, health checks, dashboards, and alerts exist.
- Capacity limits, rate limits, quotas, and graceful degradation are addressed.

## Quality and Delivery

- Unit, integration, contract, security, and performance tests cover critical behavior.
- Configuration is validated at startup and differs safely by environment.
- Deployment, migration, rollback, and recovery procedures are documented.
- Operational ownership and runbooks are assigned.

## Mandatory Rules

- **BE-137** — Backend reviews must verify server-side enforcement of authorization, validation, business rules, and data integrity.
- **BE-138** — Critical API flows must include automated tests for success, validation failure, authentication failure, authorization failure, conflict, dependency failure, and retry behavior.
- **BE-139** — Database migrations must be reviewed for locking, duration, rollback, compatibility, and operational risk before production execution.
- **BE-140** — New background jobs and message consumers must define idempotency, retry limits, dead-letter behavior, observability, and replay safety.
- **BE-141** — Security-sensitive changes must include threat-focused review of authentication, authorization, tenant isolation, secrets, logging, and abuse resistance.
- **BE-142** — Performance-sensitive endpoints must provide evidence that query count, latency, memory, payload size, and downstream usage remain within approved limits.
- **BE-143** — Production readiness requires named ownership, dashboards, alerts, runbooks, configuration validation, and rollback capability.
- **BE-144** — Unresolved high-risk backend findings require explicit risk acceptance by the authorized owner before production release.
