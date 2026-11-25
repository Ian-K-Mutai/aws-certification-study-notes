# Service comparisons

| Decision | Choose according to |
| --- | --- |
| Security group or network ACL | Stateful interface filtering versus stateless subnet filtering. Trace reply traffic through the ACL. |
| EBS, EFS or S3 | Block device, shared NFS directory or object API. Assess application interface before performance. |
| RDS Multi-AZ or read replica | Failover requirements versus read capacity and tolerance for replication lag. Check the deployment type for reader support. |
| CloudFront or Global Accelerator | Cacheable content and HTTP edge features versus static anycast IP addresses and routing to healthy endpoints. |
| Kinesis Data Streams or Firehose | Replay and independent consumers versus buffered managed delivery to a destination. |

[Networking fundamentals](../../shared/networking/README.md) · [Performance notes](../03-high-performing-architectures/README.md)
