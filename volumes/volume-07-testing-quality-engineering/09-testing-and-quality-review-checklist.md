# Testing and Quality Review Checklist

## Strategy and Traceability

- Quality strategy reflects business, security, data, operational, and regulatory risk.
- Acceptance criteria are measurable and testable.
- Critical requirements, controls, risks, and tests are traceable.
- Entry, exit, evidence, ownership, and exception criteria are defined.

## Functional Verification

- Unit, integration, contract, API, UI, system, and end-to-end coverage is proportionate.
- Authorization, tenant isolation, validation, concurrency, and failure paths are tested.
- Critical user journeys and business rules have explicit evidence.
- Database, files, background jobs, schedules, and integrations are covered where applicable.

## Non-Functional Quality

- Performance objectives are measurable and tested at representative scale.
- Load, stress, soak, capacity, resilience, failover, backup, and recovery evidence exists.
- Accessibility, localization, compatibility, mobile, and responsive requirements are verified.

## Security and Privacy

- Testing is aligned with the threat model and data classification.
- SAST, SCA, DAST, secret scanning, authorization, injection, file, API, and transport controls are verified.
- Privacy, sensitive-data handling, audit, tenant isolation, and business-logic abuse are tested.
- Findings are triaged, remediated, retested, or formally accepted.

## Automation and Environments

- Tests are deterministic, isolated, maintainable, diagnostic, and appropriately parallelized.
- Flaky tests have owners and remediation plans.
- CI quality gates are enforced and auditable.
- Test data and environments are representative, secure, reproducible, and monitored.

## Release and Production

- Release readiness includes defects, migrations, rollback, monitoring, and support readiness.
- Smoke, canary, rollback, and post-release validation are defined.
- Production telemetry covers technical and business outcomes.
- Escaped defects and incidents produce verified systemic improvements.

## Decision Outcome

Record one of:

- Approved
- Approved with conditions
- Rework required
- Exception required
- Rejected

The review record must identify evidence, gaps, conditions, owners, due dates, and accepted risks.