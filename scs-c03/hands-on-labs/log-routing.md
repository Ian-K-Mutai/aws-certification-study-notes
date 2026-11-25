# Alert routing exercise

Use a fictional CloudTrail record and EventBridge event pattern. This exercise needs no AWS account.

```json
{
  "source": "aws.ec2",
  "detail-type": "AWS API Call via CloudTrail",
  "detail": {
    "eventSource": "ec2.amazonaws.com",
    "eventName": "CreateTags"
  }
}
```

1. Write an event pattern that matches the source, detail type and event name. EventBridge patterns express accepted scalar values as arrays.
2. Make two copies of the record. In one, change the event name to `DescribeInstances`. In the other, leave the event unchanged and assume the target refuses delivery for permission reasons.
3. Explain why the first change should result in no match and why the second can produce a match without a notification.
4. Draw which metrics or logs would help distinguish absent source events, failed matches and failed target invocations.

[EventBridge event patterns](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-event-patterns.html) · [Detection notes](../01-detection/README.md)
