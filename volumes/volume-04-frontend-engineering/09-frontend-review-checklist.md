# Frontend Review Checklist

Use this checklist for new frontend applications, major journeys, framework migrations, design-system changes, and material security or performance changes.

## Architecture and State

- Feature and shared-component boundaries are explicit.
- Dependency direction is controlled and free of cycles.
- State ownership, persistence, synchronization, and invalidation are documented.
- Routes support direct navigation, authorization, loading, and error behavior.

## API and Reliability

- API calls use approved clients and stable contracts.
- Timeouts, cancellation, retry, duplicate submission, and authentication expiration are handled.
- Loading, empty, stale, partial, offline, unauthorized, forbidden, and failure states exist.

## Security and Privacy

- Authorization remains server-enforced.
- Rendering, token handling, CSRF, CSP, redirects, third-party scripts, and dependencies are reviewed.
- Sensitive data is excluded from URLs, storage, logs, analytics, and error reports.

## Accessibility and Localization

- Keyboard, focus, semantic structure, labels, contrast, alternatives, and dynamic announcements are verified.
- Automated checks are supplemented by manual testing on critical journeys.
- Localization, text expansion, locale formatting, timezone, and RTL behavior are tested.

## Performance and Delivery

- Performance objectives and asset budgets are met.
- Bundles, images, fonts, rendering, long tasks, and large lists are optimized.
- Caching, release compatibility, service-worker behavior, and rollback are safe.

## Testing and Operations

- Unit, component, integration, end-to-end, accessibility, and browser coverage match risk.
- Client errors, correlations, release identifiers, performance, and user outcomes are observable.
- Feature flags, analytics, support diagnostics, and operational ownership are documented.

## Decision Outcome

The review must record one of:

- Approved
- Approved with conditions
- Rework required
- Exception required
- Rejected

Any unresolved high-risk security, accessibility, privacy, or release-safety finding requires explicit authorized acceptance before production.