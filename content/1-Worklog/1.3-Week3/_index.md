---
title: "Worklog Week 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* Transition from self-managed databases on EC2 to managed database services such as Amazon RDS and DynamoDB to reduce operational overhead.
* Understand Multi-AZ architecture, replication mechanisms, and the failover process of RDS.
* Learn and work with DynamoDB NoSQL database, including table design, read/write operations, and Index usage.
* Improve application performance using caching with ElastiCache.
* Combine knowledge to build a Highly Available (HA) Web Application architecture.
* Become familiar with AWS Directory Services to simulate enterprise environments.

### Tasks to be carried out this week:
| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T3.1 | 15 | **RDS – Relational Database:** <br> - Deploy Amazon RDS (MySQL or PostgreSQL) <br> - Enable Multi-AZ Deployment <br> - Analyze synchronous replication & automatic failover mechanism | 15/09/2025 | 15/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T3.2 | 16 | **RDS – Operations & Connectivity:** <br> - Configure Security Group to allow only EC2 access to RDS <br> - Customize Parameter Groups <br> - Configure Automated Backup & create Manual Snapshot <br> - Test DB Restore to evaluate RPO | 16/09/2025 | 16/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T3.3 | 17 | **DynamoDB – NoSQL Basics:** <br> - Learn NoSQL mindset <br> - Create Users table with Partition Key = UserId <br> - Compare Provisioned vs On-Demand Capacity <br> - Choose On-Demand for development environment | 17/09/2025 | 17/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T3.4 | 18 | **DynamoDB – Advanced:** <br> - Practice PutItem, GetItem, Query, Scan <br> - Evaluate performance differences between Query and Scan <br> - Create Global Secondary Index (GSI) for Email queries | 18/09/2025 | 18/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T3.5 | 19 | **ElastiCache – In-Memory Cache:** <br> - Deploy ElastiCache Redis <br> - Apply Lazy Loading strategy <br> - Place Redis cluster inside Private Subnet | 19/09/2025 | 19/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T3.6 | 20 | **Web Architecture – Highly Available:** <br> - Combine EC2 + RDS Multi-AZ + S3 <br> - Deploy Application Load Balancer (ALB) <br> - Simulate failover when one AZ has issues | 20/09/2025 | 20/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T3.7 | 21 | **Directory Services:** <br> - Learn AWS Managed Microsoft AD <br> - Integrate Windows EC2 into Domain <br> - Apply basic GPO for centralized management | 21/09/2025 | 21/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |

### Week 3 Achievements:

* **Relational Database (RDS):**
  * Successfully deployed MySQL/PostgreSQL database.
  * Understood and tested Multi-AZ Failover mechanism.
  * Configured Parameter Groups and completed Backup setup.

* **NoSQL Database:**
  * Created DynamoDB table following correct Partition Key design.
  * Distinguished clearly between Query vs Scan in cost & performance.
  * Built GSI for more flexible querying.

* **Caching:**
  * Integrated Redis to reduce RDS read load.
  * Applied Lazy Loading strategy for optimal performance.

* **HA Web Architecture:**
  * EC2 multi-AZ + RDS Multi-AZ + S3 + ALB operating correctly.
  * Simulated failover successfully when 1 AZ went down.

* **Directory Services:**
  * Understood architecture and use-cases of AWS Managed Microsoft AD.
  * Joined Windows EC2 to Domain and applied basic GPO.

* **Summary:**
  * Completed strong foundation in Database & Application Architecture.
  * Ready to move to Week 4 covering Network Scaling, Auto Scaling, and Monitoring.
