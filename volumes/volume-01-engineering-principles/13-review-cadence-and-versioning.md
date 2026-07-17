# Review Cadence and Versioning

## Purpose

The playbook must remain current, enforceable, and compatible with evolving technology, threats, regulations, and organizational needs.

## Rules

### ENG-067 — Scheduled Review

Each volume **MUST** have an accountable owner and be reviewed at least annually, or more frequently when risk, technology, regulation, or organizational change requires it.

### ENG-068 — Triggered Review

A review **MUST** be initiated after material incidents, major architecture changes, significant audit findings, new regulatory obligations, platform end-of-support announcements, or repeated rule exceptions.

### ENG-069 — Semantic Versioning

Published playbook releases **MUST** use semantic versioning:

- Major: incompatible governance or mandatory-control changes
- Minor: backward-compatible rules, chapters, or control enhancements
- Patch: clarifications, corrections, and nonmaterial improvements

### ENG-070 — Change Classification

Every change **MUST** identify whether it is mandatory, recommended, explanatory, deprecated, or editorial, and state any implementation deadline.

### ENG-071 — Deprecation Lifecycle

Deprecated rules or practices **MUST** identify the replacement, migration guidance, effective date, and removal date where applicable.

### ENG-072 — Effective-Date Control

New mandatory requirements **MUST** define when they apply to new systems, existing systems, and in-flight releases.

### ENG-073 — Changelog Integrity

Each published release **MUST** maintain a changelog describing added, changed, deprecated, removed, fixed, and security-relevant content.

## Review Inputs

Reviews should consider:

- Incident and problem-management trends
- Audit and penetration-test findings
- Exception frequency and expiry patterns
- Developer and operator feedback
- Dependency and platform lifecycle changes
- Regulatory and contractual updates
- Industry standards and threat intelligence
- Measured control effectiveness

## Approval

Material changes require review by the relevant engineering, architecture, security, data, operations, and governance stakeholders according to scope.