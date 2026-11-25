# SAA-C03 decision checklist

| Signal in a scenario | Design question |
| --- | --- |
| Linux workers need the same mounted file system | Does the application require shared NFS semantics? |
| Relational reads dominate | Can replicas or a cache meet the workload's consistency requirements? |
| Requests exceed worker capacity in bursts | Can the caller accept asynchronous processing and retry safely? |
| A single zone can fail | Can remaining targets and dependencies meet the SLO? |
| Objects are cold but short-lived | Will minimum-duration or retrieval charges outweigh storage savings? |

[Exam coverage matrix](../exam-coverage-matrix.md)
