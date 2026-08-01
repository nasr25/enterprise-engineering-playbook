# Quality Strategy and Governance

## Purpose

Establish ownership, risk-based planning, traceability, and evidence requirements for quality engineering.

## Mandatory Rules

- **TST-001** — Every project must define a documented quality strategy proportional to business criticality, security exposure, data sensitivity, and change risk.
- **TST-002** — Quality responsibilities must be shared by product, engineering, security, operations, and quality roles rather than delegated solely to testers.
- **TST-003** — Test scope must be derived from requirements, architecture, threats, failure modes, and operational risks.
- **TST-004** — Acceptance criteria must be specific, measurable, testable, and agreed before implementation begins.
- **TST-005** — Requirements, risks, controls, and tests must be traceable for critical capabilities.
- **TST-006** — Quality planning must identify test levels, environments, data, tools, ownership, entry criteria, and exit criteria.
- **TST-007** — Risk-based testing must prioritize high-impact and high-likelihood failure scenarios.
- **TST-008** — New or changed trust boundaries, data flows, permissions, integrations, and persistence behavior must trigger targeted testing.
- **TST-009** — Quality gates must be explicit, automated where practical, and resistant to informal bypass.
- **TST-010** — A release must not be approved solely from pass percentages; unresolved risk, coverage gaps, and evidence quality must be considered.
- **TST-011** — Independent review is required for tests covering critical security, financial, safety, privacy, or regulatory controls.
- **TST-012** — Test plans must include negative, misuse, boundary, and failure scenarios, not only expected success paths.
- **TST-013** — Quality evidence must be retained according to release, audit, contractual, and regulatory needs.
- **TST-014** — Test cases must identify expected outcomes and must not rely on subjective visual judgment when objective checks are possible.
- **TST-015** — Quality risks accepted for release must name the owner, impact, mitigation, monitoring, expiry, and follow-up action.
- **TST-016** — Teams must review production incidents and escaped defects to update tests, controls, and quality strategy.
- **TST-017** — Shift-left practices must include early review of requirements, architecture, contracts, schemas, and threat models.
- **TST-018** — Shift-right practices must include production telemetry, synthetic checks, canary validation, and user-impact monitoring where appropriate.
- **TST-019** — Test effort must be focused on business and technical risk rather than arbitrary test-count targets.
- **TST-020** — Material deviations from the approved quality strategy require documented approval.