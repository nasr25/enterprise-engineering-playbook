# Pull Request & Code Review — Template

## Change Summary
- Problem / requirement:
- Solution:
- Scope:
- Related issue / change:

## Risk
- Risk level: Low / Medium / High
- Security impact:
- Data / schema impact:
- Authorization impact:
- Performance impact:
- Availability impact:
- Compatibility impact:

## Author Checklist
- [ ] Change is focused and understandable.
- [ ] No credentials, secrets, private keys, or environment-specific sensitive values are committed.
- [ ] Authentication and authorization are enforced at trusted server boundaries.
- [ ] No authorization is based solely on hard-coded business role names where configurable permissions/policies are required.
- [ ] Inputs are validated and outputs encoded appropriately.
- [ ] Queries are parameterized and critical access paths are indexed.
- [ ] Errors do not expose sensitive implementation details.
- [ ] Logs are useful and do not expose secrets or unnecessary sensitive data.
- [ ] Tests cover success, failure, authorization, and relevant edge cases.
- [ ] Database migrations are safe and backward-compatible where required.
- [ ] Dependencies are justified and security-scanned.
- [ ] Documentation / API contract / runbook updated where applicable.
- [ ] Rollback or roll-forward implications are understood.

## Reviewer Checklist
- [ ] Correctness and business rules
- [ ] Security and permissions
- [ ] Architecture boundaries
- [ ] Data integrity and concurrency
- [ ] Failure handling and resilience
- [ ] Performance and scalability
- [ ] Test quality, not only coverage percentage
- [ ] Maintainability and readability
- [ ] Observability
- [ ] Operational / deployment risk

## Evidence
- Test results:
- Security scan:
- Screenshots / API examples:
- Migration validation:
- Performance evidence:

## Review Outcome
Approve only when blocking findings are resolved or explicitly risk-accepted through the approved exception process.
