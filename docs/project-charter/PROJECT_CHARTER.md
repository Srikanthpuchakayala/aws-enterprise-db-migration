# Project Charter

## Objective
Execute and document a controlled relational database migration to AWS with continuous CDC replication, data validation, HA, cutover and rollback procedures.

## Environment
- AWS Region: ap-southeast-2 (Sydney)
- Primary source: self-managed MySQL on EC2
- Target: Amazon RDS for MySQL

## Success criteria
- Source and target schemas are compatible
- Full load completes without unresolved critical errors
- CDC runs continuously and reaches agreed cutover threshold
- Row counts and business aggregates reconcile
- PK/FK and data-integrity checks pass
- Application smoke tests pass
- Target performance is within the agreed lab baseline
- Cutover and rollback procedures are tested
- RDS HA/failover behavior is verified
