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
