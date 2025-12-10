---
title: "Worklog Week 9"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Master Docker and AWS container orchestration platforms: ECS and EKS.
* Deploy, automate and operate containerized applications with CI/CD.
* Understand trade-offs between ECS (Fargate) and EKS (Kubernetes) for different scenarios.

### Tasks to be carried out this week:

| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T9.1 | 1 | **Docker Fundamentals:** <br> - Containerization with Docker <br> - Write optimized Dockerfile (Multi-stage build) <br> - Create ECR repo and docker push private image | 01/11/2025 | 01/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T9.2 | 2 | **Amazon ECS & Fargate:** <br> - Deploy ECS with Fargate <br> - Define Task (CPU/RAM) <br> - Create Service and integrate with ALB | 02/11/2025 | 02/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T9.3 | 3 | **ECS with IaC (CDK):** <br> - Apply CDK for ECS <br> - Use ApplicationLoadBalancedFargateService (L3 Construct) | 03/11/2025 | 03/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T9.4 | 4 | **Amazon EKS – Setup:** <br> - Create EKS cluster (eksctl / CDK EKS Blueprints) <br> - Configure Managed Node Groups | 04/11/2025 | 04/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T9.5 | 5 | **Deploying applications on EKS:** <br> - Write manifests (Deployment, Service, Ingress) <br> - Install AWS Load Balancer Controller to provision ALB from Ingress | 05/11/2025 | 05/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T9.6 | 6 | **CI/CD for Containers:** <br> - Build pipeline: CodeCommit → CodeBuild → CodeDeploy <br> - Practice Blue/Green deployment for ECS/EKS | 06/11/2025 | 06/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T9.7 | 7 | **ROSA – Red Hat OpenShift on AWS:** <br> - Learn ROSA (Managed OpenShift) <br> - Use case: migrate OpenShift on-prem → AWS | 07/11/2025 | 07/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |

### Week 9 Achievements:

* Mastered optimized Dockerfile patterns and private image management on ECR.  
* Deployed serverless containers with ECS Fargate and integrated with ALB.  
* Automated ECS deployment using CDK (L3 Construct).  
* Bootstrapped EKS cluster, managed Node Groups and deployed K8s manifests.  
* Implemented CI/CD pipelines for container workflows and practiced Blue/Green deployment.  
* Understood ROSA use-cases for enterprises migrating OpenShift on-prem to AWS.
