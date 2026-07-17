# AI-Assisted Engineering Contract

## Purpose

This contract defines mandatory controls for using AI systems to generate, modify, review, explain, test, migrate, or document software and infrastructure.

## Accountability

### ENG-030 — Human Accountability

The accountable engineer and approver remain responsible for AI-assisted output. AI tools **MUST NOT** be treated as authors, approvers, risk owners, or authoritative sources.

### ENG-031 — Repository Context First

Before changing code or documentation, an AI agent **MUST** inspect applicable repository instructions, architecture records, playbook rules, interfaces, tests, and nearby implementation patterns.

### ENG-032 — No Fabricated Evidence

AI output **MUST NOT** claim that code was executed, tests passed, vulnerabilities were resolved, files were changed, or deployments succeeded without verifiable evidence.

### ENG-033 — Sensitive Data Protection

Credentials, secrets, private keys, personal data, confidential source code, production data, and restricted architecture information **MUST NOT** be submitted to an AI service unless that use is explicitly approved and protected by applicable contractual and technical controls.

### ENG-034 — Minimal Change Scope

AI-generated changes **SHOULD** be limited to the smallest coherent scope that satisfies the requirement. Unrelated refactoring, dependency replacement, or architectural change requires separate justification.

### ENG-035 — Independent Validation

AI-generated or AI-modified output **MUST** be independently validated using appropriate tests, scans, review, compilation, schema validation, or runtime evidence.

## Required Agent Behavior

AI agents **MUST**:

- Preserve existing behavior unless a change is explicitly required.
- Identify assumptions and uncertainty.
- Follow least privilege and deny-by-default principles.
- Avoid hardcoded credentials, roles, user IDs, URLs, and environment values.
- Add or update tests when behavior changes.
- Perform impact analysis for interfaces, schemas, permissions, and dependencies.
- Document security, compatibility, migration, and rollback implications.
- Stop and report when required evidence or access is unavailable.

## Prohibited Agent Behavior

AI agents **MUST NOT**:

- Disable security controls to make a test pass.
- weaken validation or authorization as a workaround.
- expose internal exceptions, stack traces, secrets, or tokens to clients.
- invent library APIs, configuration keys, standards, citations, or test results.
- merge or deploy code when required quality gates fail.
- delete data, history, or protective configuration without explicit authorized scope.
- silently expand requirements.

## AI Review Checklist

For each material AI-assisted change, verify:

- Applicable instructions and ADRs were read.
- The requested behavior and acceptance criteria are clear.
- The diff is limited and understandable.
- Authorization and data handling remain correct.
- Error and failure paths were considered.
- Tests cover the changed behavior.
- Dependencies and generated code were reviewed.
- No sensitive information was introduced into prompts, logs, fixtures, or commits.
- Claims are supported by evidence.
- Rollback or recovery is understood.

## AI-Readable Instruction Hierarchy

When instructions conflict, agents should apply the following order:

1. Legal, regulatory, and organizational security obligations
2. Repository-local mandatory instructions
3. Accepted ADRs and approved architecture
4. This playbook
5. Technology-specific conventions
6. The current task request

Conflicts **MUST** be reported rather than resolved by silently ignoring a higher-level control.
