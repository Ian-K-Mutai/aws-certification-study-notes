# High-performing architectures

<a id="task-3-1"></a>

## 3.1 Storage performance

Match the storage interface to the workload: S3 for objects, EBS for attached block storage and EFS for shared NFS access. An application that requires a shared POSIX directory across instances has different semantics from one that reads media via object URLs. For EBS, compare volume IOPS, throughput, I/O size and the instance's EBS capacity. gp3 allows independent performance provisioning within its limits. gp2 scales baseline IOPS with volume size up to 16,000 IOPS.

Use observed throughput and latency together. A sequential transfer and a small random I/O workload can hit different limits. [EBS general purpose SSD](https://docs.aws.amazon.com/ebs/latest/userguide/general-purpose.html)

<a id="task-3-2"></a>

## 3.2 Elastic compute

For a stateless site, use an ALB and an Auto Scaling group, and pick a metric that rises with per-instance work. A containerised service may benefit from ECS with Fargate when the team wants to manage tasks without managing container instances. Lambda suits event-driven execution within its runtime constraints. Validate concurrency, warm-up latency, memory and downstream capacity before scaling the front end.

For HPC, determine whether the jobs are independent or exchange data frequently. The second case can make placement and low-latency networking central. [Performance efficiency pillar](https://docs.aws.amazon.com/wellarchitected/latest/performance-efficiency-pillar/)

<a id="task-3-3"></a>

## 3.3 Database performance

Choose a database from access patterns and consistency requirements. A relational workload can use indexes and read replicas to reduce load on the writer, subject to replica lag. DynamoDB needs a partition key that distributes traffic and supports the required queries. ElastiCache absorbs repeated reads where the application can manage expiry, invalidation and cache misses.

Measure tail latency and the behaviour during cache loss. Evaluate RDS, Aurora and DynamoDB against the data model and read/write pattern. [Performance efficiency pillar](https://docs.aws.amazon.com/wellarchitected/latest/performance-efficiency-pillar/)

<a id="task-3-4"></a>

## 3.4 Network performance

CloudFront caches cacheable responses close to users. Inspect the cache key before forwarding high-cardinality request attributes. Global Accelerator uses static anycast IP addresses and routes supported traffic over the AWS network to healthy endpoints. For private connectivity, assess throughput, path redundancy and latency across VPN and Direct Connect options.

Measure viewer-to-edge and edge-to-origin behaviour separately. [VPC traffic and connectivity](../../shared/networking/README.md)

<a id="task-3-5"></a>

## 3.5 Ingestion and transformation

For replayable streaming with independent consumers, use Kinesis Data Streams and plan retention and throughput. For managed delivery into S3, evaluate Amazon Data Firehose and its buffering and transformation features. Use Glue to catalogue and transform stored datasets, then make partition choices that match common analytical queries.

Start with latency, replay and destination requirements. Fine-grained processing before storage and batch transformation after storage serve different needs. [Amazon Data Firehose](https://docs.aws.amazon.com/firehose/latest/dev/what-is-this-service.html)

[Official exam domain guide](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03-domain3.html)
