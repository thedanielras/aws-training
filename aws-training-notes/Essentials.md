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

### Unstructured data storage

Fundamentally these types are available:
* File storage
* Object storage
* Block storage

### Structured  data storage - databases

There are 2 way to have a database in AWS, either it is unmanaged, which means that you can migrate your RDB to an EC2 instance which will result in having to managed all aspects down to host system.
And managed, which can be be provided by Amazon RDS.
It is recommended to have RDS deployed at least in 2 availability zones for redundancy.

There are other databases build for specific use cases which can be used instead of RDB
* Amazon DynamoDB
* Amazon ElasticCache
* Amazon MemoryDB for Redis
* Amazon DocumentDB with MongoDB compatibility
* Amazon Keyspaces for Apache Cassandra
* Amazon Neptune (graph database)
* Amazon Timestream (timeseries db for IOT)
* Amazon Quantum Ledger Database (history of db transactions?)

### Monitoring

Benefits of using a monitoring solution:
 * Respond to operational issues before the end users are aware of them
 * Improve performance and reliability
 * Recognise security threats and events
 * Make data driven decisions
 * Create cost effective solution by optimising sizes based on usage

AWS CloudWatch is the aws solution for observability, can also trigger alarms and actions on some metrics threshold.

### Scalability, Availability
Availability is measured in downtime per year expressed in 9 percentiles ex: 99% 99.9%

AWS ELB - elastic load balancer

Can operate on application or ip layer
