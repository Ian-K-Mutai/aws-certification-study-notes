# Data protection

<a id="task-5-1"></a>

## 5.1 Data in transit

Inventory client-to-edge, edge-to-origin and service-to-service connections. Use ACM certificates for compatible managed endpoints and plan certificate validation and renewal. A certificate deployed to CloudFront for viewer HTTPS must be in US East (N. Virginia). Evaluate private trust roots and mutual TLS when the application needs authenticated clients.

Check the certificate name, chain, TLS policy and termination point separately. [CloudFront certificate requirements](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/cnames-and-https-requirements.html)

<a id="task-5-2"></a>

## 5.2 Data at rest

Use encryption and key controls appropriate to a workload's ownership, audit and recovery requirements. An S3 bucket policy can enforce specific encryption requirements, and a KMS key policy governs use of the key. For cross-account encrypted data, assess access at both layers and plan for key use during restore.

Use explicit separation of key administrators and key users as a design input. [Encryption and key management](../../shared/encryption/README.md)

<a id="task-5-3"></a>

## 5.3 Secrets and key material

Use Secrets Manager when a secret requires lifecycle management and rotation. For a rotation function, ensure connectivity to the target service and the secrets endpoint, scope access to the relevant secret and key, and test consumers across the credential transition. Evaluate CloudHSM when the organisation requires greater control of an HSM-backed deployment.

Distinguish rotating a database credential from rotating KMS key material. Each operation affects a different part of the dependency chain. [Secrets Manager rotation](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html)

[Official exam domain guide](https://docs.aws.amazon.com/aws-certification/latest/security-specialty-03/security-specialty-03-domain5.html)
