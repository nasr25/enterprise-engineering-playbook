# AI Engineering Review Checklist

- **AI-171 — Purpose and Ownership Gate:** Confirm purpose, owner, users, prohibited uses, risk class, and accountability are documented.
- **AI-172 — Data Gate:** Confirm provenance, authorization, classification, minimization, quality, lineage, retention, and leakage controls.
- **AI-173 — Evaluation Gate:** Confirm baseline, acceptance metrics, representative evaluation, error analysis, robustness, and promotion evidence.
- **AI-174 — GenAI and RAG Gate:** Where applicable, confirm prompt versioning, injection resistance, retrieval authorization, grounding, citations, and regression evaluation.
- **AI-175 — Security Gate:** Confirm threat model, least privilege, endpoint protection, supply-chain integrity, exfiltration tests, isolation, and emergency disable controls.
- **AI-176 — Privacy and Responsible-AI Gate:** Confirm privacy review, transparency, fairness risks, human review requirements, contestability, and applicable obligations.
- **AI-177 — Agent Safety Gate:** Where agents exist, confirm tool allowlists, independent authorization, parameter validation, bounded autonomy, approvals, audit, and loop limits.
- **AI-178 — MLOps Gate:** Confirm versioning, reproducible deployment, rollback, observability, drift strategy, capacity, resilience, and runbooks.
- **AI-179 — Production Readiness Gate:** Confirm failure modes, fallback behavior, operational ownership, incident response, continuity, and support readiness.
- **AI-180 — Evidence Gate:** Release approval MUST reference test results, evaluation artifacts, security evidence, approvals, known limitations, and accepted residual risks.

## Review Outcome

A review MUST end with one of: **Approved**, **Approved with time-bound conditions**, or **Rejected pending remediation**. Exceptions MUST identify owner, rationale, risk, compensating controls, and expiry date.
