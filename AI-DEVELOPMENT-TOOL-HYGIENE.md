# AI Development Tool Hygiene

This policy governs development-tool residue in source repositories and delivery artifacts. It does **not** prohibit approved AI functionality that is an intentional part of the product.

## Purpose

Repositories MUST remain product-focused, vendor-neutral where practical, auditable, and free from unnecessary artifacts or attribution introduced only by AI-assisted development tools.

## Mandatory Rules

- `AIH-001` Source code, comments, filenames, generated files, documentation, scripts, configuration, and delivery artifacts MUST NOT contain unnecessary references to development assistants or their vendors.
- `AIH-002` Names such as Claude, Codex, ChatGPT, OpenAI, Anthropic, Copilot, Gemini, or equivalent tool/vendor names MUST NOT be introduced merely to identify which assistant generated or edited code.
- `AIH-003` AI SDKs, libraries, agents, MCP integrations, model clients, telemetry, hooks, or related dependencies MUST NOT be added unless they are an approved functional or engineering requirement.
- `AIH-004` Hidden files, assistant-specific instruction files, caches, session files, generated prompts, transcripts, scratch files, or local tool state MUST NOT be committed unless explicitly required and reviewed.
- `AIH-005` Commit subjects and bodies MUST describe the engineering change and MUST NOT contain unnecessary AI-tool attribution, generation notices, assistant branding, or promotional text.
- `AIH-006` Automated assistant attribution such as AI-specific `Co-authored-by`, `Generated-by`, `Assisted-by`, or equivalent trailers MUST NOT be added to commits.
- `AIH-007` Branch names, tags, PR titles/descriptions, release notes, changelogs, build metadata, and deployment artifacts MUST NOT expose unnecessary development-assistant branding.
- `AIH-008` Author and committer identity MUST represent the accountable human or approved organizational automation identity. Identity metadata MUST NOT be falsified or rewritten merely to conceal legitimate human authorship.
- `AIH-009` Existing human authorship, copyright, license, provenance, security evidence, and legally required attribution MUST NOT be removed by hygiene cleanup.
- `AIH-010` Cleanup MUST NOT remove an AI dependency, provider name, model identifier, prompt, configuration, or documentation when it is genuinely required by an approved product feature, integration, test, compliance obligation, or operational procedure.
- `AIH-011` Approved product AI usage MUST follow Volume 08 — AI Engineering and normal security, privacy, testing, dependency, and change controls.
- `AIH-012` Before merge and release, repositories SHOULD be scanned for prohibited development-tool residue across tracked files, filenames, dependency manifests, commit messages, and relevant delivery metadata.
- `AIH-013` Any automated cleanup MUST be reviewed before destructive changes and MUST preserve application behavior, required dependencies, licenses, and auditability.
- `AIH-014` Rewriting published Git history to remove development-tool residue requires explicit repository-owner approval because it changes commit identities and may disrupt clones, branches, tags, signatures, and open work.
- `AIH-015` Exceptions MUST identify the exact reference/dependency retained, business or technical justification, owner, scope, and review/expiry condition where applicable.

## Pre-Merge Hygiene Check

Review at minimum:

- tracked source, comments, docs, configuration, dotfiles, scripts, images, generated artifacts, and filenames;
- dependency manifests and lockfiles for unapproved AI/model/agent SDKs;
- commit subjects/bodies and trailers for unnecessary assistant attribution;
- branch and PR metadata;
- CI/CD definitions for assistant-specific hooks, external calls, telemetry, or secrets;
- build/release packages for accidental assistant artifacts.

Search terms are indicators, not automatic deletion instructions. Context MUST be reviewed before removal because the same terms may be legitimate product functionality.

## Decision Rule

**Development assistance is implementation provenance, not product functionality.** Do not persist assistant-specific residue unless there is a documented reason for the repository or delivered system to contain it.
