# Security foundations and governance

<a id="task-6-1"></a>

## 6.1 Central account management

Use AWS Organizations to group accounts into organisational units with common requirements, and use Control Tower where a managed landing zone and account provisioning help standardise the environment. Delegate appropriate security services to dedicated accounts and plan account enrolment and exceptions.

Apply controls by workload class and test their impact in a staging OU before broader rollout. [AWS Control Tower](https://docs.aws.amazon.com/controltower/latest/userguide/what-is-control-tower.html)

<a id="task-6-2"></a>

## 6.2 Secure deployment

Version infrastructure templates and build artefacts, require review, and run policy checks before promotion. Preventive controls restrict selected operations, detective controls surface drift, and proactive controls can evaluate supported resource properties before provisioning. Assign remediation ownership and define an exception process.

Pair deployment checks with configuration monitoring because resources can drift after creation. [Control Tower controls](https://docs.aws.amazon.com/controltower/latest/controlreference/introduction.html)

<a id="task-6-3"></a>

## 6.3 Compliance evaluation

Use AWS Config recording and rules to assess supported resources. Conformance packs distribute a collection of rules and remediation actions. Aggregators provide a cross-account and cross-Region view where configured. Confirm recording and delivery before interpreting missing results.

Evaluate the intended policy first and test automated remediation on a representative non-production resource before rolling it out. [AWS Config](https://docs.aws.amazon.com/config/latest/developerguide/WhatIsConfig.html)

[Official exam domain guide](https://docs.aws.amazon.com/aws-certification/latest/security-specialty-03/security-specialty-03-domain6.html)
