Choices: EC2, Containers, Serverless

How to chose the optimal type?

* Assessing your workload (Get data on what resources the app sues during normal and peak usage times)


ES2
	you can use instances for long-running, stateful applications

Labmda:
	under 15 min
	not great fro compute intensive
	small, simple, modular
	focus on code
	might trigger another aws service
	

Containers:
	monolith with many parts
	microservices
	fast deploy, fast scale

**Amazon EC2 provides each instance with a consistent and predictable amount of CPU capacity,** regardless of its underlying hardware.


![[Pasted image 20230806232435.png]]


#### AWS Step functions

Visual ui where you connect your components and functions to build the system.

#### AWS Batch

Batch jobs with big compute

#### AWS Elastic Beanstalk 

Give it the app and it deploy it and scale automatically?

#### AWS LightSail

Low-cost preconfigured. Low-cost alternative to ec2?
