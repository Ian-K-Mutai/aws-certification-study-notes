# Disaster recovery

Recovery time objective (RTO) is the maximum acceptable restoration time. Recovery point objective (RPO) describes the maximum acceptable period of data loss. Set objectives for the whole workload, including dependencies such as DNS, secrets, encryption keys and external systems.

Backup and restore usually has the lowest steady-state infrastructure cost. Pilot light keeps essential data or resources ready, while warm standby runs a scaled-down functional environment. Multi-site active/active serves traffic in multiple locations and shifts complexity into routing, data consistency and operational coordination.

Test restoring data and switching traffic. Include the capacity required after failover and a plan for failing back. A replicated deletion or corruption can affect both sites, so retain independent recovery points.

[Reliability pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/)
