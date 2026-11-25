# SCS-C03 control checklist

| Signal | First check |
| --- | --- |
| A role cannot be assumed | Caller permission, target trust and request conditions |
| S3 can list but reads fail | Object-level permission and KMS authorisation |
| Logs are missing centrally | Source collection, delivery permissions, encryption and destination scope |
| A private TLS connection fails | Certificate name, chain, trust root and termination point |
| Remediation repeats | Whether the underlying deployment restores the undesired configuration |

[Exam coverage matrix](../exam-coverage-matrix.md)
