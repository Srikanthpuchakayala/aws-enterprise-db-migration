# Enterprise Database Migration, CDC Replication, HA & Cutover on AWS

Hands-on enterprise-style migration lab covering assessment, AWS architecture, secure networking, schema/data migration, AWS DMS, CDC replication, validation, performance troubleshooting, cutover, rollback, HA/DR, monitoring, automation, and operational documentation.

## Project scope

### Primary hands-on migration
- Source: self-managed MySQL on Amazon EC2 (on-premises simulation)
- Target: Amazon RDS for MySQL
- Region: ap-southeast-2 (Sydney)
- Migration mode: Full Load + CDC
- Target HA: RDS Multi-AZ
- Migration platform: AWS DMS

### Heterogeneous migration module
- Source: Oracle / SQL Server concepts and lab where available
- Target: PostgreSQL
- Tooling: AWS DMS Schema Conversion / SCT concepts
- Focus: data type mapping, stored procedure/function conversion, remediation and validation

## Lifecycle

1. Business requirements and migration success criteria
2. Source discovery and assessment
3. Migration strategy and downtime/RPO/RTO definition
4. AWS target architecture
5. VPC, subnets, routing and security
6. Source database build and workload simulation
7. RDS target build and HA
8. DMS replication infrastructure
9. Endpoints and connectivity tests
10. Schema/object preparation
11. Full Load
12. CDC replication
13. Source-target reconciliation
14. Data integrity / checksum validation
15. CDC latency and bottleneck analysis
16. Performance testing and tuning
17. Cutover
18. Rollback drill
19. RDS HA/failover test
20. DMS HA review/test
21. CloudWatch monitoring and alerting
22. Incident/RCA exercises
23. Terraform / automation
24. Final documentation and cleanup

## Evidence standard

Every phase must record:
- Objective
- Procedure
- Commands / console actions
- Expected result
- Actual result
- Validation evidence
- Failure scenarios
- Troubleshooting / RCA
- Final status

## Honesty rule

This repository documents a hands-on lab. It must not represent lab work as production customer experience or invent production volumes, incidents, downtime or business outcomes.
