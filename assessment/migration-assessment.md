# Migration Assessment

## Source

Self-managed MySQL on EC2

## Target

Amazon RDS for MySQL

## Migration Type

Homogeneous database migration

## Proposed Method

AWS DMS Full Load + CDC

## Why Full Load + CDC

Full Load moves the existing dataset.

CDC captures ongoing INSERT, UPDATE and DELETE activity after and during the initial load.

This allows the target to remain synchronized while the source application continues operating.

## Alternative Approaches Considered

### 1. Full Load Only

Suitable when:
- Downtime is acceptable
- Application can be stopped
- Database is small

Not selected for the primary lab because we want to demonstrate low-downtime migration.

### 2. Backup and Restore

Potentially useful for:
- Large homogeneous migrations
- Engine-native migration

Not selected for the primary CDC lab because we need ongoing change replication.

### 3. AWS DMS Full Load + CDC

Selected because it allows:
- Initial data load
- Continuous change replication
- Controlled low-downtime cutover
- Migration monitoring

## Key Risks

- Source/DMS connectivity failure
- CDC latency
- Target performance bottleneck
- Missing or incompatible schema objects
- Data mismatch
- Large transactions
- Long-running transactions
- Network bottleneck
- Application connection problems
- Cutover failure

## Validation Strategy

- Row counts
- Aggregates
- Record-level checks
- PK validation
- FK validation
- NULL validation
- Duplicate detection
- Checksum/hash reconciliation
- DMS validation
- Application smoke tests
- Performance comparison

## Cutover Requirements

Before cutover:

- CDC healthy
- CDC backlog within agreed threshold
- Critical data reconciled
- Application test completed
- Rollback procedure ready
- Monitoring active
- Change approval completed

## Current Assessment Status

Architecture approved for hands-on lab.

Detailed measurements will be completed after source implementation.
