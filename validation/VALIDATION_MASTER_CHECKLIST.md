# Post-Migration Validation Master Checklist

## Data Completeness
- [ ] Row counts
- [ ] Table-level counts
- [ ] Aggregate checks (SUM/MIN/MAX/COUNT)
- [ ] Critical-record checks

## Data Integrity
- [ ] Primary-key uniqueness
- [ ] NULL constraints
- [ ] Foreign-key integrity
- [ ] Orphan-record checks
- [ ] Duplicate checks
- [ ] Data-type/precision checks

## Reconciliation
- [ ] DMS validation
- [ ] Deterministic row hash/checksum
- [ ] Source-target reconciliation report

## Application
- [ ] Connectivity
- [ ] Read operations
- [ ] Write operations
- [ ] Update/delete operations
- [ ] Critical transactions

## Performance
- [ ] Query latency baseline
- [ ] EXPLAIN / execution plans
- [ ] Index usage
- [ ] CPU
- [ ] I/O
- [ ] Connections

## CDC
- [ ] Source latency
- [ ] Target latency
- [ ] CDC backlog
- [ ] Critical change verification

## HA / DR
- [ ] RDS failover test
- [ ] Application reconnect test
- [ ] Recovery time recorded

## Final Sign-Off
- [ ] GO / NO-GO decision recorded



# Migration Validation Master Checklist

## A. Pre-Migration

- [ ] Source inventory completed
- [ ] Database size recorded
- [ ] Object inventory completed
- [ ] Workload baseline captured
- [ ] Dependencies identified
- [ ] Backup/recovery verified
- [ ] Migration strategy approved

## B. Connectivity

- [ ] Source endpoint connectivity tested
- [ ] Target endpoint connectivity tested
- [ ] Security groups verified
- [ ] Network routing verified
- [ ] TLS/encryption requirements reviewed

## C. Full Load

- [ ] DMS task started
- [ ] Tables loaded successfully
- [ ] Failed tables reviewed
- [ ] Table statistics reviewed
- [ ] Row counts compared

## D. CDC

- [ ] CDC started
- [ ] INSERT replicated
- [ ] UPDATE replicated
- [ ] DELETE replicated
- [ ] Source CDC latency monitored
- [ ] Target CDC latency monitored
- [ ] CDC backlog investigated when applicable

## E. Data Integrity

- [ ] Row counts reconciled
- [ ] SUM/aggregate values reconciled
- [ ] Critical records validated
- [ ] Duplicate records checked
- [ ] NULL constraints checked
- [ ] Primary keys checked
- [ ] Foreign keys checked
- [ ] Orphan records checked
- [ ] Data types checked
- [ ] Precision/scale checked
- [ ] Checksum/hash reconciliation completed where appropriate

## F. Application

- [ ] Application connectivity tested
- [ ] SELECT workflow tested
- [ ] INSERT workflow tested
- [ ] UPDATE workflow tested
- [ ] DELETE workflow tested
- [ ] Transaction workflow tested
- [ ] Critical business workflow tested

## G. Performance

- [ ] Query baseline captured
- [ ] Execution plans reviewed
- [ ] Indexes verified
- [ ] CPU reviewed
- [ ] I/O reviewed
- [ ] Connections reviewed
- [ ] Locking reviewed
- [ ] Slow queries reviewed

## H. Cutover

- [ ] Go/No-Go review completed
- [ ] Application writes stopped
- [ ] CDC backlog drained
- [ ] Final reconciliation completed
- [ ] Application switched to target
- [ ] Smoke testing completed
- [ ] Monitoring confirmed

## I. HA / DR

- [ ] RDS Multi-AZ verified
- [ ] RDS failover tested
- [ ] Application reconnection verified
- [ ] Recovery time measured
- [ ] DMS HA behavior reviewed

## J. Rollback

- [ ] Rollback criteria documented
- [ ] Rollback procedure documented
- [ ] Post-cutover write handling reviewed
- [ ] Rollback drill completed

## K. Final

- [ ] Business validation approved
- [ ] Migration report completed
- [ ] Lessons learned documented
- [ ] Runbooks completed
- [ ] AWS resources reviewed
- [ ] Lab cleanup completed
