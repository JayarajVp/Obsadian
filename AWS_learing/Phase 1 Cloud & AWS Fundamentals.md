##### What is Cloud Computing?
##### Simple Definition
Cloud computing means:
Using computing resources (servers, storage, databases, networking) over the internet instead of owning physical hardware.
##### Real-life Example
Gmail → SaaS
AWS EC2 → IaaS
AWS Elastic Beanstalk → PaaS

----

##### Cloud Service Models
-----
##### IaaS (Infrastructure as a Service)
###### You manage:
- OS
- Applications
###### AWS manages:
- Hardware
- Networking
###### Example:
- Amazon EC2
- Amazon EBS
-----
##### SaaS (Software as a Service)
You just use the software
AWS manages everything
###### Example:
- Gmail
- AWS Console
- Amazon WorkMail
----
##### PaaS (Platform as a Service)
###### You manage:
- Application code
###### AWS manages:
- OS
- Runtime
- Infrastructure
###### Example:
- AWS Elastic Beanstalk
- AWS App Runner
-----
#### AWS Shared Responsibility Model 
**Key Rule:**
Security OF the Cloud → AWS
Security IN the Cloud → You

-----
####  Responsible 
**You Are Responsible For:** User access (IAM), OS updates, Application security, Data encryption.
**AWS Responsible For** Data center security, Hardware, Physical networking, Managed services.

---
#### AWS Global Infrastructure 
**Components**
- **Region** → Physical location (e.g., Mumbai)
- **Availability Zone (AZ)** → Isolated data centers inside a region
- **Edge Location** → Content delivery (CloudFront)
###### Example
`Region: ap-south-1 (Mumbai)
`AZs: ap-south-1a, ap-south-1b, ap-south-1c

----
#### AWS Pricing Models 
**On-Demand**
- Pay per second/hour
- No commitment
**Reserved Instances**
* 1 or 3 year commitment
* Cheaper than On-Demand
**Spot Instances**
* Use unused AWS capacity
* Cheapest
* Can be terminated anytime
----
#### Hands-On: AWS Console Basics
**Task 1:** Explore AWS Console
* Login to AWS Console
* Change region → Mumbai (ap-south-1)
**Explore services:**
* EC2
* S3
* IAM
* Billing
----
#### Hands-On: AWS CLI

Check if AWS CLI is installed
`aws --version`
If not installed → we’ll install it inside an EC2 
Vm 
* `curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"`
* ` unzip awscliv2.zip
* ` sudo ./aws/install
--- 
#### Cost Management & Budgets 
**Set Billing Alerts**
* Go to Billing Dashboard
* Enable Billing Alerts
* Create Budget
* Amount: $1 or $5
* Email alert
---
Phase 1 Checklist 
 Understand cloud basics
- [x] Know IaaS / PaaS / SaaS
- [x] Understand Shared Responsibility
- [x] Know AWS regions & AZs
- [x] Know pricing models
- [x] Login to AWS Console
- [x] Enable billing alerts
---
