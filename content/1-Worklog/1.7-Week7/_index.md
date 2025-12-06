---
title: "Week 7 Worklog"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Access Security: Eliminate the need for SSH Keys and Port 22 using SSM Session Manager.
* Resource Management: Organize resources using Resource Groups and Tagging Strategy.
* Large-Scale Operations: Execute commands on multiple servers simultaneously without logging into each machine.
* Patching: Automate security patch update process.

### Tasks to be carried out this week:
| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T7.1 | 2 | **Tagging - Tag Audit:** <br> - Review and apply standard tags to all resources <br> - Format: `Env:Dev`, `Project:FCJ`, `Owner:Student` | 10/20/2025 | 10/20/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T7.2 | 2 | **SSM - Role Update:** <br> - Update EC2 IAM Role <br> - Add policy `AmazonSSMManagedInstanceCore` | 10/20/2025 | 10/21/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T7.3 | 3 | **SSM - Session Manager:** <br> - Access EC2 Instance via Console <br> - Use Session Manager instead of SSH | 10/21/2025 | 10/22/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T7.4 | 4 | **Security - Hardening:** <br> - Remove Port 22 Rule in Security Group `Web-SG` <br> - Verify access via SSM (success) <br> - Verify via SSH (fail as expected) | 10/22/2025 | 10/23/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T7.5 | 5 | **Resource Groups - Grouping:** <br> - Create Resource Group based on tag `Project:FCJ` <br> - Centrally manage resources | 10/23/2025 | 10/24/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T7.6 | 6 | **SSM - Run Command:** <br> - Use Run Command <br> - Run `yum update -y` on all instances with `Env:Dev` | 10/24/2025 | 10/25/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 7 Achievements:

* **Enhanced Security:**
  * Significantly reduced Attack Surface
  * No admin ports exposed to Internet
  * All access sessions logged in CloudTrail and Session Manager logs
  * Can record sessions for audit

* **Operational Efficiency:**
  * Updated software for entire Autoscaling Group with just a few clicks
  * No need to manage SSH keys for each user
  * Can run scripts on hundreds of servers simultaneously

* **Mindset:**
  * Shifted from "Managing individual servers" to "Fleet Management"
  * Understanding of Zero Trust Network Access
  * No need for bastion host or VPN

* **Skills:**
  * Proficient in SSM Session Manager
  * Understanding of IAM Instance Profile
  * Know how to organize resources with Tags and Resource Groups
  * Use SSM Run Command for automation
