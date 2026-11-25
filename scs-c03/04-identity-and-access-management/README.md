# Identity and access management

<a id="task-4-1"></a>

## 4.1 Authentication strategies

Use IAM Identity Center with the workforce identity source and assign permission sets to groups in target accounts. For customer-facing applications, use Cognito user pools for user authentication and consider identity pools when the application needs temporary AWS credentials for direct access to resources. Workload roles avoid embedding permanent credentials.

Diagnose federation from issuer, audience, trust and attribute mapping through to role assignment. Treat session duration and revocation capabilities as part of the design. [IAM and federated access](../../shared/identity-and-access-management/README.md)

<a id="task-4-2"></a>

## 4.2 Authorisation strategies

When a cross-account role can list a bucket but cannot read an encrypted object, check the object action and ARN as well as bucket policy, organisation controls and KMS authorisation. Apply endpoint-policy conditions at the relevant VPC endpoint and evaluate them in addition to service permissions. Use IAM Access Analyzer findings to review unintended access.

Map the caller and resource first. Changing an identity policy cannot override an applicable explicit deny. [IAM and federated access](../../shared/identity-and-access-management/README.md)

[Official exam domain guide](https://docs.aws.amazon.com/aws-certification/latest/security-specialty-03/security-specialty-03-domain4.html)
