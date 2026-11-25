# Resilient architectures

<a id="task-2-1"></a>

## 2.1 Scale and decouple

Place a queue between an order API and workers when requests can be accepted before processing completes. Scale workers against backlog and processing time. Align visibility timeout with processing time, retry transient failures, and use a dead-letter queue for repeated failures. Store an idempotency key with the business transaction so that reprocessing a message does not repeat a charge.

Use SNS with separate subscriber queues for independent fan-out, and EventBridge when routing by event attributes or connecting supported event sources is central to the design. [Amazon SQS](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html)

<a id="task-2-2"></a>

## 2.2 Availability and fault tolerance

Distribute an ALB and Auto Scaling group across Availability Zones, keep session state outside individual instances and use health checks. Provision enough capacity to meet critical demand during a zone failure. For relational storage, distinguish the failover path of the selected RDS Multi-AZ deployment from the read-scaling path of replicas. Test connection retry behaviour during failover.

A Multi-AZ deployment and a regional disaster recovery plan address different failure scopes. Choose a [recovery strategy](../../shared/disaster-recovery/README.md) using RTO and RPO. [Reliability pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/)

[Official exam domain guide](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03-domain2.html)
