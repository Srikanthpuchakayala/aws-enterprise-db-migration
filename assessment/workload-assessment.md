# Source Workload Assessment

## Purpose

Understand the source workload before selecting the migration approach and DMS replication capacity.

## Metrics

| Metric | Baseline | Peak | Status |
|---|---:|---:|---|
| Database Size | TBD | TBD | Pending |
| TPS | TBD | TBD | Pending |
| Queries/sec | TBD | TBD | Pending |
| CPU | TBD | TBD | Pending |
| Memory | TBD | TBD | Pending |
| Disk I/O | TBD | TBD | Pending |
| Network Throughput | TBD | TBD | Pending |
| Active Connections | TBD | TBD | Pending |
| Long Transactions | TBD | TBD | Pending |
| Largest Transaction | TBD | TBD | Pending |

## Performance Baseline

Capture:

- Top SQL statements
- Slow queries
- Missing indexes
- Full table scans
- Lock waits
- Long-running transactions
- Connection peaks
- Transaction volume

## Migration Impact

Assess:

- Whether source workload can tolerate DMS extraction
- Whether CDC can keep up with write volume
- Whether migration should run during off-peak hours
- Whether source throttling is required
- Whether target capacity is sufficient

## Findings

Pending source implementation and measurement.
