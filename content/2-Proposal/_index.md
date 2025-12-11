---
title: "Proposal"
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Project Plan: AWS Jewelry Web Store

## 1. Background and Motivation

### 1.1 Executive Summary
This project aims to build an e-commerce platform for jewelry. The architecture includes a backend and database hosted on **AWS Lightsail**, and a **React** frontend stored on **Amazon S3** and delivered through **CloudFront** with HTTPS via ACM. The goal is to ensure easy scalability, strong security, and cost optimization using essential AWS services.

**Key Features**
- Jewelry product management.
- Product image uploads.
- Shopping cart.
- User registration/login using **Amazon Cognito**.
- Backend API on Lightsail with **MySQL/Postgres** database.
- CloudFront CDN + global SSL.

### 1.2 Success Criteria
- Performance: page load < 2s via CloudFront.
- Stability: Lightsail API supports realistic traffic.
- Data integrity: secure and efficient database operations.
- User management: reliable and secure Cognito authentication.
- Security: safe S3 image uploads.
- Monitoring: complete API logging via CloudWatch.

### 1.3 Assumptions
- Traffic < 100,000 requests/month.
- No advanced autoscaling requirements.
- Domain already available or purchased through Route 53.
- Team is experienced with .NET/React (migration from Node.js to .NET).

## 2. Solution Architecture

### 2.1 Architecture Diagram
![alt text](/images/Diagram.jpg)

### 2.2 Technical Plan
- Configure S3 hosting + CloudFront, set up HTTPS/ACM, map domain with Route 53.
- Deploy Lightsail API, connect DB, integrate Cognito, load secrets from Secrets Manager.
- Image upload workflow: API provides presigned URLs; S3 remains private with CloudFront access only.
- Logging/metrics through CloudWatch.

### 2.3 Project Plan
Estimated timeline: 6–12 weeks depending on final scope.

### 2.4 Security
- S3 private access, readable only through CloudFront.
- API secrets stored in Secrets Manager.
- Full HTTPS enforcement.
- Cognito-protected login.

## 3. Activities and Deliverables

| Phase | Week | Main Activities | Deliverable | MD |
|-----------|------|-------------------------|-------------------------|----|
| Assessment | 1 | Requirement gathering, architecture design, DB schema drafting, secrets listing | Architecture diagram, DB schema, secrets inventory | 5 |
| Core Infrastructure | 2 | S3 + CloudFront + ACM + Route 53 setup; Lightsail API & DB; Cognito; secrets creation; enable CloudWatch | Working CDN frontend, ready API & DB, Cognito login, secrets configured | 7 |
| Component 1 – Backend | 3 | API reads secrets, presigned uploads, product CRUD, Cognito authentication, CloudWatch logs | Stable API, successful uploads, working login, no hardcoded configs | 7 |
| Component 2 – Frontend | 4 | React shop UI, Cognito login UI, image upload UI, API integration, build & deploy to S3+CF | Complete UI with API integration | 7 |
| Testing & Go-live | 5 | FE↔BE↔S3↔DB integration test, security test (IAM + Secrets Manager), E2E tests | Test report, security checklist | 5 |
| Handover | 6 | Secrets update guide, account transfer, runbook | Full runbook, project closure | 5 |

### 3.2 Out of Scope
- AI/ML, advanced e-commerce systems, complex image processing.
- Multi-region/DR deployment, complex admin systems, third-party integrations.
- Advanced autoscaling, complex CI/CD pipelines.

### 3.3 Production Roadmap
- Improve operations.
- Strengthen production secrets.
- Add error-handling.
- Deploy & validate in production.
- DR planning.
- Operations handover.

## 4. Estimated AWS Costs (Reference)

| Service | Upfront | Monthly | Region |
|---------|---------|---------|---------|
| S3 | 0.00 USD | 0.26 USD | AP-Singapore |
| CloudFront | 0.00 USD | 0.17 USD | AP-Singapore |
| ACM | 0.00 USD | 0 USD | AP-Singapore |
| Route 53 | 0.00 USD | 0.50–1.00 USD | AP-Singapore |
| Lightsail – DB | 0.00 USD | 10–15 USD | AP-Singapore |
| Cognito | 0.00 USD | 2.00 USD | AP-Singapore |
| Secrets Manager | 0.00 USD | 0.40 USD | AP-Singapore |
| CloudWatch | 0.00 USD | 0.30 USD | AP-Singapore |
| Lightsail – API | 0.00 USD | 5–10 USD | AP-Singapore |

## 5. Project Team
- Product Owner / PM: Nguyễn Duy Hiếu  
- Backend Developer: Lưu Ngọc Ngân Giang  
- Frontend Developers: Nguyễn Huy Hoàng, Trần Hồ Phương Khanh, Tăng Khánh Nhi  
- (Fill detailed contact info as needed)

## 6. Resources & Estimated Costs

| Resource | Responsibility | Rate (USD) / Hour |
| :---- | :---- | :---- |
| Solution Architects \[assigned count\] | - Design AWS infrastructure ecosystem, integrate key services such as S3, CloudFront, Lightsail, ACM, Route 53, and Secrets Manager. - Advise on security and cost optimization strategies. - Conduct comprehensive deployment assessments to ensure best practices. | 12 |
| Engineers \[assigned count\] | - Provision and deploy core infrastructure components including S3, CloudFront, Route 53, ACM, and Lightsail. - Set up CI/CD pipelines and assist with frontend deployment to S3. - Deploy and configure .NET API runtime on AWS Lightsail. - Configure secure credential management using Secrets Manager and set up CloudWatch logging. | 6 |
| Others (Specify) | - Perform rigorous post-deployment validation and integration testing. - Provide ongoing technical consulting and dedicated customer support. | 0 |

\* Refer to "Activities & Deliverables" for phase breakdown.

| Project Phase | Solution Architects | Engineers | Others | Total Hours |
| :---: | :---: | :---: | :---: | :---: |
| S3 + CloudFront | 1 | 2 |  | 3 |
| Lightsail API + DB | 1 | 4 |  | 4 |
| Cognito | 1 | 2 |  | 5 |
| Logging & Monitoring | 1 | 1 |  | 3 |
| Total Hours | 4 | 12 |  | 15 |
| Total Cost |  |  |  |  |

Budget estimates available at:  
[AWS Pricing Calculator](https://calculator.aws/#/estimate?id=621f38b12a1ef026842ba2ddfe46ff936ed4ab01)

| Service Name | Upfront Cost | Monthly Cost | Description | Region | Configuration Summary |
| :---- | :---- | :---- | :---- | :---- | :---- |
| AWS Secrets Manager | 0.00 USD | 0.13 USD | DB password management | Asia Pacific (Singapore) | Secrets (1), Average rotation (10 days), API calls (1/mo) |
| AWS Certificate Manager | 15.00 USD | 0.00 USD | SSL Certificate | Asia Pacific (Singapore) | FQDNs (1) |
| Amazon S3 | 0.00 USD | 0.03 USD | Host React + store images | Asia Pacific (Singapore) | 1 GB storage, no data transfer |
| Amazon Route 53 | 0.00 USD | 3.50 USD | Domain management | Asia Pacific (Singapore) | Hosted Zone (1) |
| Amazon Lightsail | 0.00 USD | 3.20 USD | API + Database Server | Asia Pacific (Singapore) | 1 instance, 100GB storage, 250GB bandwidth |
| Amazon Cognito | 0.00 USD | 0.05 USD | User Login/Auth | Asia Pacific (Singapore) | MAU (1), security features enabled |
| Amazon CloudWatch | 0.00 USD | 0.30 USD | API Logging | Asia Pacific (Singapore) | Metrics (1), widget image (1), custom metrics (1) |
| Amazon CloudFront | 0.00 USD | 0.00 USD | Frontend CDN | Asia Pacific (Singapore) | Free tier |

Allocation of cost contributions among Partner, Customer, AWS:

| Party | Contribution (USD) | % of Total |
| :---- | :---- | :---- |
| Customer |  |  |
| Partner |  |  |
| AWS |  |  |

## 7. Acceptance Criteria
- Website runs stably on the actual domain.
- API fully connected to the database.
- Image upload works properly.
- CloudWatch logging & Cognito login operate correctly.
- Approved by client/project owner.

## DOCX TEMPLATE FILE:  

[**DOWNLOAD Proposal (DOCX)**](https://drive.google.com/drive/folders/1TLXOU4XDvSqv1hfWYhXhWilc5G53iN2H?usp=sharing)
