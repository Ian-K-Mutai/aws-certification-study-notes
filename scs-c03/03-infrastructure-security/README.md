# Infrastructure security

<a id="task-3-1"></a>

## 3.1 Network edge controls

Use WAF to inspect supported HTTP request paths, Shield for DDoS protection, and Firewall Manager where supported policies need central administration across accounts. Stage WAF rule changes in count mode when possible and inspect sampled traffic or logs before switching to blocking.

Compare noisy rules with legitimate request patterns and define narrow exceptions. Verify the policy applies to the intended resource and Region. [AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html)

<a id="task-3-2"></a>

## 3.2 Compute security controls

Use controlled images, patch operating systems where responsibility remains with the customer, and assign workload roles with workload-specific permissions. Evaluate Inspector coverage for supported workloads, and distinguish findings about vulnerable packages from runtime activity. For EC2, use managed access such as Systems Manager Session Manager when platform prerequisites are met.

A new image protects future launches. Verify rollout or remediation for instances already running. [Amazon Inspector](https://docs.aws.amazon.com/inspector/latest/user/what-is-inspector.html)

<a id="task-3-3"></a>

## 3.3 Network security controls

For a private workload that cannot reach an AWS API, check routing, DNS, subnet ACLs, endpoint security groups and endpoint policy. Use Reachability Analyzer for supported static path analysis and VPC Flow Logs for observations about network traffic. Network Firewall covers inspected network paths, while security groups and ACLs apply at their respective boundaries.

Trace both directions of the path and validate that inspection routing remains symmetric where the design requires it. [VPC traffic and connectivity](../../shared/networking/README.md)

[Official exam domain guide](https://docs.aws.amazon.com/aws-certification/latest/security-specialty-03/security-specialty-03-domain3.html)
