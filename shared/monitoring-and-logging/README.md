# Monitoring and logging

CloudWatch metrics describe measurements over time. CloudWatch Logs holds application and service log records. CloudTrail records AWS API and other supported account activity. AWS Config tracks supported resource configuration and evaluates rules against those resources. Use the telemetry source that answers the investigation question. A configuration timeline can show when a bucket changed, while CloudTrail may identify the principal and API request.

Centralise logs in a dedicated account where appropriate. Scope collection by account, Region and event type, define retention and access, and enable encryption where required. Test delivery and alert routing. A quiet dashboard can indicate either normal operation or missing telemetry. Confirm events at the source before debugging filters and downstream destinations.

[CloudTrail user guide](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html) · [AWS Config developer guide](https://docs.aws.amazon.com/config/latest/developerguide/WhatIsConfig.html)
