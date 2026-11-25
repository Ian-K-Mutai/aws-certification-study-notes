# VPC traffic and connectivity

Read the route table before evaluating packet filters. A route determines where a packet is sent. Security groups apply stateful rules to supported network interfaces. Network ACLs apply stateless rules to subnets and evaluate numbered rules in order. For an ACL-controlled TCP connection, check the return traffic to the client's ephemeral port range as well as the inbound service port. A security group reference lets a rule identify interfaces associated with another group.

An internet-facing load balancer can accept traffic from the internet while its targets remain in private subnets. Use a NAT gateway when private workloads need outbound IPv4 internet connectivity. Determine whether the design uses zonal or regional NAT before discussing failure modes, routing and costs. Gateway endpoints provide route-table access to S3 and DynamoDB. Interface endpoints use elastic network interfaces and can use private DNS for supported services.

For hybrid connectivity, compare VPN and Direct Connect against throughput, encryption and provisioning requirements. Check route propagation and overlapping address ranges before treating an intermittent connection as an application problem.

[Amazon VPC user guide](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html) · [Regional NAT gateways](https://docs.aws.amazon.com/vpc/latest/userguide/nat-gateways-regional.html)
