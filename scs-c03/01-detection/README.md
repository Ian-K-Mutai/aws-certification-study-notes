# Detection

<a id="task-1-1"></a>

## 1.1 Monitoring and alerts

Delegate administration of supported security services to a security account. Identify which accounts and Regions must emit findings and how new accounts enrol. Use GuardDuty for supported threat detections, Security Hub for supported findings and posture workflows, and Macie for supported sensitive-data discovery in S3. Route actionable alerts by severity, ownership and environment.

Validate an end-to-end finding, including event arrival, routing, notification and acknowledgement. [Monitoring and logging](../../shared/monitoring-and-logging/README.md)

<a id="task-1-2"></a>

## 1.2 Logging architecture

Define management and data event requirements separately. Use an organisation trail and central delivery where appropriate, and restrict access to the log archive. Retention depends on investigation and compliance needs. Use CloudWatch Logs for application logs and evaluate Security Lake for supported security datasets. CloudTrail Lake closed to new customers on 31 May 2026.

Test that intended accounts and Regions actually deliver events. [CloudTrail Lake availability](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-lake-service-availability-change.html)

<a id="task-1-3"></a>

## 1.3 Telemetry troubleshooting

For a missing alert, follow the event from producer to destination. Verify collection is enabled and check event selection, service role permissions, destination resources and encryption permissions. For a CloudWatch agent, check configuration, agent status and connectivity to the regional endpoint. For EventBridge, inspect the event pattern, target permissions and delivery metrics.

Use a known benign event to prove each hop independently. [Monitoring and logging](../../shared/monitoring-and-logging/README.md)

[Official exam domain guide](https://docs.aws.amazon.com/aws-certification/latest/security-specialty-03/security-specialty-03-domain1.html)
