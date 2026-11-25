# IAM and federated access

Authentication identifies the caller. Authorisation evaluates the action, resource and request context. For a role, the trust policy defines who may assume it. The permissions attached to the role determine what the resulting session may do. AWS STS issues temporary credentials after successful role assumption. Use IAM Identity Center for workforce access across accounts and workload roles for applications running on AWS.

Start an access review with the caller ARN, action, resource ARN, account, Region and relevant request conditions. Within an account, identity and resource policies can grant access. Explicit denies take precedence. Permissions boundaries and session policies can limit the permissions available, and AWS Organizations service control policies (SCPs) can limit permissions in member accounts. An SCP provides a ceiling on permissions. Resource-policy behaviour depends on whether the grant names a role ARN or a role session ARN, so consult the evaluation rules when diagnosing exceptions.

For cross-account role assumption, check both the source principal's permission to call STS and the target role's trust policy. Then evaluate the role session's permissions on the destination resource. A cross-account S3 read may also require a bucket policy and permission to decrypt with the relevant KMS key.

[Policy evaluation logic](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic.html)
