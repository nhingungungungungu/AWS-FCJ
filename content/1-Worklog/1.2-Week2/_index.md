---
title: "Week 2 Worklog"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Compute: Launch and manage EC2 instances using best practices.
* Storage: Understand and work with EBS, EBS Snapshots, and S3 object storage.
* Development: Set up and use AWS Cloud9 as a cloud-based IDE.
* Simplified Compute: Explore Amazon Lightsail for lightweight and quick deployments.

### Tasks to be carried out this week:

| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T2.1 | 8 | **EC2 – Launch & Connect:** <br> - Select appropriate Instance Types (T3, C5, R5) <br> - Launch Amazon Linux 2023 AMI <br> - Create & use Key Pair to SSH into EC2 | 09/08/2025 | 09/08/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T2.2 | 9 | **EBS & Windows Workloads:** <br> - Create & attach gp3 EBS Volume <br> - Mount volume to EC2 <br> - Launch Windows Server & connect via RDP <br> - Install IIS Web Server <br> - Create EBS Snapshot | 09/09/2025 | 09/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T2.3 | 10 | **Cloud9 – Cloud IDE:** <br> - Set up AWS Cloud9 environment <br> - Test terminal, AWS CLI, SAM, and Docker <br> - Explore remote development without opening SSH ports | 09/10/2025 | 09/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T2.4 | 11 | **Amazon S3 – Basics:** <br> - Create S3 Bucket and upload files <br> - Enable Static Website Hosting <br> - Write JSON Bucket Policy for public read | 09/11/2025 | 09/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T2.5 | 12 | **Amazon S3 – Advanced:** <br> - Analyze Storage Classes (Standard, IA, Glacier, etc.) <br> - Configure Lifecycle Policy (move objects >30 days to Glacier) <br> - Enable Block Public Access, Versioning, and Default Encryption | 09/12/2025 | 09/12/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T2.6 | 13 | **Amazon Lightsail – VM Deployment:** <br> - Explore Lightsail features <br> - Deploy WordPress using LAMP Blueprint <br> - Compare EC2 vs Lightsail (cost & use-cases) | 09/13/2025 | 09/13/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T2.7 | 14 | **Lightsail Containers:** <br> - Build a simple Node.js app into Docker Image <br> - Push and deploy with Lightsail Container Service <br> - Review differences with ECS/EKS | 09/14/2025 | 09/14/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |

### Week 2 Achievements:

* **Compute:**  
  - Successfully launched EC2 Linux & Windows instances.  
  - Understood instance families (T3, C5, R5) and their use-cases.  
  - Connected securely using SSH and RDP.

* **Storage:**  
  - Worked with EBS volumes (create, attach, mount).  
  - Created incremental Snapshots for data backup.  
  - Built static website hosting using S3 and configured Bucket Policies.  
  - Implemented Lifecycle Policies, Versioning, and Default Encryption.

* **Development Environment:**  
  - Set up Cloud9 as a cloud-based IDE with built-in AWS tooling.  
  - Performed development without exposing SSH ports.

* **Lightsail:**  
  - Deployed WordPress using Lightsail VM.  
  - Built and deployed containerized apps using Lightsail Container Service.

* **Overall:**  
  - Completed foundational Compute & Storage services.  
  - Ready for Week 3 focusing on Load Balancing, Auto Scaling, and deeper AWS Architecture.
