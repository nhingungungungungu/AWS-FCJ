---
title: "Worklog Week 12"
date: 2025-11-28
weight: 1
chapter: false
pre: " <b> 1.12. </b> "
---
### Week 12 Goals:

* Deploy backend API to Lightsail and stabilize post-deployment issues.
* Validate end-to-end flows: auth, uploads, reviews, accounts, and database operations.

### Tasks for Week 12

| Day | Task | Start Date | End Date | Reference Material |
|-----|------|------------|----------|--------------------|
| 1   | Build and publish backend artifacts; configure systemd/reverse proxy on Lightsail. | 24/11/2025 | 24/11/2025 | Deployment notes |
| 2   | Run DB migrations and seed baseline data; verify connectivity and health checks. | 25/11/2025 | 25/11/2025 | `AWSJewelry` proposal |
| 3   | Configure domain + HTTPS (ACM/CloudFront) for API; update CORS allowed origins. | 26/11/2025 | 26/11/2025 | AWS docs |
| 4   | Perform regression tests (auth, account, review, upload); monitor logs/metrics. | 27/11/2025 | 27/11/2025 | Postman, CloudWatch |
| 5   | Fix post-deploy issues (CORS, JWT clock skew, file path, env vars) and retest. | 28/11/2025 | 28/11/2025 | CloudWatch logs |

### Achievements of Week 12:
* Backend deployed to Lightsail with reverse proxy + systemd service; health checks green.
* PostgreSQL migrations applied; secrets/env values aligned for Cognito, S3, DB access.
* HTTPS and CORS tuned for CloudFront/SPA; domain reachable end-to-end.
* Regression tests passed for login, account, review, and image upload flows.
* Post-deployment fixes addressed CORS headers, JWT expiry skew, and S3 path inconsistencies.