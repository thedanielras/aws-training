Availability zone is composed of multiple interconnected data centers.
A region is a cluster of availability zones.

Resons to chose a region:
1. Compliance
2. Latency
3. Pricing
4. Service availability

Main ways to interact with AWS services:
1. Management console
2. CLI
3. SDK

Shared responsibility model
AWS is ensuring the security of the cloud, while the user has the responsibility to ensure security in the cloud.


AWS Identity management
For authentication and authorization of users
	Policy -> Group -> User
	Policy -> User
	User -> Multiple Groups <- Multiple policies
For access to resources by api by other apps
    Policy -> Role

