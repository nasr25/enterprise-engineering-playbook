# Testing and Quality

## Purpose

Provide confidence in component behavior, user journeys, contracts, accessibility, and release safety.

## Mandatory Rules

- **FE-091** — Tests must focus on externally observable behavior and user outcomes rather than internal implementation details.
- **FE-092** — Domain and application logic must have fast deterministic unit tests.
- **FE-093** — Shared components must have interaction, accessibility, variant, and edge-case tests.
- **FE-094** — API integration tests must cover success, validation, authorization, timeout, partial, and server-error outcomes.
- **FE-095** — Critical user journeys must have end-to-end tests against a production-like environment.
- **FE-096** — End-to-end tests must use stable user-visible selectors or dedicated test identifiers rather than fragile layout selectors.
- **FE-097** — Tests must not depend on uncontrolled external services or shared mutable test data.
- **FE-098** — Visual regression testing should cover design-system components and high-risk layouts.
- **FE-099** — Accessibility automation must be integrated into component or journey tests.
- **FE-100** — Cross-browser and responsive testing must reflect the supported browser and device policy.
- **FE-101** — Loading, empty, stale, offline, unauthorized, forbidden, and error states must be tested explicitly.
- **FE-102** — Time, locale, timezone, RTL, and text-expansion behavior must be testable and deterministic.
- **FE-103** — Flaky tests must be quarantined only temporarily with an owner and resolution date.
- **FE-104** — Test failures must block release when they protect mandatory quality or security controls.
- **FE-105** — Production defects must result in regression tests when technically feasible.

## Test Portfolio

A balanced frontend test portfolio includes:

- Unit tests for pure logic
- Component tests for isolated interactions
- Integration tests for state and API boundaries
- End-to-end tests for critical journeys
- Accessibility and visual checks
- Production synthetic monitoring where appropriate