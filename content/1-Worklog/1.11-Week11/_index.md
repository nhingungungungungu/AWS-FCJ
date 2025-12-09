---
title: "Worklog Week 11"
date: 2025-11-21
weight: 1
chapter: false
pre: " <b> 1.11. </b> "
---
### Week 11 Goals:

* Provision AWS Lightsail instance and managed PostgreSQL for the backend.
* Prepare deployment pipeline/environment variables for AWS Jewelry API.

### Tasks for Week 11

| Day | Task | Start Date | End Date | Reference Material |
|-----|------|------------|----------|--------------------|
| 1   | Create Lightsail instance (tk giang), configure networking, SSH keys, firewall rules. | 17/11/2025 | 17/11/2025 | AWS Lightsail docs |
| 2   | Provision Lightsail PostgreSQL; create DB/user, set parameter group, capture connection string. | 18/11/2025 | 18/11/2025 | AWS Lightsail docs |
| 3   | Harden instance (updates, fail2ban/basic firewall), install runtime and reverse proxy. | 19/11/2025 | 19/11/2025 | Team playbook |
| 4   | Prepare environment configs (.env) for DB, Cognito, S3, Secrets Manager placeholders. | 20/11/2025 | 20/11/2025 | `AWSJewelry` proposal |
| 5   | Dry-run deployment build on Lightsail; verify DB connectivity and migrations. | 21/11/2025 | 21/11/2025 | Deployment notes |

### Achievements of Week 11:
* Lightsail instance created (user giang) with secured SSH access and firewall aligned to API ports.
* Managed PostgreSQL set up with dedicated DB/user; connection string validated from instance.
* Server hardened and runtime stack installed with reverse proxy ready for API hosting.
* Environment variables prepared for Cognito, S3, DB, Secrets Manager to support deployment.