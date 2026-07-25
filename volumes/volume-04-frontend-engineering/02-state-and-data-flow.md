# State and Data Flow

## Purpose

Keep state ownership, synchronization, and lifecycle behavior explicit and predictable.

## Mandatory Rules

- **FE-016** — Every state value must have one authoritative owner.
- **FE-017** — Server state, URL state, form state, session state, and local UI state must be treated as distinct categories.
- **FE-018** — Server responses must not be copied into multiple mutable stores without a synchronization strategy.
- **FE-019** — Derived values should be computed rather than independently stored.
- **FE-020** — URL-addressable filters, pagination, and navigation state should be represented in the URL when users need bookmarking or sharing.
- **FE-021** — State updates must be deterministic and observable during debugging.
- **FE-022** — Asynchronous requests must define loading, success, empty, stale, partial, and error states.
- **FE-023** — Optimistic updates must define rollback, conflict, and duplicate-submission behavior.
- **FE-024** — Cached server state must define freshness, invalidation, and refetch rules.
- **FE-025** — Sensitive data must not persist in browser storage unless explicitly required and risk-approved.
- **FE-026** — Cross-tab state synchronization must be explicit and protected from stale or conflicting updates.
- **FE-027** — Forms must distinguish initial, dirty, validating, submitting, succeeded, and failed states.
- **FE-028** — Unsaved user work must be protected against accidental navigation where business impact warrants it.
- **FE-029** — State restoration after refresh must not bypass authentication or authorization checks.
- **FE-030** — State-management libraries must not become hidden service locators or unrestricted global dependency containers.

## Review Questions

- Who owns each state value?
- What invalidates it?
- Can two sources disagree?
- What survives refresh, logout, or tenant change?
- How are stale writes detected?