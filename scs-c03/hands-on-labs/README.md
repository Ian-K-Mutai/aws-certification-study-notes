# Incident triage tabletop

Use a fictional account and the following simulated evidence. This exercise needs no AWS resources or privileges.

| Time UTC | Evidence |
| --- | --- |
| 09:13 | CloudTrail shows a sensitive configuration change by a role session |
| 09:14 | A detection service emits a finding for the same account |
| 09:17 | An analyst receives the alert |

1. Assign an incident lead and an evidence custodian. Record the account, Region, role session and time range.
2. Identify what you would preserve, where you would store it and which permissions would protect the copy.
3. Propose a reversible containment decision and describe its operational impact and approval path.
4. Define the evidence needed to conclude recovery and identify one telemetry improvement.

The exercise is complete when someone who did not participate can reconstruct the timeline and explain each decision. [Incident response notes](../02-incident-response/README.md)

- [Alert routing exercise](log-routing.md)
