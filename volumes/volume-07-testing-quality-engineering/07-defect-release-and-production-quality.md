# Defect, Release, and Production Quality

## Mandatory Rules

- **TST-146** — Defects must record impact, severity, priority, affected versions, evidence, reproducibility, and ownership.
- **TST-147** — Severity must reflect user, business, security, data, compliance, and operational impact.
- **TST-148** — Critical and high-severity defects require root-cause analysis and verified corrective action.
- **TST-149** — Defect fixes must include regression tests that reproduce the original failure where practical.
- **TST-150** — Duplicate and rejected defects must retain rationale and traceability.
- **TST-151** — Release readiness must evaluate test evidence, defects, security findings, migrations, rollback, monitoring, and support readiness.
- **TST-152** — Known defects accepted for release must have explicit risk acceptance and customer-impact mitigation.
- **TST-153** — Production deployment must be validated through automated or scripted smoke tests.
- **TST-154** — Canary or phased releases must define success indicators, observation periods, and abort thresholds.
- **TST-155** — Rollback procedures must be tested for application, configuration, schema, and data implications.
- **TST-156** — Post-release validation must verify critical business transactions and security controls.
- **TST-157** — Production monitoring must detect elevated errors, latency, saturation, business failures, and security anomalies.
- **TST-158** — Synthetic monitoring must not create unsafe data, uncontrolled load, or misleading business records.
- **TST-159** — Escaped defects must be analyzed for missing prevention, detection, and response controls.
- **TST-160** — Release quality decisions and evidence must be retained and auditable.
- **TST-161** — Emergency releases must preserve minimum testing, approval, monitoring, and post-implementation review.
- **TST-162** — Production verification must not rely only on infrastructure health when user workflows may still fail.
- **TST-163** — Quality ownership continues after deployment through incident response, telemetry review, and corrective action.
- **TST-164** — Release success criteria must include business and user outcomes, not only technical deployment completion.
- **TST-165** — Repeated defect patterns must trigger systemic improvement rather than isolated fixes.