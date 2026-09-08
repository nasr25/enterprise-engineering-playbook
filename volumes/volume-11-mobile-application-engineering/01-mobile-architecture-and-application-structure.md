# 1. Mobile Architecture and Application Structure

Rules `MOB-001`–`MOB-025`.

## Requirements

- `MOB-001` Mobile applications MUST have an explicit architecture appropriate to their complexity and lifecycle.
- `MOB-002` Presentation, domain/business logic, data access, and platform integration concerns SHOULD be separated where doing so improves testability and change safety.
- `MOB-003` UI code MUST NOT contain security-sensitive authorization decisions that are not independently enforced by a trusted backend.
- `MOB-004` Application state ownership MUST be explicit; uncontrolled global mutable state MUST be avoided.
- `MOB-005` Navigation state and route guards MUST NOT be treated as authorization boundaries.
- `MOB-006` Network access SHOULD be centralized behind tested clients or repositories rather than scattered through screens/widgets/controllers.
- `MOB-007` API contracts MUST follow Volume 03 and failures MUST be handled consistently.
- `MOB-008` Dependency direction SHOULD favor stable domain abstractions over framework-specific coupling.
- `MOB-009` Platform-specific capabilities MUST be isolated behind clear interfaces when cross-platform portability is required.
- `MOB-010` Environment configuration MUST be externalized and MUST NOT expose production secrets.
- `MOB-011` Development, test, staging, and production endpoints MUST be distinguishable and controlled.
- `MOB-012` Feature flags MUST have owners, expiry/review expectations, and safe defaults.
- `MOB-013` App lifecycle transitions such as foreground/background/termination MUST be designed explicitly for sensitive workflows.
- `MOB-014` Sensitive screens SHOULD prevent unintended information exposure through lifecycle snapshots where platform controls allow it.
- `MOB-015` Authentication/session state MUST recover predictably after process death, device restart, token expiry, and network loss.
- `MOB-016` Background work MUST be bounded, observable, retry-safe, and compliant with platform restrictions.
- `MOB-017` Long-running work MUST NOT assume unrestricted background execution on iOS or Android.
- `MOB-018` Shared libraries/packages MUST have clear ownership and versioning rules.
- `MOB-019` Third-party SDKs MUST be justified, reviewed, and minimized.
- `MOB-020` Analytics, telemetry, crash reporting, advertising, or attribution SDKs MUST be approved for privacy and security impact before use.
- `MOB-021` Application architecture MUST identify trust boundaries between device, OS services, backend, third-party services, and external apps.
- `MOB-022` Mobile-specific ADRs SHOULD document material choices such as framework, state management, offline strategy, local database, push provider, and release model.
- `MOB-023` Cross-platform abstraction MUST NOT hide platform security requirements that need explicit iOS/Android implementation.
- `MOB-024` Error states, empty states, loading states, degraded states, and offline states MUST be intentionally designed.
- `MOB-025` Architecture reviews MUST consider maintainability, upgradeability, observability, testability, performance, security, and store/platform constraints.

## Review Evidence

Architecture diagrams, ADRs, dependency boundaries, state ownership model, environment model, lifecycle handling, and third-party SDK inventory should be available for material applications.
