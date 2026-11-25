# Cost-optimised architectures

<a id="task-4-1"></a>

## 4.1 Storage costs

Model S3 storage, request, retrieval and minimum-duration charges against retention and access patterns. Lifecycle transitions can save money for long-lived cold objects but incur costs for short-lived or frequently retrieved data. For EBS, right-size capacity and provisioned performance, and review snapshots and detached volumes.

Model a monthly request and retrieval profile before changing class. [Cost optimisation pillar](https://docs.aws.amazon.com/wellarchitected/latest/cost-optimization-pillar/)

<a id="task-4-2"></a>

## 4.2 Compute costs

Right-size first and schedule environments to match demand. Compare On-Demand for uncertain usage, Savings Plans or applicable reservation discounts for a sustained baseline, and Spot for interruption-tolerant work. Diversify suitable Spot capacity and design workers to resume from checkpoints or retry safely.

Capacity assurance is a separate requirement from a pricing discount. Check utilisation and coverage before increasing a commitment. [Cost optimisation pillar](https://docs.aws.amazon.com/wellarchitected/latest/cost-optimization-pillar/)

<a id="task-4-3"></a>

## 4.3 Database costs

A steadily used relational database may benefit from a compatible commitment, while a variable workload warrants comparison with elastic capacity options. Evaluate Aurora storage and I/O billing against actual I/O patterns. For DynamoDB, compare on-demand and provisioned capacity using measured demand and account for indexes, backups and replication.

Compare total cost with the same throughput, availability and recovery objectives. Include cache cost and expected hit rate when considering a cache. [Cost optimisation pillar](https://docs.aws.amazon.com/wellarchitected/latest/cost-optimization-pillar/)

<a id="task-4-4"></a>

## 4.4 Network costs

Draw the data path and label the account, Region and Availability Zone at each hop. Include NAT processing, interface endpoint charges, inter-AZ or inter-Region transfer where applicable, and internet egress. A gateway endpoint can remove NAT processing from eligible S3 or DynamoDB traffic. Caching can reduce origin requests and transfer when responses are reusable.

Compare zonal and regional NAT designs before costing a private subnet topology. Model realistic traffic paths alongside availability objectives. [VPC traffic and connectivity](../../shared/networking/README.md)

[Official exam domain guide](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03-domain4.html)
