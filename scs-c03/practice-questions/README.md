# SCS-C03 practice questions

1. An organisation trail receives events from one account, but a matching alert never arrives. Which layers do you check?
2. A role can access a bucket but fails to read an SSE-KMS object. Which policy boundaries matter?
3. A critical finding identifies a possibly compromised instance. What should the response lead weigh before isolation?

## Answers

1. Confirm the source event is in scope, then check delivery, event pattern, target permissions and destination telemetry.
2. Confirm object-level S3 authorisation, the KMS key policy, caller permissions and any applicable policy ceilings or denies.
3. Assess the risk of further damage, evidence that might be lost, service impact and regulatory requirements. Record the authorisation and containment decision.
