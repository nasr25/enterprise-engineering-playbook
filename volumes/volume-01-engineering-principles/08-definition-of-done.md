# Enterprise Definition of Done

## Purpose

The Definition of Done (DoD) establishes the minimum evidence required before a change may be represented as complete or ready for production.

A team may add stricter criteria. It **MUST NOT** remove applicable mandatory criteria without an approved exception.

## Product and Requirement Readiness

- Acceptance criteria are satisfied and traceable to implemented behavior.
- Scope changes and assumptions are documented.
- User-facing behavior, accessibility, localization, and error states are reviewed where applicable.
- Required business, product, data, security, and operational approvals are recorded.

## Architecture and Design

- The implementation conforms to approved architecture and applicable ADRs.
- Material changes include impact analysis.
- Trust boundaries, data flows, integration contracts, and failure modes are understood.
- New technologies and dependencies have approved ownership and lifecycle support.

## Code Quality

- Code is readable, maintainable, and consistent with repository standards.
- No secrets, credentials, environment-specific URLs, or hardcoded authorization decisions are present.
- Error handling is explicit and fails safely.
- Static analysis, formatting, linting, and compilation checks pass.
- Temporary debugging code and unsafe feature flags are removed.

## Security and Privacy

- Authentication and authorization are enforced server-side at all required boundaries.
- Input validation and output encoding are appropriate to the context.
- Sensitive data is minimized, classified, protected, and excluded from unsafe logs.
- Dependency, secret, and security scans meet the approved threshold.
- Security findings are remediated or covered by approved, active exceptions.
- Threat modeling is updated when trust boundaries or high-risk flows change.

## Data and Database

- Schema changes are versioned, reviewed, and tested.
- Migration, backward compatibility, rollback, and data recovery are addressed.
- Constraints and indexes protect integrity and expected query performance.
- Destructive operations require explicit safeguards and verified backups where applicable.

## Testing

- Automated tests cover new behavior and material failure paths.
- Existing relevant tests pass.
- Integration and contract tests are updated when interfaces change.
- Performance, resilience, security, accessibility, or compatibility tests are completed when risk requires them.
- Test evidence is linked to the change.

## Deployment and Operations

- Configuration is externalized and validated per environment.
- Deployment and rollback procedures are tested or demonstrably safe.
- Health checks, logs, metrics, alerts, and dashboards are updated.
- Runbooks, ownership, support contacts, and escalation paths are current.
- Capacity, backup, restore, disaster recovery, and dependency failure implications are addressed.

## Documentation and Governance

- User, developer, API, operational, and architecture documentation is updated as applicable.
- ADRs, exceptions, risk records, and compliance mappings are linked.
- Changelog and release notes describe relevant behavior, risk, and migration requirements.
- Licenses and third-party notices are compliant.

## Release Gate

### ENG-036 — Evidence Before Completion

A change **MUST NOT** be marked done solely because implementation is complete. Applicable verification evidence must exist.

### ENG-037 — No Unknown Critical Failure

A release **MUST NOT** proceed with an unresolved critical security, integrity, recovery, or authorization failure.

### ENG-038 — Failed Gates Block Release

Mandatory automated or manual gates **MUST** block release when they fail, unless an authorized and active exception explicitly covers the failure.

### ENG-039 — Production Verification

After deployment, teams **MUST** verify service health, critical business flows, monitoring, and absence of unexpected security or data integrity impact.

## Completion Record

The pull request, release record, or equivalent evidence should clearly state:

- What changed
- Why it changed
- Tests and scans executed
- Known limitations and residual risks
- Migration and rollback information
- Documentation updated
- Approvals and exceptions
- Production verification outcome
