# Project Engineering Charter — Template

## 1. Project Identity
- Project / service name:
- Business owner:
- Product owner:
- Technical owner:
- Repository:
- Criticality:
- Data classification:
- Intended users:

## 2. Scope
- Business problem:
- In scope:
- Out of scope:
- Key assumptions:
- External dependencies:

## 3. Technology Baseline
- Frontend:
- Backend:
- Database:
- Identity provider:
- Hosting / runtime:
- Messaging / integration:
- Observability:

## 4. Engineering Principles
- [ ] Architecture is documented and reviewed.
- [ ] Authorization is permission/policy based; business access is NOT hard-coded to role names.
- [ ] Least privilege is applied to users, services, databases, and infrastructure.
- [ ] Secrets are externalized and protected.
- [ ] Data model, constraints, indexes, migrations, retention, and backup are designed explicitly.
- [ ] Security, testing, logging, monitoring, rollback, and recovery are designed before production.
- [ ] External dependencies and offline/on-premises constraints are documented.

## 5. Quality Gates
- Requirements / acceptance criteria:
- Architecture review:
- Threat model:
- Code review:
- Automated tests:
- Security scans:
- Performance validation:
- UAT:
- Production readiness review:

## 6. Definition of Done
A feature is complete only when code, tests, authorization, validation, telemetry, documentation, migration impact, security considerations, and rollback implications are addressed.

## 7. Exceptions
| Rule / Standard | Reason | Risk | Compensating Control | Owner | Expiry |
|---|---|---|---|---|---|
