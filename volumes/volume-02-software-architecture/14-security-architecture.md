# Security Architecture

## Purpose

Embed security controls in system structure, trust decisions, data flows, and operational boundaries.

## Mandatory Rules

- **ARC-151** — Every material architecture must identify trust boundaries, protected assets, threat actors, abuse cases, and security assumptions.
- **ARC-152** — Authentication must be delegated to an approved identity authority; applications must not create ad hoc identity stores without approval.
- **ARC-153** — Authorization must be enforced server-side at every protected operation and must be based on explicit permissions or policy, not client state.
- **ARC-154** — Least privilege must apply to users, services, workloads, databases, queues, and administrative accounts.
- **ARC-155** — Service-to-service communication crossing a trust boundary must use authenticated and encrypted channels.
- **ARC-156** — Sensitive data must be classified and protected in transit, at rest, in logs, in backups, and during support activities.
- **ARC-157** — Secrets must be stored in an approved secret-management mechanism and must not be embedded in source code, images, templates, or logs.
- **ARC-158** — Public attack surfaces must be minimized and protected with rate limits, input controls, secure defaults, and monitored ingress.
- **ARC-159** — Privileged and security-relevant operations must produce tamper-resistant audit records with actor, action, target, outcome, and timestamp.
- **ARC-160** — Security controls must fail closed unless an approved availability requirement justifies a documented alternative.
- **ARC-161** — Threat modeling must be refreshed after significant changes to exposure, identity, data classification, integration, or tenancy.
- **ARC-162** — Break-glass access must be time-bound, logged, reviewed, and separated from normal administration.

## Review Questions

- What is trusted, and why?
- Where is identity established and propagated?
- Which operations require authorization?
- What happens when the identity provider, policy engine, or secret store is unavailable?
- Can one tenant, service, or operator access another party's data?
