# AWS Migration Network Design

## Project

Enterprise Database Migration, CDC Replication, HA, Validation and Cutover on AWS

## AWS Region

ap-southeast-2 (Sydney)

## VPC

| Resource | Design |
|---|---|
| VPC Name | migration-lab-vpc |
| CIDR | 10.20.0.0/16 |
| DNS Resolution | Enabled |
| DNS Hostnames | Enabled |

## Availability Zones

- ap-southeast-2a
- ap-southeast-2b

## Subnets

| Subnet | CIDR | AZ | Intended Use |
|---|---|---|---|
| migration-public-a | 10.20.1.0/24 | ap-southeast-2a | Source EC2 / controlled administration |
| migration-private-a | 10.20.11.0/24 | ap-southeast-2a | RDS / DMS |
| migration-private-b | 10.20.12.0/24 | ap-southeast-2b | RDS / DMS |

## Gateways

Internet Gateway:
- Required for public subnet internet routing
- No NAT Gateway in the initial lab to control cost

## Routing

Public route table:
- 10.20.0.0/16 → local
- 0.0.0.0/0 → Internet Gateway

Private route tables:
- 10.20.0.0/16 → local

## Security Principles

- No database port exposed to 0.0.0.0/0
- Database access controlled by security groups
- RDS placed in private subnets
- DMS connectivity restricted to required database ports
- Administrative access restricted to approved source
- No credentials or secrets stored in Git

## Production Equivalent

In a production environment, the self-managed source would normally be an on-premises network connected to AWS through approved private connectivity such as VPN or Direct Connect rather than simply exposing the source database to the public internet.

This lab uses EC2 to simulate the source environment.

## Validation

Before proceeding to database deployment:

- [ ] VPC created
- [ ] Two AZs confirmed
- [ ] Three subnets created
- [ ] Public route validated
- [ ] Private routes validated
- [ ] Internet Gateway attached
- [ ] No unintended public database access
- [ ] Architecture evidence captured



## Deployed Resource IDs

| Resource | ID |
|---|---|
| VPC | vpc-0bab9fddf9954abcf |
| Public Subnet A |subnet-0064f04d4fe4430d6 |
| Public Subnet B | subnet-06a888ee433b9abef |
| Private Subnet A | subnet-0d211e7f2dc9f93eb |
| Private Subnet B | subnet-0a4c67beb83a88521 |
| Internet Gateway | igw-041f9598defa6f10a |
| Public Route Tabel | rtb-0edce5bfaff707fa4 | 
| Private Route Table |rtb-03e4b18414c0b80d3 |



## Deployed Resource IDs

| Resource | ID |
|---|---|
| VPC | vpc-0bab9fddf9954abcf |
| Public Subnet AZ-A | subnet-0064f04d4fe4430d6 |
| Public Subnet AZ-B | subnet-06a888ee433b9abef |
| Private Subnet AZ-A | subnet-0d211e7f2dc9f93eb |
| Private Subnet AZ-B | subnet-0a4c67beb83a88521 |
| Internet Gateway | igw-041f9598defa6f10a |
| Public Route Table | rtb-0edce5bfaff707fa4 |
| Private Route Table AZ-A | rtb-03e4b18414c0b80d3 |
| Private Route Table AZ-B | rtb-0ab1a184865979ef4 |


## Actual Subnet Mapping

| Subnet | CIDR | AZ | Role |
|---|---|---|---|
| subnet-0064f04d4fe4430d6 | 10.20.1.0/24 | ap-southeast-2a | Public / Source EC2 |
| subnet-06a888ee433b9abef | 10.20.2.0/24 | ap-southeast-2b | Public / Reserved |
| subnet-0d211e7f2dc9f93eb | 10.20.11.0/24 | ap-southeast-2a | Private / RDS + DMS |
| subnet-0a4c67beb83a88521 | 10.20.12.0/24 | ap-southeast-2b | Private / RDS + DMS |
