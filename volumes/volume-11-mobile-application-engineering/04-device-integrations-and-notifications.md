# 4. Device Capabilities, Integrations, and Notifications

Rules `MOB-076`–`MOB-095`.

## Requirements

- `MOB-076` Device permissions MUST be requested only when needed and with a clear user-facing purpose.
- `MOB-077` Permission denial MUST be handled gracefully without crashing or unsafe fallback behavior.
- `MOB-078` Applications SHOULD support limited/approximate permission modes where platforms provide them.
- `MOB-079` Camera, microphone, location, contacts, photos, Bluetooth, NFC, and sensor access MUST be minimized to the feature requirement.
- `MOB-080` Collected device data MUST follow approved privacy, retention, and transmission requirements.
- `MOB-081` Push notification payloads MUST NOT contain secrets or unnecessary sensitive data.
- `MOB-082` Push notifications MUST be treated as untrusted signals; business state MUST be confirmed with the backend before sensitive actions.
- `MOB-083` Notification actions MUST enforce authentication/authorization when they initiate protected operations.
- `MOB-084` Device push tokens MUST be associated and revoked safely across login, logout, reinstall, token rotation, and account switching.
- `MOB-085` Notification preferences SHOULD be user-controllable where appropriate and centrally enforceable for mandatory operational/security messages.
- `MOB-086` Deep links opened from notifications MUST pass the same input validation and authorization checks as any other deep link.
- `MOB-087` Universal Links / App Links SHOULD be preferred over custom schemes for sensitive navigational flows.
- `MOB-088` QR/barcode input MUST be validated and MUST NOT directly trigger privileged actions without confirmation and authorization.
- `MOB-089` File picker/share-sheet inputs MUST be treated as external untrusted content.
- `MOB-090` External browser, SSO, OAuth/OIDC, and callback flows MUST use approved redirect handling and anti-CSRF/state protections.
- `MOB-091` Device identifiers MUST NOT be assumed stable, unique, secret, or suitable as authentication credentials.
- `MOB-092` Background location or persistent device monitoring MUST require explicit business justification and privacy approval.
- `MOB-093` Native plugins/bridges MUST expose the smallest API surface required and validate all cross-boundary inputs.
- `MOB-094` Third-party mobile SDK network calls and telemetry MUST be inventoried and reviewed.
- `MOB-095` Integrations MUST include degraded-mode behavior for unavailable OS services, revoked permissions, unsupported devices, and vendor outages.

## Review Evidence

Permission matrix, push architecture, link/callback design, third-party SDK inventory, device-integration threat scenarios, and privacy approvals where required.
