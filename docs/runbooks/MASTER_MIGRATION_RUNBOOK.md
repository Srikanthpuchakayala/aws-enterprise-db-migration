# Master Migration Runbook

## Phase 0 — Requirements
- [ ] Define database scope
- [ ] Define downtime window
- [ ] Define RPO/RTO
- [ ] Define validation criteria
- [ ] Define rollback criteria

## Phase 1 — Assessment
- [ ] Engine/version
- [ ] Database size
- [ ] Tables/objects
- [ ] PK/FK/index inventory
- [ ] Views/procedures/functions/triggers
- [ ] Workload/TPS/connections
- [ ] Application dependencies

## Phase 2 — Build AWS
- [ ] VPC
- [ ] Subnets in two AZs
- [ ] Route tables
- [ ] Security groups
- [ ] IAM
- [ ] KMS
- [ ] RDS subnet group
- [ ] RDS target

## Phase 3 — DMS
- [ ] Replication instance
- [ ] Source endpoint
- [ ] Target endpoint
- [ ] Endpoint connection tests
- [ ] Task configuration

## Phase 4 — Migration
- [ ] Schema preparation
- [ ] Full Load
- [ ] CDC
- [ ] Monitoring

## Phase 5 — Validation
- [ ] Row counts
- [ ] Aggregates
- [ ] NULL/duplicate checks
- [ ] PK/FK integrity
- [ ] Critical records
- [ ] Checksum/reconciliation
- [ ] DMS validation
- [ ] Application validation
- [ ] Performance validation

## Phase 6 — Cutover
- [ ] Change approval
- [ ] Backup confirmation
- [ ] CDC lag within threshold
- [ ] Freeze writes
- [ ] Drain CDC
- [ ] Final reconciliation
- [ ] Redirect application
- [ ] Smoke test

## Phase 7 — Post-cutover
- [ ] Monitor
- [ ] HA/failover test
- [ ] Close migration window
- [ ] Document lessons learned
- [ ] Cleanup resources
