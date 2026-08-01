# Environments, Configuration, Secrets, and Certificates

## Mandatory Rules

- **DO-037** — Development, test, staging, and production environments must have explicit purposes and controlled boundaries.
- **DO-038** — Production credentials, keys, certificates, and sensitive data must not be reused in non-production environments.
- **DO-039** — Environment parity must be sufficient to reveal deployment, integration, security, and performance risks before production.
- **DO-040** — Configuration must be externalized from application binaries and images where values vary by environment.
- **DO-041** — Configuration schemas, required values, defaults, and validation rules must be documented.
- **DO-042** — Applications must validate critical configuration at startup and fail safely when invalid.
- **DO-043** — Secrets must be stored and delivered through an approved secret-management mechanism.
- **DO-044** — Secrets must not appear in source control, build logs, container layers, command history, telemetry, or deployment output.
- **DO-045** — Secret access must use least privilege, short-lived credentials where practical, and auditable identity.
- **DO-046** — Secrets must have owners, rotation schedules, revocation procedures, and emergency replacement processes.
- **DO-047** — Certificate inventories must include owner, purpose, subject, issuer, location, expiry, and renewal method.
- **DO-048** — Certificate renewal must be automated where feasible and monitored before expiration.
- **DO-049** — Private keys must be protected from export and unauthorized use according to risk.
- **DO-050** — Feature flags must have owners, purpose, defaults, targeting rules, expiry dates, and removal plans.
- **DO-051** — Security controls must not be disabled through ordinary environment configuration.
- **DO-052** — Configuration changes in protected environments must be versioned, approved, and auditable.
- **DO-053** — Production data used outside production must be minimized, masked, authorized, and traceable.
- **DO-054** — Environment drift must be detected and corrected through automation or documented reconciliation.

## Evidence

- Environment inventory
- Configuration schema
- Secret and certificate inventory
- Rotation evidence
- Drift reports