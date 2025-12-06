---
title: "Week 5 Worklog"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Fast VPS: Deploy a complete WordPress application in 5 minutes using Amazon Lightsail.
* Containerization: Package a small application into a Docker Image and deploy on Lightsail Container Service.
* Elasticity: Set up self-healing and auto-scaling architecture with EC2 Auto Scaling Group.
* Load Balancing: Distribute user traffic through Application Load Balancer (ALB).

### Tasks to be carried out this week:
| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T5.1 | 2 | **Lightsail - WordPress Deploy:** <br> - Initialize Lightsail Instance with "WordPress" Blueprint <br> - Assign Static IP | 10/06/2025 | 10/06/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T5.2 | 2 | **Container - Docker Intro:** <br> - Write simple Dockerfile for Hello World webpage <br> - Build and test on Cloud9 | 10/06/2025 | 10/07/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T5.3 | 3 | **Lightsail - Container Deploy:** <br> - Push Docker Image to Lightsail Container Service <br> - Configure Public Endpoint | 10/07/2025 | 10/08/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T5.4 | 4 | **EC2 - Launch Template:** <br> - Create Launch Template: Amazon Linux 2023, t3.micro <br> - User Data script to auto-install Apache Web Server | 10/08/2025 | 10/09/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T5.5 | 4 | **Networking - Target Group:** <br> - Create empty Target Group <br> - Ready for ASG to register instances | 10/09/2025 | 10/10/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T5.6 | 5 | **EC2 - Create ALB:** <br> - Initialize internet-facing Application Load Balancer <br> - Listen on port 80, route traffic to Target Group | 10/09/2025 | 10/10/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T5.7 | 5 | **EC2 - Auto Scaling Group:** <br> - Create ASG: Min=1, Desired=2, Max=4 <br> - Use Launch Template <br> - Integrate with ALB Target Group | 10/09/2025 | 10/10/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T5.8 | 6 | **Testing - Stress Test:** <br> - SSH into instance, install stress tool <br> - Push CPU to 100% and observe ASG Scale Out | 10/10/2025 | 10/12/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 5 Achievements:

* **Comparison:**
  * Lightsail extremely fast to deploy but lacks deep network customization
  * Lightsail VPC Peering has limitations
  * Suitable for small projects, blogs, prototypes

* **Elastic System:**
  * Built a Fault Tolerant Web system
  * When manually terminating 1 instance, ASG immediately creates a new replacement instance
  * System automatically scales up/down based on demand

* **Load Balancing:**
  * ALB distributes requests evenly between instances
  * Ensures users don't experience service interruption when a server fails
  * Understanding of Health Checks and Drain Connection

* **Architecture:**
  * Solid grasp of Stateless Architecture concept
  * Cannot store uploaded files or sessions on EC2 hard drive
  * Combine S3 (files) and RDS (data) for Cloud-Native system
  * User Data for Bootstrapping is a key automation technique
