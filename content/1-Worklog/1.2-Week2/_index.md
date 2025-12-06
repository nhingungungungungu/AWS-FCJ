---
title: "Week 2 Worklog"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Identity Security: Completely eliminate the use of the Root account for daily administration tasks; establish a standard User/Group structure.
* Network Architecture: Design and deploy a Custom VPC instead of using the Default VPC, ensuring deep understanding of IP planning.
* Traffic Control: Configure Route Tables to clearly distinguish between Public and Private Subnets.
* Compliance: Enable Multi-Factor Authentication (MFA) as a mandatory requirement for all Console access accounts.

### Tasks to be carried out this week:
| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T2.1 | 2 | **IAM - Securing Root:** <br> - Log in as Root, enable MFA (Virtual Authenticator App) <br> - Remove all Access Keys for Root (if any) | 09/15/2025 | 09/15/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T2.2 | 2 | **IAM - Admin Group Setup:** <br> - Create IAM Group `CloudAdmins` <br> - Attach policy `AdministratorAccess` (AWS Managed Policy) | 09/15/2025 | 09/15/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T2.3 | 3 | **IAM - User Creation:** <br> - Create IAM User for yourself <br> - Set Password Policy (complexity, rotation) <br> - Add to group `CloudAdmins` | 09/16/2025 | 09/16/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T2.4 | 4 | **VPC - IP Planning:** <br> - Calculate CIDR for VPC (10.0.0.0/16) <br> - Design Subnets to support up to 65,536 IP addresses | 09/17/2025 | 09/17/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T2.5 | 4 | **VPC - Deploy VPC:** <br> - Initialize VPC in Region ap-southeast-1 (Singapore) <br> - Tag with `Project=FCJ` | 09/17/2025 | 09/17/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T2.6 | 5 | **VPC - Subnet Design:** <br> - Create 4 Subnets: 2 Public (10.0.1.0/24, 10.0.2.0/24) <br> - 2 Private (10.0.3.0/24, 10.0.4.0/24) <br> - Distribute evenly across 2 AZs | 09/18/2025 | 09/18/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T2.7 | 5 | **VPC - Internet Access:** <br> - Create and attach Internet Gateway (IGW) to VPC <br> - Configure Route Table of Public Subnet to route 0.0.0.0/0 to IGW | 09/18/2025 | 09/19/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T2.8 | 6 | **Security - Firewall Basics:** <br> - Create Security Group `Web-SG` <br> - Allow Inbound HTTP (80) from 0.0.0.0/0 <br> - Allow SSH (22) from MyIP | 09/19/2025 | 09/21/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 2 Achievements:

* **Account Security:** 
  * Transitioned to using IAM User with MFA for login
  * Root account protected with strong password and separate physical/application MFA
  * Applied the principle of "Least Privilege"

* **Network Infrastructure:**
  * A fully functional custom VPC operational
  * Verified DNS resolution capability (DNS Hostnames enabled)
  * Established 2-Tier Network Architecture model

* **Architecture:**
  * Ready for deploying Web applications and Databases in upcoming weeks
  * Clear understanding of the difference between Public and Private Subnets
  * Solid grasp of CIDR and subnet mask concepts

* **Lessons Learned:**
  * Security Group is an instance-level firewall (stateful)
  * Network ACL is a subnet-level firewall (stateless)
  * Understanding of AWS Shared Responsibility Model
