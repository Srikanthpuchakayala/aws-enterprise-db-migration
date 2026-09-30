# Application and Dependency Assessment

## Purpose

Identify systems and database objects dependent on the source database.

## Application Dependencies

| Dependency | Type | Criticality | Migration Impact |
|---|---|---|---|
| Application | TBD | High | TBD |
| Reporting | TBD | Medium | TBD |
| ETL | TBD | Medium | TBD |
| Batch Jobs | TBD | Medium | TBD |
| BI | TBD | Medium | TBD |
| APIs | TBD | High | TBD |

## Database Dependencies

Assess:

- Tables
- Views
- Stored procedures
- Functions
- Triggers
- Foreign keys
- Scheduled jobs
- External connections
- Reporting queries
- ETL pipelines

## Application Cutover Dependencies

Document:

- Application connection string
- DNS/service discovery
- Connection pool behavior
- Credentials/secrets
- Maintenance window
- Application restart requirements
- Smoke tests
- Business validation

## Findings

Pending source and application simulation.
