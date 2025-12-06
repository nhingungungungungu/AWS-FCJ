---
title: "Week 4 Worklog"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---


### Week 4 Objectives:

* Dev Environment: Set up AWS Cloud9 as a unified development environment.
* Serverless Web: Deploy a static website on S3, configure Bucket Policy to allow safe public access.
* Database: Initialize Amazon RDS MySQL in Private Subnet to ensure security.
* Multi-Tier Connectivity: Establish connection from EC2/Cloud9 (Public Subnet) to RDS (Private Subnet).

### Tasks to be carried out this week:
| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T4.1 | 2 | **Cloud9 - Setup IDE:** <br> - Initialize Cloud9 environment (EC2 t3.small) in VPC <br> - Enable Auto-hibernate after 30 minutes | 09/29/2025 | 09/29/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T4.2 | 3 | **S3 - Static Hosting:** <br> - Create S3 Bucket with unique name <br> - Enable "Static website hosting" <br> - Upload index.html and error.html | 09/30/2025 | 09/30/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T4.3 | 3 | **S3 - Public Policy:** <br> - Disable "Block Public Access" <br> - Write Bucket Policy (JSON) allowing s3:GetObject | 09/30/2025 | 10/01/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T4.4 | 4 | **RDS - Subnet Group:** <br> - Create DB Subnet Group <br> - Include 2 Private Subnets created in Week 2 | 10/01/2025 | 10/01/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T4.5 | 4 | **RDS - Launch DB:** <br> - Launch RDS MySQL (Free Tier) <br> - Disable Multi-AZ <br> - Disable Public Accessibility | 10/01/2025 | 10/02/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T4.6 | 5 | **Security - Security Chaining:** <br> - Configure RDS Security Group <br> - Only allow Inbound Port 3306 from Cloud9/EC2 SG | 10/02/2025 | 10/03/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T4.7 | 6 | **Database - Connection Test:** <br> - Use terminal on Cloud9 <br> - Connect MySQL: `mysql -h <endpoint> -u admin -p` | 10/03/2025 | 10/05/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 4 Achievements:

* **Web:**
  * Static website operational at S3 Endpoint URL
  * Clear understanding of how S3 can host websites without servers
  * Solid grasp of writing Bucket Policy for safe public access

* **Database:**
  * DB instance operating isolated in internal network
  * Cannot access DB directly from Internet (correct security standard)
  * Understanding of RDS Managed Service and its benefits

* **Skills:**
  * Mastered JSON syntax for S3 Policy
  * Understanding of "Security Group Referencing" (nested SG references)
  * Critical technique for building dynamic N-tier architecture

* **Architecture:**
  * Completed preliminary "3-Tier Web Architecture" model:
    * Presentation Tier (S3)
    * Application Tier (Cloud9/EC2)
    * Data Tier (RDS)
  * Understanding of separation of concerns in cloud architecture
