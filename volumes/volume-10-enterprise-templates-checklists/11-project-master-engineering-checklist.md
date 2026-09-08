# Project Master Engineering Checklist

Use this as the final cross-volume gate. Detailed evidence SHOULD link to the applicable review or template.

## Governance & Architecture
- [ ] Ownership, scope, criticality, and data classification are defined.
- [ ] Architecture and deployment diagrams are current.
- [ ] Major decisions have ADRs.
- [ ] Dependencies, failure modes, and trust boundaries are known.

## Backend & Authorization
- [ ] API contracts and validation are defined.
- [ ] Authentication uses approved mechanisms.
- [ ] Authorization is enforced server-side at operation and resource level.
- [ ] Permissions/policies are configurable where business access changes; code does not depend on fixed business role names for authorization.
- [ ] Background jobs and integrations are idempotent where required.

## Frontend
- [ ] UI handles loading, empty, error, expired-session, and unauthorized states.
- [ ] Sensitive authorization decisions are not trusted to the client.
- [ ] Accessibility, responsiveness, localization, and browser/device requirements are tested.
- [ ] Frontend security and dependency controls pass.

## Database
- [ ] Schema integrity and naming reviewed.
- [ ] Critical queries and indexes reviewed with evidence.
- [ ] Transactions and concurrency behavior defined.
- [ ] Migrations are controlled and production-safe.
- [ ] Backup, restore, retention, and deletion are verified.

## Security
- [ ] Threat model completed.
- [ ] Least privilege applied end to end.
- [ ] Secrets / certificates have controlled storage and rotation.
- [ ] SAST, SCA, secret scanning, and applicable DAST passed.
- [ ] Critical/high findings are remediated or formally risk-accepted.
- [ ] Audit logging covers privileged and sensitive actions.

## Testing & Quality
- [ ] Requirements trace to acceptance tests.
- [ ] Unit / integration / API / E2E coverage matches risk.
- [ ] Negative, authorization, concurrency, and failure scenarios are tested.
- [ ] Performance / resilience tests are complete where applicable.
- [ ] UAT and regression gates pass.

## DevOps & Supply Chain
- [ ] Reproducible build and controlled CI/CD exist.
- [ ] Artifacts are immutable and traceable to source.
- [ ] Dependencies and images are scanned.
- [ ] Environments and configuration are separated.
- [ ] Deployment and rollback procedures are validated.

## Operations & SRE
- [ ] Service owner and support model are documented.
- [ ] SLI/SLO and critical dashboards exist where required.
- [ ] Alerts are actionable.
- [ ] Runbooks cover likely failures.
- [ ] Capacity and dependency risks are acceptable.
- [ ] RTO/RPO and recovery tests meet business needs.

## AI — When Applicable
- [ ] AI use case, model/provider, data, and risk are documented.
- [ ] Evaluation evidence meets acceptance criteria.
- [ ] Prompt injection, data leakage, and retrieval authorization are tested.
- [ ] Agents/tools have bounded permissions and human approval where required.
- [ ] Model/prompt/RAG changes are regression-tested.

## Release Gate
- [ ] Production Readiness Review approved.
- [ ] Change record / implementation plan complete.
- [ ] Rollback or roll-forward path exists.
- [ ] Monitoring is active before traffic is enabled.
- [ ] Known residual risks have named owners and expiry/review dates.

## Final Decision
**Approved / Approved with time-bound conditions / Rejected pending remediation**
