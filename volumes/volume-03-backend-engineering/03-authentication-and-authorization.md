# Authentication and Authorization

## Mandatory Rules

- **BE-027** — Backend services must validate the authenticity, issuer, audience, lifetime, and integrity of credentials before trusting identity claims.
- **BE-028** — Authorization must be evaluated for every protected operation and object, including indirect and bulk access.
- **BE-029** — Authorization policy must use permissions, attributes, ownership, or policy rules rather than hardcoded role-name comparisons.
- **BE-030** — A user-visible identifier or tenant identifier supplied by the client must not be trusted without binding it to authenticated context.
- **BE-031** — Services must prevent horizontal and vertical privilege escalation through object-level and function-level checks.
- **BE-032** — Administrative operations must use explicit elevated permissions and must produce security audit events.
- **BE-033** — Service accounts and machine identities must be scoped to the minimum required permissions and must not share human credentials.
- **BE-034** — Authorization decisions must default to deny when policy input is missing, malformed, expired, or unavailable unless an approved exception defines safe degraded behavior.
- **BE-035** — Token and session revocation requirements must match the risk of the protected operation.
- **BE-036** — Impersonation or delegated access must be explicit, time-bound where practical, auditable, and distinguish the acting identity from the represented identity.
- **BE-037** — Authorization caches must include all policy-relevant context and use bounded freshness.
- **BE-038** — Tests must cover allowed, denied, cross-user, cross-tenant, expired, revoked, and privilege-escalation cases.

## Enforcement Order

1. Authenticate the caller.
2. Resolve trusted tenant and identity context.
3. Validate request structure.
4. Authorize the operation and target object.
5. Execute business rules and side effects.
6. Record relevant audit evidence.
