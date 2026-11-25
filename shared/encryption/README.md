# Encryption and key management

TLS protects data in transit between two endpoints. Identify every hop where TLS terminates, including load balancers and edge distributions. Protect the next hop separately when the threat model or compliance policy requires it.

Envelope encryption uses a data key for the payload and a longer-lived key to protect the data key. The encrypted data key can be stored alongside the encrypted payload. AWS KMS manages keys and authorisation for cryptographic operations. Check the key policy, the caller's permissions and applicable grants when an encrypted object is visible but cannot be read.

Choose a customer managed KMS key when the design needs control over key policy, grants or lifecycle. Plan recovery around the key as well as the data. Retaining encrypted backups while deleting the only usable key can render the backups unrecoverable. Rotation changes which key material protects new data and preserves the material required for existing ciphertext under the supported rotation lifecycle.

[Using IAM policies with AWS KMS](https://docs.aws.amazon.com/kms/latest/developerguide/iam-policies.html)
