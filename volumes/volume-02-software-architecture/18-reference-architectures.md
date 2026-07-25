# Reference Architectures

## Purpose

Provide reusable starting points while preserving explicit design decisions and avoiding cargo-cult implementation.

## Reference Architecture A — Internal Business Application

Typical elements:

- Managed enterprise identity provider
- Web or mobile client
- Protected application/API tier
- Relational system of record
- Centralized audit, logs, metrics, and tracing
- Approved email, document, and integration services
- Reverse proxy or application gateway between trust zones

## Reference Architecture B — Public Digital Service

Typical elements:

- CDN and protected public ingress
- WAF, rate limiting, and abuse controls
- Stateless application replicas
- Isolated internal APIs and data tier
- Queue-backed asynchronous work
- External-service adapters with timeouts, retries, and circuit breaking
- End-to-end observability and security audit

## Reference Architecture C — Event-Driven Integration

Typical elements:

- Contract-governed event schemas
- Transactional outbox or equivalent publication guarantee
- Durable broker
- Idempotent consumers
- Dead-letter handling and replay controls
- Reconciliation and business-level monitoring

## Reference Architecture D — Multi-Tenant Platform

Typical elements:

- Trusted tenant identity context
- Central authorization and entitlement policy
- Tenant-safe repository/data-access layer
- Isolation model matched to risk
- Per-tenant quotas and observability
- Tenant-aware backup, export, suspension, and deletion

## Mandatory Rules

- **ARC-197** — A reference architecture is a starting point, not an automatic approval; project-specific risks and deviations must be documented.
- **ARC-198** — Teams adopting a reference architecture must identify which components are mandatory, optional, substituted, or excluded.
- **ARC-199** — Reference architectures must remain vendor-neutral at the logical level even when implementation examples name products.
- **ARC-200** — Each reference architecture must define trust boundaries, data ownership, failure behavior, observability, deployment assumptions, and recovery expectations.
- **ARC-201** — Reusable components must publish supported use cases, limits, ownership, versioning, and deprecation policy.
- **ARC-202** — Reference architectures must be reviewed periodically against incidents, platform changes, security findings, and operational evidence.
