# Authentication Abuse, Rate Limiting, and Automated Traffic Protection

Rules `BE-145`–`BE-180`.

## Purpose

Protect authentication and other abuse-sensitive APIs against brute force, credential stuffing, password spraying, automated bots, denial-of-wallet/resource exhaustion, and distributed high-volume attempts without unnecessarily blocking legitimate users.

## Risk Model

Controls MUST be layered. A single IP limit, CAPTCHA, account lockout, or WAF rule is not sufficient by itself for high-risk authentication endpoints.

## Rate Limiting and Dimensions

- **BE-145** — Internet-facing and abuse-sensitive authentication endpoints MUST have explicit rate-limiting and automated-abuse controls.
- **BE-146** — Rate limits MUST be defined from risk, expected legitimate traffic, endpoint cost, and capacity rather than arbitrary defaults.
- **BE-147** — Authentication protection SHOULD evaluate multiple dimensions where applicable, including source IP/network, account identifier, device/client signal, session, endpoint, and global traffic.
- **BE-148** — Systems MUST NOT rely exclusively on source IP for account protection because legitimate users may share addresses and attackers may distribute traffic.
- **BE-149** — Per-account controls MUST resist password spraying and distributed attempts against one identity.
- **BE-150** — Per-IP/network controls SHOULD resist one source attacking many accounts while accounting for NAT, proxies, enterprise networks, and trusted intermediaries.
- **BE-151** — Global/service-level limits MUST protect backend capacity during broad attacks or traffic anomalies.
- **BE-152** — Expensive operations SHOULD have stricter cost-aware limits than inexpensive reads.
- **BE-153** — Rate-limit keys derived from user-controlled identifiers MUST be normalized consistently and protected against unbounded state creation.
- **BE-154** — Client IP extraction MUST trust only explicitly configured proxies/load balancers and MUST reject spoofable forwarding-header assumptions.
- **BE-155** — Limit windows, burst capacity, quotas, and reset behavior MUST be documented and testable.
- **BE-156** — Rate-limit responses SHOULD use HTTP 429 where semantically appropriate and SHOULD communicate safe retry behavior without leaking sensitive account state.

## Progressive Friction and Verification

- **BE-157** — Repeated suspicious failures SHOULD trigger progressive friction rather than an immediate permanent block.
- **BE-158** — Progressive delay/backoff SHOULD increase the cost of repeated automated attempts while remaining bounded and operationally safe.
- **BE-159** — CAPTCHA or equivalent bot challenges MAY be introduced adaptively when risk rises; they SHOULD NOT be the sole authentication control.
- **BE-160** — Higher-risk authentication attempts SHOULD support step-up verification such as MFA or another approved verification mechanism.
- **BE-161** — Risk signals MAY include velocity, failed-attempt patterns, device/client changes, network reputation, impossible behavior, or other approved signals; sensitive profiling requires privacy review.
- **BE-162** — Challenge decisions MUST fail safely and MUST NOT silently bypass required authentication or authorization.
- **BE-163** — Accessibility and legitimate-user recovery MUST be considered when CAPTCHA or additional challenges are used.

## Account Lockout and Enumeration Safety

- **BE-164** — Account lockout design MUST consider denial-of-service abuse in which an attacker intentionally locks a victim's account.
- **BE-165** — Permanent or long-duration lockout based only on remote failed attempts SHOULD be avoided unless business risk explicitly requires it.
- **BE-166** — Authentication responses SHOULD avoid revealing whether an account exists, is disabled, is locked, or uses a particular authentication factor unless disclosure is explicitly required.
- **BE-167** — Timing and response-shape differences SHOULD be reviewed for practical username/account enumeration risk.
- **BE-168** — Password-reset, OTP, verification-code, account-recovery, registration, invitation, and resend endpoints MUST receive equivalent abuse analysis rather than protecting login alone.

## Distributed Enforcement and Edge Protection

- **BE-169** — Multi-instance deployments MUST use coordinated/distributed enforcement for limits that require a shared view of attempts.
- **BE-170** — Shared rate-limit state MAY use Redis or another suitable centralized/distributed mechanism; the selected design MUST define atomicity, expiry, availability, and failure behavior.
- **BE-171** — Local in-memory counters MUST NOT be assumed to provide an effective global limit across multiple backend instances.
- **BE-172** — Internet-facing systems SHOULD reject clearly malicious or excessive traffic as early as practical using approved WAF, API gateway, reverse proxy, load balancer, CDN, or equivalent edge controls.
- **BE-173** — Edge protection MUST complement, not replace, application-level account and business-context controls.
- **BE-174** — Failure or unavailability of the shared limiter/challenge service MUST have an explicit fail-open/fail-closed decision based on endpoint risk and availability requirements.

## Observability, Privacy, and Testing

- **BE-175** — Systems MUST record security-relevant abuse events and metrics sufficient to investigate attack patterns without logging passwords, OTP values, access tokens, or unnecessary personal data.
- **BE-176** — Monitoring SHOULD expose failed/successful authentication rates, throttled requests, challenged requests, lockouts/delays, abnormal account/IP/device distributions, and limiter infrastructure health.
- **BE-177** — Alerts MUST be actionable and tuned to detect meaningful abuse without creating uncontrolled alert noise.
- **BE-178** — Automated tests MUST verify limits across relevant dimensions, boundary/reset behavior, concurrency, proxy/IP handling, progressive delays, challenge flows, enumeration resistance, and legitimate-user recovery.
- **BE-179** — Distributed deployments MUST test that limits remain effective when requests are spread across multiple application instances.
- **BE-180** — Production readiness for abuse-sensitive authentication MUST include documented thresholds/configuration ownership, monitoring, incident response, emergency tuning/disable procedures, and evidence that controls do not prevent expected legitimate traffic.

## Reference Control Flow

A typical high-risk login flow is:

`Edge filtering -> Global/service limit -> IP/network limit -> Account/device risk evaluation -> Authentication -> Progressive challenge/backoff when indicated -> MFA/step-up when required -> Session issuance`

The exact order may vary by architecture. Controls MUST avoid unnecessary expensive work before obviously abusive traffic is rejected.

## Review Evidence

Provide, where applicable:

- threat model for brute force, credential stuffing, password spraying, enumeration, bot traffic, and lockout abuse;
- documented rate-limit dimensions, thresholds, windows, burst behavior, and owners;
- WAF/gateway/reverse-proxy and application enforcement configuration;
- distributed limiter design and failure behavior;
- CAPTCHA/challenge and MFA/step-up decision logic;
- dashboards, alerts, and incident/runbook procedures;
- automated test evidence including multi-instance and legitimate-user scenarios.
