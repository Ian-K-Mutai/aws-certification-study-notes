# Secure architectures

<a id="task-1-1"></a>

## 1.1 Secure resource access

A team needs to deploy to several accounts. Assign workforce access through IAM Identity Center and use a deployment role in each target account. Scope its trust to the approved deployment identity and its permissions to deployment resources. For EC2 applications, attach an instance profile and use the AWS SDK credential provider chain. Separate the deployment identity from the runtime identity so that compromise of the workload does not grant deployment authority.

The request must pass both the relevant trust and authorisation checks. Work through the [IAM evaluation model](../../shared/identity-and-access-management/README.md) before broadening permissions.

<a id="task-1-2"></a>

## 1.2 Secure workloads

Put an internet-facing ALB in public subnets and application targets in private subnets. Allow application ingress from the ALB security group and database ingress from the application security group. Use AWS WAF for supported HTTP endpoints when application-layer filtering is required. Private service endpoints can remove the need for workloads to reach public service endpoints through NAT.

Trace each hop using the [VPC connectivity notes](../../shared/networking/README.md). Design the management path separately from user traffic.

<a id="task-1-3"></a>

## 1.3 Protect data

For private downloads, use an S3 bucket origin behind CloudFront and grant the distribution access through origin access control. Keep S3 Block Public Access enabled where the delivery design permits it. With SSE-KMS, authorise the required key operations and account for key-policy dependencies when configuring replication or sharing. Use versioning when the recovery design needs prior object versions.

Treat public access, encryption and recovery as independent controls. [Encryption and key management](../../shared/encryption/README.md) · [CloudFront origin access](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html)

[Official exam domain guide](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03-domain1.html)
