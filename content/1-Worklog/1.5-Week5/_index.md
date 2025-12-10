---
title: "Week 5 worklog"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:
Eliminate manual operations, manage large-scale server fleets, and fully codify infrastructure using IaC.

### Tasks completed this week:

| Task ID | Day | Task | Start Date | End Date | Status | Reference |
| --- | --- | --- | --- | --- | --- | --- |
| T5.1 | 01 | **AWS Systems Manager:** <br> - Ensure EC2 has AmazonSSMManagedInstanceCore role <br> - Use Run Command to execute shell commands across instances without SSH <br> - Enable Inventory for audit data collection | 01/10/2025 | 01/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T5.2 | 02 | **Session Manager:** <br> - Remove SSH access entirely, close port 22 <br> - Access EC2 via Session Manager (IAM + HTTPS) <br> - Log all sessions to S3/CloudWatch Logs | 02/10/2025 | 02/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T5.3 | 03 | **CloudFormation – IaC:** <br> - Understand IaC and CloudFormation workflow <br> - Write YAML template for VPC + EC2 <br> - Practice Stack create/update/delete + Drift Detection | 03/10/2025 | 03/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T5.4 | 04 | **AWS CDK – Basics:** <br> - Learn CDK and Imperative IaC <br> - Define infrastructure using TypeScript/Python <br> - Create VPC using L2 Construct | 04/10/2025 | 04/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T5.5 | 05 | **AWS CDK – Advanced:** <br> - Build custom Constructs (e.g., StandardS3Bucket) <br> - Participate in IaC Workshop to handle circular dependencies <br> - Manage Context and environment configs | 05/10/2025 | 05/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T5.6 | 06 | **Tagging & Resource Groups:** <br> - Design consistent tagging strategy (CostCenter, Env, Owner) <br> - Create Resource Groups based on tags | 06/10/2025 | 06/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T5.7 | 07 | **Tag-based Access Control – ABAC:** <br> - Learn ABAC <br> - Write IAM Policy allowing Developers to Start/Stop EC2 with tags Env=Dev & Owner=User | 07/10/2025 | 07/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |

### Week 5 Achievements:

* **Systems Manager & Session Manager:**
  * Manage systems without SSH access.
  * Improve EC2 security through IAM + HTTPS.
  * Collect logs and inventory from all instances.

* **Infrastructure as Code:**
  * Automate infrastructure using CloudFormation.
  * Use AWS CDK to write IaC with TypeScript/Python.
  * Build reusable Constructs for organizational standards.

* **Resource Management:**
  * Implement consistent tagging strategy.
  * Build Resource Groups based on tags.
  * Apply flexible access control using ABAC.

* **Summary:**
  * Strengthened DevOps mindset and Operational Excellence.
  * Ready for Week 6: CI/CD, Lambda, and Containers.
