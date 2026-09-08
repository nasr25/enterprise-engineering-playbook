# AI System Assessment — Template

## Use Case
- AI capability:
- Business owner:
- Technical owner:
- Intended users:
- Intended purpose:
- Prohibited uses:
- Risk classification:
- Human decision / approval points:

## Model / Provider
- Model / version:
- Hosting: on-premises / private / external provider
- Provider / license:
- Data residency:
- External network calls:
- Fallback:

## Data
- Training / tuning data:
- Retrieval sources:
- Data classification:
- Provenance:
- Retention:
- Personal / sensitive data:
- Authorization enforcement for retrieval:

## Evaluation
- Baseline:
- Acceptance metrics:
- Evaluation dataset:
- Error / hallucination analysis:
- Segment / fairness analysis where applicable:
- Adversarial / prompt-injection testing:
- Latency / capacity / cost:

## Generative AI / RAG
- [ ] System prompts are versioned.
- [ ] Untrusted content is separated from privileged instructions.
- [ ] Retrieved content respects caller authorization.
- [ ] Output consumed by software is schema-validated.
- [ ] Citations / grounding are evaluated where required.
- [ ] Regression evaluation covers model, prompt, retrieval, and tool changes.

## Agent / Tool Controls
- Tool allowlist:
- Agent identity / privileges:
- High-impact approval requirements:
- Iteration / cost limits:
- Audit logging:
- Human escalation:

## Security / Privacy
- Threat model:
- Data-exfiltration testing:
- Cross-user / cross-tenant isolation:
- Secret protection:
- Model / dependency provenance:
- Emergency disable mechanism:

## Production
- Observability:
- Drift / quality monitoring:
- Rollback:
- Incident runbook:
- Retraining / replacement criteria:

## Decision
Approved / Approved with conditions / Rejected pending remediation.
