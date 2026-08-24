# API & Integration Contract — Template

## Identity
- API / integration name:
- Provider owner:
- Consumer owner(s):
- Environment endpoints:
- Data classification:
- Criticality:

## Contract
- Protocol / style:
- Versioning strategy:
- Authentication:
- Authorization model:
- Request / response schemas:
- Pagination:
- Filtering / sorting:
- Idempotency:
- Error model:
- Correlation ID:

## Security
- [ ] TLS and certificate requirements defined.
- [ ] Authentication credentials have lifecycle and rotation controls.
- [ ] Authorization is enforced server-side per operation and resource.
- [ ] Input size and format limits defined.
- [ ] Rate / abuse limits defined.
- [ ] Sensitive fields are minimized and protected.
- [ ] Logs exclude secrets and unnecessary sensitive payloads.

## Resilience
- Timeout:
- Retry policy:
- Backoff / jitter:
- Circuit breaking:
- Duplicate handling:
- Partial failure behavior:
- Provider outage behavior:

## Compatibility
- Breaking-change definition:
- Deprecation period:
- Consumer notification:
- Contract tests:

## Operations
- SLI / SLO:
- Monitoring:
- Alerting:
- Support owner:
- Dependency dashboard:

## Acceptance
Provider and consumer MUST validate the contract in a non-production environment before production enablement.
