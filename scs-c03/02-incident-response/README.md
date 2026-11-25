# Incident response

<a id="task-2-1"></a>

## 2.1 Plan and test incident response

Write a playbook that identifies the incident lead, account owners, evidence custodian and communications channels. Define the authority required for containment and recovery. Preconfigure access to investigation accounts and verify it during tabletop exercises. Test a lost credential scenario and record decision times, missing telemetry and permissions failures.

Define escalation and handover before the incident. A tabletop tests decisions and roles, while a technical exercise tests access, evidence collection and recovery. [AWS Security Incident Response guide](https://docs.aws.amazon.com/security-ir/latest/userguide/)

<a id="task-2-2"></a>

## 2.2 Respond to security events

Triage the finding and establish the affected identity, resource, account, Region and time range. Preserve relevant logs and snapshots using restricted evidence storage and record collection times and permissions. Choose containment based on potential damage, evidence needs and business impact. Recover from trusted artefacts and monitor for recurrence before closing the incident.

For a suspected workload compromise, decide whether isolation or service continuity takes precedence and account for evidence that could be lost if the instance stops. [AWS containment guidance](https://docs.aws.amazon.com/security-ir/latest/userguide/contain.html)

[Official exam domain guide](https://docs.aws.amazon.com/aws-certification/latest/security-specialty-03/security-specialty-03-domain2.html)
