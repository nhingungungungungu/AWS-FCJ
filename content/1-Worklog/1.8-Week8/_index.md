---
title: "Week 8 Worklog"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Infrastructure Automation: Recreate network architecture (VPC) and servers (EC2) with code.
* Understanding Essence: Master CloudFormation structure (Parameters, Resources, Outputs).
* Modern Tools: Get familiar with AWS CDK and the cdk init, cdk synth, cdk deploy workflow.
* Lifecycle Management: Practice clean deletion (Destroy) and recreation (Deploy) of entire stack in minutes.

### Tasks to be carried out this week:
| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T8.1 | 2 | **CloudFormation - Write Template:** <br> - Write `vpc.yaml` file defining VPC <br> - Include: Subnet, Internet Gateway, Route Table | 10/27/2025 | 10/27/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T8.2 | 2 | **CloudFormation - Deploy Stack:** <br> - Upload file to CloudFormation Console <br> - Create stack `FCJ-VPC-Stack` <br> - Verify resources created | 10/27/2025 | 10/28/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T8.3 | 3 | **CDK - Init Project:** <br> - Install AWS CDK <br> - Initialize TypeScript project: `cdk init app --language typescript` | 10/28/2025 | 10/28/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T8.4 | 4 | **CDK - Define S3:** <br> - In `lib/stack.ts`, add code to create S3 Bucket <br> - Enable versioning and encryption (L2 Construct) | 10/29/2025 | 10/29/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T8.5 | 5 | **CDK - Deploy:** <br> - Run `cdk deploy` <br> - Observe ChangeSet creation and execution | 10/30/2025 | 10/30/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T8.6 | 5 | **IaC - Drift Detection:** <br> - Manually change S3 bucket tag on Console <br> - Run Drift Detection to detect discrepancy | 10/30/2025 | 10/31/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T8.7 | 6 | **IaC - Cleanup:** <br> - Run `cdk destroy` to remove all resources <br> - Ensure no cost leakage | 10/31/2025 | 10/31/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 8 Achievements:

* **Speed:**
  * Can rebuild entire network environment in just 2 minutes running commands
  * Instead of 30 minutes of manual clicking
  * Minimizes human errors

* **Control:**
  * Infrastructure code stored in Git
  * Review change history (Who modified the Subnet? Why?)
  * Code review for infrastructure changes
  * Version control for infrastructure

* **Experience:**
  * CDK is intuitive and requires less code than pure CloudFormation
  * Thanks to high-level Constructs (L2, L3)
  * Has type checking and autocomplete
  * Easy to test infrastructure code

* **Skills:**
  * Understanding of Infrastructure as Code (IaC)
  * Solid grasp of CloudFormation template structure
  * Proficient in AWS CDK with TypeScript
  * Know how to use Drift Detection

* Used AWS CLI to perform basic operations such as:

  * Check account & configuration information
  * Retrieve the list of regions
  * View EC2 service
  * Create and manage key pairs
  * Check information about running services
  * ...

* Acquired the ability to connect between the web interface and CLI to manage AWS resources in parallel.
* ...
