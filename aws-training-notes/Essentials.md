Availability zone is composed of multiple interconnected data centers.
A region is a cluster of availability zones.

### Resons to chose a region:
1. Compliance
2. Latency
3. Pricing
4. Service availability

### Main ways to interact with AWS services:
1. Management console
2. CLI
3. SDK

### Shared responsibility model
AWS is ensuring the security of the cloud, while the user has the responsibility to ensure security in the cloud.


### AWS Identity management
For authentication and authorization of users
	Policy -> Group -> User
	Policy -> User
	User -> Multiple Groups <- Multiple policies
For access to resources by api by other apps
    Policy -> Role


### Amazon EC2
Naming:
	type-generation-attribute.size
Uses Amazon Machine Image (AMI) which can be used from available or created
Bills only when instance is in running state
Can have hibernate or stop which requires using EBS storage
Can resize instance
Can provide on-demand instances, or a bunch of option to increase savings, like spot instances and reserved ones
Can rent bare-metal

### Amazon ECS, EKS
Managed container env, eks is managed kubernetes, but still need to take care of ec2 instances that this runs on
Amazon Fargate is the serverless option here, meaning you will care only about kubernetes and not care about the underlying host os

### Amazon Lambda
Serverless functions that can be triggered by some trigger and are used an billed on demand

### Networking

IPv4 - 32 bit address
IPv4 Notation - 4 bytes in decimal separated by .
CIDR notation - IPv4 notation / number of fixed bytes so that the remaining bytes represent the range of ip addresses

To access subnet from internet need to create an Internet Gateway
To link subnet to own private network need to create Virtual Private Gateway

VPC -> Subnet

Routing table should be set to allow traffic to subnet from the internet to allow traffic to it through internet gateway

NetworkAccessControlList (firewall at subnet level, stateless) -> Security Groups (firewall at EC2 level, stateful)
