# 7. Flutter Engineering Guidance

Rules `MOB-146`–`MOB-170`.

These rules complement the technology-neutral mobile requirements. They are not permission to bypass the broader playbook.

## Requirements

- `MOB-146` Flutter applications MUST use an explicit architecture that separates UI from business/domain logic and infrastructure concerns for non-trivial applications.
- `MOB-147` Widget trees SHOULD remain focused on presentation and interaction rather than embedding substantial business rules.
- `MOB-148` State management MUST be selected deliberately and used consistently within a bounded architecture.
- `MOB-149` Teams SHOULD avoid mixing multiple state-management approaches without documented justification.
- `MOB-150` Business logic SHOULD be independently testable without requiring full widget rendering where practical.
- `MOB-151` Dependency injection/service location MUST be controlled and MUST NOT become an unstructured global dependency registry.
- `MOB-152` Network clients, authentication/session handling, serialization, retry policy, and API error translation SHOULD be centralized.
- `MOB-153` Dart models crossing trust boundaries MUST validate or safely parse untrusted server/device input rather than assuming schema correctness.
- `MOB-154` Build flavors or equivalent environment mechanisms SHOULD separate development, staging, and production configuration.
- `MOB-155` Secrets MUST NOT be protected merely by Dart constants, environment defines, asset files, or obfuscation.
- `MOB-156` `flutter_secure_storage` or equivalent platform-backed secure storage SHOULD be used for sensitive tokens when appropriate; ordinary shared preferences MUST NOT store secrets.
- `MOB-157` Platform channels and native plugins MUST validate inputs, minimize exposed methods, and follow the same security controls as native code.
- `MOB-158` Plugin dependencies MUST be reviewed for maintenance status, platform permissions, native code, transitive dependencies, and security impact.
- `MOB-159` Generated serialization/router/state code MUST remain reviewable and reproducible from source-controlled definitions.
- `MOB-160` Widget rebuild scope SHOULD be controlled to avoid unnecessary rendering and performance regressions.
- `MOB-161` Large collections SHOULD use lazy rendering and pagination patterns appropriate to Flutter.
- `MOB-162` Controllers, streams, subscriptions, focus nodes, animation controllers, and similar lifecycle resources MUST be disposed/cancelled appropriately.
- `MOB-163` Expensive synchronous work MUST NOT block the Flutter UI isolate; isolates or suitable asynchronous/native mechanisms SHOULD be used when justified.
- `MOB-164` Navigation libraries/guards MUST NOT be relied upon as server authorization controls.
- `MOB-165` Flutter applications SHOULD include unit tests for domain logic, widget tests for important UI behavior, and integration tests for critical end-to-end journeys.
- `MOB-166` Golden/snapshot tests MAY be used for stable visual components but MUST NOT replace functional/accessibility testing.
- `MOB-167` iOS and Android platform behavior MUST both be tested for plugins, permissions, lifecycle, deep links, notifications, biometrics, storage, and signing.
- `MOB-168` `dart analyze`, formatting/lint rules, dependency checks, automated tests, and release-build verification SHOULD be included in CI.
- `MOB-169` Obfuscation/symbol splitting MAY reduce reverse-engineering convenience or improve diagnostics but MUST NOT be treated as protection for embedded secrets.
- `MOB-170` Flutter SDK and plugin upgrades MUST be reviewed, tested, and released through normal change controls rather than automatically adopted in production.

## Recommended Project Shape

A project may use structures such as feature-first, layered, clean architecture, or another documented model. The required properties are more important than folder names:

- clear UI/domain/data/platform boundaries;
- explicit dependency direction;
- centralized cross-cutting controls;
- testable business logic;
- safe configuration;
- platform-specific code isolated where appropriate;
- consistent state and navigation ownership.

## Review Evidence

Architecture diagram, package structure, state-management decision, dependency inventory, flavor/environment setup, secure-storage implementation, platform-channel review, test results, static analysis, and signed release-build evidence.
