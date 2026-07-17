# AI Agent Instructions

This repository is the authoritative Enterprise Engineering Playbook.

All AI coding assistants, including Codex and Claude, must follow these rules:

1. Read `README.md`, this file, and all relevant volume documents before proposing changes.
2. Never invent organizational requirements, security assumptions, roles, permissions, APIs, or database structures.
3. Treat every rule marked **MUST**, **SHALL**, **REQUIRED**, or **PROHIBITED** as mandatory.
4. Never authorize by hardcoded role names. Authorization must use permissions, policies, attributes, or centrally managed authorization rules.
5. Never hardcode credentials, keys, tokens, certificates, internal URLs, or environment-specific configuration.
6. Perform impact analysis before architectural, security, API, schema, or compatibility changes.
7. Preserve backward compatibility unless a breaking change is explicitly approved and documented.
8. Add or update tests, documentation, examples, checklists, and decision records when applicable.
9. Do not weaken validation, authorization, cryptography, audit logging, security headers, or other controls to make a feature work.
10. Clearly identify assumptions, risks, unresolved questions, and exceptions.

## Required Change Workflow

Before implementation:

- Identify applicable rule IDs.
- Review existing content for duplication or conflicts.
- State the proposed scope and impact.

During implementation:

- Use clear, technology-neutral language in core volumes.
- Place framework-specific guidance under technology standards.
- Use normative keywords consistently.
- Provide secure and insecure examples where valuable.

Before completion:

- Verify internal links and rule IDs.
- Confirm no rule contradicts another volume.
- Update `CHANGELOG.md` for meaningful changes.
- Ensure the pull request describes security, data, performance, and compatibility impact.
