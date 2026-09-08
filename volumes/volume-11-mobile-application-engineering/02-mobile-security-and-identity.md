# 2. Mobile Security and Identity

Rules `MOB-026`–`MOB-055`.

## Requirements

- `MOB-026` Mobile applications MUST treat the device and client runtime as potentially compromised.
- `MOB-027` Authentication MUST rely on trusted identity providers or backend services; local UI state MUST NOT establish identity.
- `MOB-028` Authorization MUST be enforced server-side using permissions, policies, scope, and resource ownership as applicable.
- `MOB-029` Access tokens MUST be short-lived where practical and refresh-token handling MUST minimize replay risk.
- `MOB-030` Sensitive tokens MUST be stored using platform-protected secure storage such as Keychain/Keystore-backed mechanisms.
- `MOB-031` Passwords, API secrets, signing keys, private keys, and privileged service credentials MUST NOT be embedded in source code or application binaries.
- `MOB-032` Biometric authentication MUST be used only as a local user-verification factor and MUST NOT replace backend authorization.
- `MOB-033` Biometric-protected actions SHOULD use platform cryptographic binding when higher assurance is required.
- `MOB-034` Session timeout, logout, token revocation, and device-loss scenarios MUST be defined.
- `MOB-035` Logout MUST clear sensitive local session material and cached protected data as required by the threat model.
- `MOB-036` TLS MUST be used for production network communication unless an explicitly approved exception exists.
- `MOB-037` Certificate validation MUST NOT be disabled in production builds.
- `MOB-038` Certificate pinning MAY be used for higher-risk systems but MUST include an operational rotation/recovery strategy.
- `MOB-039` Network security configuration MUST prevent unintended cleartext traffic in production.
- `MOB-040` Deep links, universal links, app links, intents, custom URL schemes, QR payloads, clipboard data, and external app inputs MUST be validated as untrusted input.
- `MOB-041` Custom URL schemes SHOULD NOT be used for sensitive flows when claimed HTTPS-based links are available.
- `MOB-042` Sensitive data MUST NOT be written to application logs, analytics, crash reports, or debug consoles.
- `MOB-043` Production logging MUST avoid tokens, credentials, full personal identifiers, and sensitive payloads.
- `MOB-044` Screens containing high-sensitivity data SHOULD apply platform controls against screenshots/screen recording where justified and supported.
- `MOB-045` Clipboard use for secrets SHOULD be avoided; when unavoidable, lifetime and exposure MUST be minimized.
- `MOB-046` Root/jailbreak detection MAY be used as a risk signal but MUST NOT be the sole security control.
- `MOB-047` Anti-tamper or runtime-integrity controls MUST be risk-based and MUST NOT create false confidence in client trustworthiness.
- `MOB-048` App attestation/device integrity services MAY strengthen risk decisions but backend authorization remains mandatory.
- `MOB-049` WebViews MUST be minimized, configured securely, and prevented from exposing unsafe JavaScript/native bridges.
- `MOB-050` File downloads and uploads MUST validate type, size, content expectations, destination, and server-side authorization.
- `MOB-051` Local files containing sensitive data MUST use appropriate OS data-protection/encryption controls.
- `MOB-052` Exported Android components, iOS URL handlers, app extensions, and inter-process interfaces MUST expose only the minimum required surface.
- `MOB-053` Mobile threat modeling MUST include lost/stolen devices, malicious apps, compromised OS, network interception, reverse engineering, replay, deep-link abuse, notification leakage, and local-data extraction.
- `MOB-054` Security testing SHOULD include applicable static, dependency, secret, runtime, API, and mobile-specific assessments.
- `MOB-055` Critical/high security findings MUST be remediated or formally risk-accepted before production release.

## Review Evidence

Threat model, authentication/session design, secure-storage design, network configuration, deep-link validation, SDK inventory, mobile security test results, and exception records.
