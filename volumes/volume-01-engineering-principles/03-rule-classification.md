# Rule Classification and Identifiers

## Normative Language

The terms **MUST**, **MUST NOT**, **SHOULD**, **SHOULD NOT**, and **MAY** are normative:

- **MUST / MUST NOT** — mandatory unless an approved exception exists.
- **SHOULD / SHOULD NOT** — expected practice; deviation requires documented rationale.
- **MAY** — optional practice selected according to context.

Words such as recommended, preferred, avoid, and consider are informative unless paired with normative language.

## Rule Identifier Format

Every enforceable rule **MUST** have a stable identifier:

```text
<DOMAIN>-<NUMBER>
```

Examples:

- `ENG-015` — engineering principle
- `ARCH-021` — architecture rule
- `DB-034` — database rule
- `API-012` — API rule
- `AUTH-018` — authentication or authorization rule
- `SEC-041` — cybersecurity rule
- `TEST-009` — testing rule
- `AI-006` — AI engineering rule

Identifiers **MUST NOT** be reused after a rule is removed. Removed rules remain listed in the change history as retired.

## Rule Metadata

Substantive rules should include:

- Rule ID and title
- Status: Draft, Active, Deprecated, or Retired
- Requirement level
- Purpose and risk addressed
- Scope and applicability
- Mandatory requirements
- Recommended implementation guidance
- Prohibited practices
- Verification method
- Exceptions and compensating controls
- Related standards and rules
- Review checklist

## Severity Classification

Rules may be classified by non-compliance impact:

| Severity | Meaning | Typical examples |
|---|---|---|
| Critical | Likely to enable severe compromise, regulatory breach, or unrecoverable loss | exposed credentials, broken authorization, no recoverable backup |
| High | Significant security, integrity, availability, or operational risk | missing validation, unsafe migrations, unbounded privileged access |
| Medium | Material maintainability, performance, or reliability risk | missing indexes, inadequate tests, undocumented interface changes |
| Low | Consistency or quality improvement with limited immediate risk | naming, formatting, minor documentation gaps |

Severity informs remediation priority but does not change whether a **MUST** requirement is mandatory.

## Applicability

A rule may apply globally or only when defined conditions exist. Conditional applicability **MUST** be explicit. For example:

> SEC-XXX applies to systems that process confidential information or are reachable from untrusted networks.

Teams **MUST NOT** declare a rule inapplicable merely because a technology differs from the provided examples.

## Verification Types

Each mature rule should identify one or more verification methods:

- Automated static check
- Automated dynamic test
- Configuration inspection
- Architecture review
- Code review
- Evidence review
- Penetration or security test
- Operational exercise
- Manual checklist

## Conflict Resolution

When rules appear to conflict:

1. Legal and regulatory obligations take precedence.
2. More specific rules take precedence over general rules.
3. Higher-risk controls take precedence over convenience.
4. The conflict **MUST** be documented and escalated to the rule owner.
5. An ADR or exception record **MUST** capture the selected resolution.
