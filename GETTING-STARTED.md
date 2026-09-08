# Getting Started

Use this playbook as the engineering baseline for a new project, modernization initiative, integration, or major feature.

## 1. Classify the Project

Record:
- Business owner and technical owner
- Criticality and availability expectations
- Data classification and privacy sensitivity
- Internet-facing / internal / isolated-network exposure
- User population and expected load
- External integrations and third-party dependencies
- Regulatory or contractual obligations
- Whether AI/ML is used
- Whether a mobile application is included and which target platforms/frameworks are used

## 2. Establish Project Engineering Evidence

Copy these templates from `volumes/volume-10-enterprise-templates-checklists/` into the project repository when applicable:

- Project Engineering Charter
- Architecture Decision Record
- Security Threat Model
- Database Design Review
- API & Integration Contract
- Pull Request & Code Review
- Release, Change & Rollback Plan
- Production Readiness Review
- Incident & Post-Incident Review
- AI System Assessment
- Project Master Engineering Checklist

Do not delete irrelevant sections silently. Mark them `Not Applicable` with a short rationale.

## 3. Select Applicable Standards

### Always Applicable
- Volume 01 — Engineering Principles & Governance
- Volume 02 — Software Architecture
- Volume 06 — DevOps & Platform Engineering
- Volume 07 — Testing & Quality Engineering
- Volume 09 — Operations & SRE
- Volume 10 — Templates & Checklists

### Apply by Workload
- Volume 03 — Backend Engineering for APIs, services, workers, integrations, and server-side business logic.
- Volume 04 — Frontend Engineering for web, SPA, desktop-web, or client UI code.
- Volume 05 — Database Engineering for relational, NoSQL, cache, search, analytics, or persistence workloads.
- Volume 08 — AI Engineering for ML, LLM, RAG, embeddings, agents, AI assistants, or model integrations.
- Volume 11 — Mobile Application Engineering for iOS, Android, Flutter, React Native, native mobile, and comparable mobile clients.

## 4. Authorization Design Rule

Do not implement authorization using scattered checks such as fixed business role names in application code.

Preferred model:

`User -> RoleAssignment(scope) -> Role -> Permission -> Policy / Resource Ownership Check`

The exact model may vary, but the system must preserve these properties:
- permissions are explicit;
- assignment is manageable without source-code changes where business access is expected to change;
- authorization is enforced server-side;
- resource ownership / scope prevents IDOR/BOLA;
- privileged bypasses are rare, explicit, logged, and independently protected.

For mobile applications, local navigation guards, biometric checks, hidden UI controls, or cached device state do not replace backend authorization.

## 5. Database Design Rule

Before production:
- define keys, constraints, nullability, and data types deliberately;
- identify critical query patterns;
- design indexes from evidence rather than guesswork;
- validate execution plans for high-impact queries;
- define migration, rollback/roll-forward, retention, backup, and restore behavior.

## 6. Security Baseline

At minimum:
- threat model the system;
- apply least privilege;
- externalize secrets;
- validate all untrusted input;
- parameterize database access;
- enforce authentication and authorization at trusted boundaries;
- protect transport with approved TLS settings;
- run applicable SAST, SCA, secret scanning, and runtime security testing;
- remediate critical/high findings or use the formal exception process;
- log privileged and security-relevant actions without exposing secrets.

Mobile applications must additionally consider secure local storage, deep links, push notifications, device permissions, external intents/files, offline authorization, signing credentials, and store/release controls.

## 7. Quality Gates

A typical enterprise delivery flow is:

`Requirements -> Architecture -> Threat Model -> Implementation -> Code Review -> Automated Tests -> Security Gates -> UAT -> Production Readiness Review -> Change / Release -> Post-Deployment Validation`

Higher-risk systems require stronger evidence, not merely more paperwork.

## 8. AI Coding Assistants

AI coding assistants may help produce code, tests, documentation, and analysis, but they must follow the playbook. Generated output must be reviewed like human-written code and must not introduce hidden external calls, secrets, hardcoded business roles, insecure dependencies, unapproved telemetry, or bypasses around testing/security gates.

## 9. Exceptions

If a rule cannot be met, document:
- rule identifier;
- reason;
- risk;
- compensating control;
- accountable owner;
- approval;
- expiry or review date.

An undocumented deviation is non-conformance, not an exception.

## 10. Release Gate

Before production, complete the Project Master Engineering Checklist and Production Readiness Review. For mobile applications, also complete the Mobile Engineering Review Checklist in Volume 11. Release only when blocking findings are closed or explicitly risk-accepted by the appropriate authority.
