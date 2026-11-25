# Availability and recovery design exercise

This walkthrough uses a paper or digital diagram and incurs no AWS charges.

1. Draw two Availability Zones, an ALB, private application targets and a relational database with failover.
2. Mark how the targets obtain credentials and identify the security group allowed to connect to the database.
3. Cross out one zone. Trace the surviving request path and identify the remaining application capacity and the database recovery path.
4. Cross out the Region. Define an RTO and RPO and select a recovery strategy that also covers DNS, backups and encryption keys.

The exercise is complete when the diagram explains both failure scopes and records the capacity and recovery assumptions. [Resilience notes](../02-resilient-architectures/README.md)

- [Storage cost model](storage-cost-model.md)
