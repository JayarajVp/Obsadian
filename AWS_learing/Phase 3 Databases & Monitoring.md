We will cover 
- RDS (Relational Database Service)
- DynamoDB (NoSQL Database)
- CloudWatch (Monitoring & Logging)
-  Basic Alarms & Metrics
---
#### RDS – Relational Database Service 
**What is RDS?**
RDS is a managed SQL database service.
**AWS manages:**
- OS
- Patching
- Backups
- High availability (optional)
**You manage:**
- Database schema
- Users
- Queries
---
#### Supported Engine 
| Engine     | type |
| ---------- | ---- |
| MySQL      | SQL  |
| PostgreSQL | SQL  |
| MariaDB    | SQL  |
| Oracle     | SQL  |
| SQL Server | SQL  |

----
**Free Tier Rule**
- Instance: db.t3.micro
- Storage: ≤ 20 GB
- Single AZ only(Availablity zone)
---
#### Hands-On: Create RDS (Free Tier Safe)
**Step 1:** Create Database
- Go to RDS → Create database
- Creation method: Standard
- Engine: MySQL
- Templates: Free tier
**Step 2:** Settings
- DB identifier: mydb
- Master username: admin
- Password: set & save
**Step 3:** Instance & Storage
- Instance class: db.t3.micro
- Storage: 20 GB
- Disable autoscaling
**Step 4:** Connectivity
- VPC: Default
- Public access: Yes
- Security group:
- Allow MySQL (3306) from your IP
**Step 5:** Create Database 
* Takes ~5–10 minutes
**Connect to RDS (From EC2)**
`sudo yum install mysql -y
`mysql -h <RDS-ENDPOINT> -u admin -p

---
#### DynamoDB – NoSQL Database 
**What is DynamoDB?**
* Fully managed NoSQL (key-value)
* Serverless
* Extremely fast
* No servers to managel
**Key Concepts**
- Table
- Primary key
    - Partition key
    - (Optional) Sort key
- Items & attributes
**When to Use DynamoDB?**
✅ High scale
✅ Low latency
✅ Serverless apps
❌ Complex SQL joins

---
#### Hands-On: Create DynamoDB Table
**Step 1**
- Go to DynamoDB → Create table
- Table name: users
- Partition key: userId (String)
**Step 2**
- Capacity mode: On-demand
- Create table
**Add Item**
Example:
`{
 `"userId": "101",
 `"name": "Alice",
 `"email": "alice@example.com"
}`

**CLI test**
` aws dynamodb list-tables

----
