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



# Enterprise Database Migration Project Charter

## 1. Project Name

Enterprise Database Migration, CDC Replication, HA, Validation and Cutover on AWS

## 2. Project Objective

Migrate a self-managed MySQL database to Amazon RDS for MySQL using AWS Database Migration Service (DMS), while maintaining data consistency, minimizing application downtime, implementing high availability, validating the migrated data, and establishing rollback and monitoring procedures.

## 3. Primary Migration Architecture

Source:
- Self-managed MySQL database hosted on Amazon EC2

Migration:
- AWS Database Migration Service
- Full Load + Change Data Capture (CDC)

Target:
- Amazon RDS for MySQL
- Multi-AZ deployment for high availability

Region:
- ap-southeast-2 (Sydney)

## 4. Migration Objectives

- Assess the source database and workload
- Design secure AWS networking
- Establish source and target connectivity
- Configure DMS replication
- Execute full-load migration
- Enable and monitor CDC
- Validate migrated data
- Perform source-target reconciliation
- Perform checksum/hash validation where appropriate
- Monitor CDC latency
- Diagnose migration bottlenecks
- Test target database performance
- Execute controlled cutover
- Define and test rollback procedures
- Test RDS Multi-AZ failover
- Test DMS high-availability behavior
- Configure monitoring and operational procedures
- Document lessons learned and troubleshooting procedures

## 5. Migration Success Criteria

Migration will not be considered successful merely because the DMS task reports a successful status.

Success requires:

- Source and target row counts reconciled
- Critical business aggregates reconciled
- Primary-key integrity verified
- Foreign-key integrity verified
- No unresolved critical data mismatches
- CDC caught up within the agreed cutover threshold
- Application smoke tests successful
- Critical queries perform within the agreed baseline
- Security controls validated
- HA/failover test completed
- Rollback plan documented and tested

## 6. Lab Disclaimer

This repository documents a controlled hands-on migration lab.

It is not a claim of performing a production migration for a real customer.

Production-sized examples such as 500 GB databases, enterprise RPO/RTO targets, or regulated workloads may be discussed as interview scenarios unless actually reproduced in the lab.

## 7. Technical Scope

Included:
- AWS VPC
- Subnets
- Route tables
- Security groups
- IAM
- EC2
- MySQL
- Amazon RDS
- AWS DMS
- CloudWatch
- Backup and recovery concepts
- RDS Multi-AZ
- Migration validation
- Performance troubleshooting
- Cutover and rollback
- Terraform/IaC documentation

Future extension:
- Oracle to PostgreSQL
- SQL Server to PostgreSQL
- Schema Conversion/SCT remediation
- Heterogeneous stored procedure conversion

## 8. Project Operating Model

Every migration phase follows:

Objective
→ Prerequisites
→ Design
→ Procedure
→ Execution
→ Validation
→ Evidence
→ Failure Scenarios
→ Troubleshooting
→ RCA
→ Exit Criteria
→ Interview Explanation
