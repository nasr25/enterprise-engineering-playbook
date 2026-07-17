# Technical Debt Governance

## Purpose

Technical debt must be visible, assessed, prioritized, and reduced deliberately. It must not remain hidden in source code, team memory, or informal conversations.

## Debt Categories

- Architecture and coupling
- Security and privacy
- Reliability and recovery
- Data and schema quality
- Performance and scalability
- Test coverage and automation
- Dependency and platform obsolescence
- Documentation and operability
- Accessibility and user experience

## Rules

### ENG-046 — Debt Registration

Known material technical debt **MUST** be recorded in a managed backlog with an owner, description, affected assets, impact, likelihood, and proposed treatment.

### ENG-047 — Security Debt Priority

Technical debt that weakens confidentiality, integrity, availability, authorization, auditability, or regulatory compliance **MUST** receive risk-based priority and may not be deferred solely for delivery convenience.

### ENG-048 — No Invisible Deferral

A pull request that knowingly introduces or preserves material debt **MUST** reference the corresponding debt record or approved exception.

### ENG-049 — Interest Assessment

Debt records **MUST** describe the continuing cost of delay, including maintenance effort, incident exposure, delivery friction, vendor lock-in, or scaling limits.

### ENG-050 — Retirement Planning

High-risk or recurring-impact debt **MUST** have a target treatment date, measurable exit criteria, and accountable owner.

### ENG-051 — Periodic Review

Teams **MUST** review technical debt periodically and before major releases, platform upgrades, architecture changes, or end-of-support dates.

## Prioritization Model

Debt should be ranked using business impact, security risk, operational frequency, change amplification, implementation effort, dependency urgency, and reversibility.

## Prohibited Practices

- Using `TODO` comments as the only debt register
- Repeatedly postponing unsupported dependencies without an approved plan
- Closing debt items without verified remediation
- Reclassifying defects as debt to avoid release criteria
- Accepting permanent workarounds without ownership or evidence

## Evidence

Acceptable evidence includes backlog items, risk assessments, dependency reports, remediation pull requests, test results, architecture decisions, and closure validation.