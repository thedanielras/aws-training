
## AWS Well-Architected Framework

### Six Pillars

#### Operational excellence

Running and monitoring system to deliver business value and continually improving processes and procedures

#### Security

Protect information, system, and assets while delivering business value through risk assessments and mitigation strategies.
Areas:
* Identity and Access Management
* Detective Controls
* Infrastructure Protection
* Data Protection
* Incident Response

#### Reliability

Ability to prevent and quick recover from failures, to meet business and customer demand.

#### Performance Efficiency

Using IT and computing resources efficiently

#### Cost optimisation

Avoiding unneeded costs

#### Sustainability

Using recommendations and strategies to maximise efficiency and reduce waste 


#### Amazon Cognito

User SignIn, SignUp for mobile, web apps.

#### AWS Directory Service

Possibility to create AWS managed Microsoft Active Directory or ldap compatible directory for user federation. Also possible to combine with using the already existing on premises active directory. 

### Security Monitoring

#### Amazon GuardDuty

Scans and analise various datasources for threats, and alerts on findings.
To protect application and services.
Can create automated scenarios where a detected malicious ipp address would be blocked in security group of EC2.

#### Amazon SecurityHub

Collects data from all security services, aggregate, prioritise findings, show in a unified place.
Continuous compliance checks.
Take action on findings.
Multi account data aggregation.
Overall security and compliance posture.

#### Amazon Macie

Scans data and uses machine learning to understand what data is business critical and detects security threats to this data.

#### Amazon WAF (Web Application Firewall)

Protect web application on malicious requests. 
Requests can be filtered by ip address, url, rate of requests from an ip
Requests can be ignored if they contain an sql injection, cross-site scripting attack.

#### AWS Shield

Protects against DDOS attacks. Basic features free, advanced are priced.

#### AWS KMS for Key Management

Centrally manage and securely store your keys

#### AWS Certificate Manager

Create TLS certificate for domain, and then use it in different services serving requests over https.

#### AWS Secrets Manager

Store secrets like connection string to the database, give access only to correct IAM, regularly rotate secrets. Provide access to applications to secrets through api/sdk.

#### AWS Config

Monitor config of different services and apply rules for compliance, and check for compliance. For example, i can apply a rule to my EBS so that all my volumes need to be encrypted and i can see if they actually are.
Run trigger on configuration change. Can trigger lambda functions.

#### AWS Well-Architected Tool

Act as self service architecture advice tool that will show how the solution os behaving and what can be improved.