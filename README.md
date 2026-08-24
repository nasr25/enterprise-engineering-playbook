# Enterprise Engineering Playbook

A version-controlled, technology-neutral engineering standard for designing, building, securing, testing, deploying, operating, and governing enterprise software systems.

> Status: Core playbook complete through Volumes 01–10. Ongoing work is limited to maintenance, hardening, cross-reference improvements, and future standards extensions.

## Core Objectives

- Secure-by-design software delivery
- Consistent architecture and coding practices
- Correct database design, indexing, migrations, and data lifecycle
- Permission/policy-based authorization without hardcoded business role names
- DevSecOps, supply-chain security, testing, observability, and operational readiness
- Controlled use of AI/ML, generative AI, RAG, and agentic systems
- Reusable project templates, review gates, and engineering evidence

## Volume Map

1. **Engineering Principles & Governance** — engineering philosophy, rule classification, ADRs, exceptions, documentation, conformance, and AI engineering contract.
2. **Software Architecture** — boundaries, dependencies, integration, resilience, data architecture, multi-tenancy, deployment, security architecture, scalability, DR, and reference architectures.
3. **Backend Engineering** — API standards, authentication, authorization, validation, data access, jobs, messaging, performance, and backend security.
4. **Frontend Engineering** — architecture, state, API integration, security, accessibility, internationalization, performance, testing, and operations.
5. **Database Engineering** — modeling, schema design, SQL, indexing, transactions, migrations, security, HA, backup, lifecycle, NoSQL, and data platforms.
6. **DevOps & Platform Engineering** — source control, CI/CD, artifacts, environments, IaC, containers, Kubernetes, deployment safety, supply-chain security, observability, and incidents.
7. **Testing & Quality Engineering** — strategy, test levels, non-functional testing, security testing, automation, quality gates, test data, defects, release readiness, and metrics.
8. **AI Engineering** — AI governance, ML lifecycle, model evaluation, LLM/RAG, AI security, MLOps, agents, human oversight, and responsible AI.
9. **Operations & SRE** — service ownership, SLI/SLO/SLA, error budgets, observability, alerting, incidents, reliability, capacity, backup, DR, runbooks, and production readiness.
10. **Enterprise Templates & Checklists** — reusable project charter, ADR, threat model, database review, API contract, PR review, release plan, PRR, incident review, AI assessment, and master engineering checklist.

## Start a New Project

For every new project:

1. Read `GETTING-STARTED.md`.
2. Copy the relevant templates from `volume-10-enterprise-templates-checklists/` into the project repository.
3. Complete the Project Engineering Charter before implementation begins.
4. Identify the applicable volumes and rule namespaces.
5. Record material architectural decisions using ADRs.
6. Complete threat modeling, database review, API/integration review, and AI assessment when applicable.
7. Apply the Master Engineering Checklist before production release.
8. Record exceptions explicitly; never silently ignore an applicable rule.

## Rule Namespaces

| Area | Prefix |
|---|---|
| Engineering governance | `ENG` |
| Architecture | `ARC` |
| Backend | `BE` |
| Frontend | `FE` |
| Database | `DB` |
| DevOps / Platform | `DO` |
| Testing / Quality | `TST` |
| AI Engineering | `AI` |
| Operations / SRE | `SRE` |

## Non-Negotiable Engineering Positions

- Authorization MUST be enforced by trusted backend policy/permission checks and resource ownership rules; business permissions MUST NOT depend on fixed role-name checks scattered through code.
- Security controls MUST be designed into architecture and delivery, not appended before release.
- Database indexing MUST follow actual access patterns and be validated with evidence.
- Secrets MUST NOT be committed to repositories or embedded in application code.
- Production changes MUST be traceable, testable, observable, and reversible or have a documented roll-forward strategy.
- Critical systems MUST have validated backup, restore, recovery, monitoring, and operational ownership.
- AI-generated output MUST NOT bypass normal software engineering, security, authorization, testing, or change-control requirements.

## Governance

Normative requirements use stable rule identifiers. Deviations require a documented exception with owner, rationale, risk, compensating controls, and expiry/review date. Changes to the playbook should be proposed through pull requests and reviewed before merging into the default branch.
