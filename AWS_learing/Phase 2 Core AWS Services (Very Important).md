#### IAM – Identity & Access Management
---
##### What is IAM?
IAM is used to:
- Create **users**
- Assign **permissions**
- Secure your AWS account
---
#####  IAM Components

##### Users
- Individual people (you)
##### Groups
- Collection of users
- Permissions assigned at group level
##### Policies
- JSON documents defining permissions
#### Roles
- Used by AWS services (EC2, Lambda)
---
#### Hands-On: Create IAM User (Free Tier Safe)
#### Step 1: Create IAM User
1. Go to **IAM → Users → Create user**
2. Username: `cloud-user`
3. Select:
	- AWS Management Console access
	- Password: Auto-generate
#### Step 2: Permissions
- Attach policy
    - `AdministratorAccess` (for learning only)
#### Step 3: Save Credentials
Download `.csv` file  
You’ll never see it again

#### Test IAM User
1. Logout root user
2. Login using **IAM user**
3. Confirm access
---
#### EC2 – Elastic Compute Cloud 
#### What is EC2?
EC2 = Virtual Machine in AWS
You choose:
- OS (Amazon Linux, Ubuntu)
- CPU & RAM
- Storage
- Network
#### EC2 Instance Types
| Type     | Use        |
| -------- | ---------- |
| t2.micro | Free Tier  |
| t3.micro | Free Tier  |
| m5       | Production |

---
#### Hands-On: Launch EC2 (Free Tier)
#### Step 1: Launch Instance
1. Go to **EC2 → Launch Instance**
2. Name: `my-first-ec2`
3. AMI: **Amazon Linux 2023**
4. Instance type: **t2.micro**
#### Step 2: Key Pair 🔑
- Create new key pair
- Name: `ec2-key`
- Download `.pem` file
#### Step 3: Network
- VPC: Default
- Auto-assign public IP: **Enabled**
#### Step 4: Security Group
Allow:
- SSH → Port **22**
- Source: `My IP`
#### Step 5: Launch
#### connect to EC2
`chmod 400 ec2-key.pem
`ssh -i ec2-key.pem ec2-user@<PUBLIC-IP>`

---
#### S3 – Simple Storage Service
#### What is S3?
- Object storage
- Unlimited scale
- Used for backups, files, logs
#### Hands-On: Create S3 Bucket
#### Step 1
- Go to **S3 → Create bucket**
- Name: `my-cloud-bucket-<unique>`
- Region: Mumbai
#### Step 2
- Block public access: ON
- Create bucket
#### Upload File

- Upload a small file (<1 MB)
- Verify upload
---
#### S3 Storage Classes (Basic)
|Class|Use|
|---|---|
|Standard|Frequent access|
|IA|Infrequent|
|Glacier|Archive

---
#### VPC – Virtual Private Cloud  (Basics Only)
#### What is VPC?
Your **private network** inside AWS
Components:
- VPC
- Subnets
- Route tables
- Internet Gateway
Default VPC is enough for beginners
#### Key Concept
- Public subnet → Internet access
- Private subnet → No internet
---
#### AWS CLI – Core Commands 
#### Configure CLI
`aws configure`
Enter:
- Access Key
- Secret Key
- Region: `ap-south-1`
- Output: `json`
#### Useful CLI Commands
#### EC2
`aws ec2 describe-instances`
#### S3
`aws s3 ls
`aws s3 ls s3://my-cloud-bucket

---
#### Phase 2 Mini Tasks (Do These)
- [x] Create IAM user
- [x] Launch EC2  
- [x] SSH into EC2  
- [x] Create S3 bucket  
- [ ] Run AWS CLI commands
---
