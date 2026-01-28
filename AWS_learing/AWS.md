### [[Phase 0 Prerequisites (Must Have)]]
Before touching AWS, ensure you are comfortable with:
- Linux fundamentals: files, permissions, users, systemctl, logs
- Networking basics: TCP/IP, DNS, HTTP/HTTPS, ports, NAT, CIDR
- Basic scripting: Bash (mandatory), Python (recommended)
- Git fundamentals: repositories, commits, branches
If these are weak, AWS will feel confusing later.
### [[Phase 1 Cloud & AWS Fundamentals]]
#### Concepts to Understand
- What is cloud computing
- IaaS vs PaaS vs SaaS
- Shared Responsibility Model
- Regions, Availability Zones, Edge Locations
- Billing model: On-Demand, Reserved, Spot
- AWS global infrastructure
#### Hands-On
- Create AWS Free Tier account
- Understand AWS Management Console
- Install and configure AWS CLI
- Learn basic cost management and budgets
### [[Phase 2 Core AWS Services (Very Important)]]

#### Identity & Access
- AWS IAM
- Users, groups, roles
- Policies and permissions
- Best practices (least privilege, MFA)
#### Compute
- Amazon EC2
    - Instance types
    - AMIs
    - Key pairs
    - Security groups
- Auto Scaling Groups
- Elastic Load Balancer (ALB/NLB)
#### Storage
- Amazon S3
    - Buckets, objects
    - Storage classes
    - Lifecycle rules
- EBS vs EFS (when to use what)
#### Networking
- Amazon VPC
    - Subnets (public/private)
    - Route tables
    - Internet Gateway, NAT Gateway
    - Security Groups vs NACLs
### [[Phase 3 Databases & Monitoring]]
#### Databases
- Amazon RDS
- MySQL/PostgreSQL basics
- Backups and snapshots
- DynamoDB basics (NoSQL use cases)
#### Monitoring & Logging
- Amazon CloudWatch
- Metrics
- Alarms
- Logs
- CloudTrail (audit logging)
### [[Phase 4 Automation & Infrastructure as Code]]
#### Infrastructure as Code
- AWS CloudFormation
    - Templates
    - Stacks
- Terraform
    - Providers
    - State files
    - Modules
### [[Phase 5 DevOps & CI CD]]
#### CI/CD Basics
- Git-based workflows
- Build → Test → Deploy pipeline
#### Tools
- Jenkins
- GitHub Actions
### AWS Deployment Services
- CodeBuild
- CodeDeploy
- CodePipeline
### [[Phase 6 Containers & Orchestration]]
Very important for modern AWS roles.
#### Containers
- Docker fundamentals
- Images, containers, volumes
#### AWS Container Services
- Amazon ECS
- Amazon EKS
### [[Phase 7 Serverless & Advanced Services]]
#### Serverless
- AWS Lambda
- API Gateway
- Event-driven architecture
#### Advanced Topics
- S3 + CloudFront (CDN)
- KMS (encryption)
- Secrets Manager
- High Availability & Disaster Recovery
- Cost optimization strategies
#### [[Phase 8 Security & Best Practices]]
Mandatory for production environments.
- IAM best practices
- Network security design
- Encryption at rest and in transit
- Logging and alerting
- Well-Architected Framework
### [[Phase 9 Real-World Projects (Critical)]]
You should build at least 3–5 solid projects:
- Host a website on EC2 behind ALB
- CI/CD pipeline deploying app to EC2
- VPC with public/private subnet architecture
- S3 static website with CloudFront
- Dockerized app deployed on ECS or EKS
----------

Test of auto sync
