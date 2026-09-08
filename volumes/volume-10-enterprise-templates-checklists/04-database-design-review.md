# Database Design Review — Template

## Database Context
- Database technology / version:
- Workload type:
- Expected data volume and growth:
- Availability target:
- RPO / RTO:
- Data classification:

## Schema Review
- [ ] Tables / collections represent clear domain concepts.
- [ ] Primary keys are explicit and stable.
- [ ] Foreign keys / integrity constraints are defined where appropriate.
- [ ] Nullability and defaults are intentional.
- [ ] Data types fit domain and scale requirements.
- [ ] Unique constraints enforce business invariants.
- [ ] Naming conventions are consistent.
- [ ] Audit fields are intentional and standardized.
- [ ] Soft delete is used only when justified.

## Index Review
For each critical query record predicates, joins, sorting, expected cardinality, index, and execution-plan evidence.

| Query / Use Case | Filter / Join / Sort | Expected Volume | Index | Evidence |
|---|---|---|---|---|

- [ ] Indexes support actual access patterns.
- [ ] Duplicate / redundant indexes are avoided.
- [ ] Write amplification is considered.
- [ ] Large-table index creation / rebuild impact is planned.

## Transactions and Concurrency
- Transaction boundaries:
- Isolation requirements:
- Locking / contention risks:
- Idempotency requirements:
- Deadlock handling:

## Security
- [ ] Application uses least-privilege DB identity.
- [ ] Administrative credentials are separate.
- [ ] Secrets are externalized.
- [ ] Encryption in transit is configured where required.
- [ ] Sensitive data protection is documented.
- [ ] Direct production access is controlled and audited.

## Lifecycle
- Migration strategy:
- Backward compatibility:
- Rollback / roll-forward strategy:
- Retention:
- Archiving:
- Backup:
- Restore test evidence:

## Decision
Approved / Approved with conditions / Rejected pending remediation.
