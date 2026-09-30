# Interview Scenarios

## DMS / CDC
1. Full Load is 100% but CDC latency is increasing. What do you check?
2. Source latency is low but target latency is high. Where is the likely bottleneck?
3. DMS task is successful but target data is incorrect. What next?
4. DMS storage keeps increasing. What are the possible causes?

## Validation
5. Why is COUNT(*) not enough?
6. How do you validate financial totals?
7. How do you detect orphan foreign keys?
8. How do you validate a migration with millions of rows?

## Performance
9. Target queries are slower after migration. How do you investigate?
10. When would you scale the DMS replication instance?
11. How do indexes affect migration and CDC apply performance?

## Cutover / rollback
12. What are your GO/NO-GO criteria?
13. What is your rollback strategy after writes have begun on the target?
14. How do you perform a low-downtime cutover?

## HA / DR
15. Difference between RDS Multi-AZ, read replica and DMS Multi-AZ?
16. How do you test failover?
17. What do RPO and RTO mean in this project?
