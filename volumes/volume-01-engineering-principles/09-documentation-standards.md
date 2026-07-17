# Documentation Standards

## Purpose

Engineering documentation is a maintained system asset. It must enable teams to understand, operate, secure, change, and recover software without depending on undocumented personal knowledge.

## Mandatory Documentation

Each production system **MUST** maintain, as applicable:

- Purpose, business owner, technical owner, and support contacts
- System context and container-level architecture diagrams
- Data classification and major data flows
- Authentication, authorization, and integration model
- Deployment, configuration, rollback, and recovery procedures
- API and event contracts
- Database schema and migration strategy
- Operational runbooks, alerts, dashboards, SLOs, and escalation paths
- Known risks, approved exceptions, and technical debt
- Architecture Decision Records for significant decisions

## Rules

### ENG-040 — Documentation as Code

Engineering documentation **MUST** be version-controlled and reviewed through the same change workflow used for source code, unless an approved enterprise repository provides equivalent history and review controls.

### ENG-041 — Change-Synchronized Documentation

A change **MUST NOT** be considered complete when it invalidates documentation without updating it in the same delivery increment.

### ENG-042 — Audience and Ownership

Every maintained document **MUST** identify its intended audience, accountable owner, and last review date.

### ENG-043 — Operational Sufficiency

Runbooks **MUST** contain executable steps, prerequisites, validation checks, failure handling, rollback guidance, and escalation criteria.

### ENG-044 — No Secret Material

Documentation **MUST NOT** contain passwords, private keys, access tokens, production secrets, or sensitive personal data.

### ENG-045 — Diagram Integrity

Architecture diagrams **MUST** identify trust boundaries, external dependencies, principal data flows, and security control points when relevant.

## Quality Criteria

Documentation must be accurate, discoverable, concise enough to use under operational pressure, and detailed enough for a qualified engineer unfamiliar with the system to act safely.

## Review Cadence

Critical production documentation must be reviewed at least annually and after any material architecture, security, integration, ownership, or recovery change.