# Performance and Delivery

## Purpose

Control loading cost, runtime responsiveness, rendering stability, and release behavior from development through production.

## Mandatory Rules

- **FE-076** — User-facing performance objectives must be defined for critical journeys and measured in production where permitted.
- **FE-077** — JavaScript, CSS, font, and image budgets must be established for major entry points.
- **FE-078** — Bundles must be analyzed regularly and duplicate or unused dependencies removed.
- **FE-079** — Code splitting must follow user journeys and avoid excessive request fragmentation.
- **FE-080** — Images must use appropriate dimensions, formats, compression, responsive variants, and lazy loading.
- **FE-081** — Fonts must be minimized, subset where appropriate, and loaded without blocking essential content.
- **FE-082** — Critical content must not depend on unnecessary third-party resources.
- **FE-083** — Long-running work must not block the main thread beyond approved responsiveness thresholds.
- **FE-084** — Rendering loops, unnecessary reactivity, and uncontrolled component re-renders must be detected and corrected.
- **FE-085** — Large lists and data grids must use pagination, virtualization, or bounded rendering.
- **FE-086** — Caching headers, asset fingerprinting, and immutable asset delivery must support safe releases.
- **FE-087** — The application shell and HTML entry point must not be cached in a way that traps users on incompatible releases.
- **FE-088** — Deployments must support rollback and must handle clients with older assets during rolling releases.
- **FE-089** — Service workers require explicit version, update, cache invalidation, offline, and rollback strategies.
- **FE-090** — Performance regressions must be detected through CI budgets, synthetic tests, or production telemetry.

## Minimum Evidence

- Bundle report
- Performance budget
- Critical journey measurements
- Cache and release strategy
- Regression-test results