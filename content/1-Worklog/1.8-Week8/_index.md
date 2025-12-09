---
title: "Worklog Week 8"
date: 2025-10-31
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---
### Week 8 Goals:

* Implement Amazon Cognito JWT authentication flow for the backend.
* Deliver Account service endpoints leveraging Cognito user attributes and project domain model.

### Tasks for Week 8

| Day | Task | Start Date | End Date | Reference Material |
|-----|------|------------|----------|--------------------|
| 1   | Set up Cognito User Pool/App Client; capture pool IDs, client IDs, JWKS endpoints. | 27/10/2025 | 27/10/2025 | AWS Cognito docs |
| 2   | Integrate JWT verification middleware (Cognito public keys, kid rotation, audience check). | 28/10/2025 | 28/10/2025 | AWS SDK docs |
| 3   | Build Account service: profile retrieval, registration binding to Cognito, update flows. | 29/10/2025 | 29/10/2025 | `AWSJewelry` proposal |
| 4   | Add role/claim mapping (admin/customer) and protect API routes via middleware attributes. | 30/10/2025 | 30/10/2025 | Team conventions |
| 5   | End-to-end test login → token issuance → API access from React SPA. | 31/10/2025 | 31/10/2025 | Postman collection |

### Achievements of Week 8:
* Cognito User Pool configured with SPA client; environment variables captured for deployment.
* Backend JWT middleware validates signature, audience, issuer, and token expiry using Cognito JWKS.
* Account service exposes profile read/update and registration flows tied to Cognito identities.
* Route protection in place with role-based checks for admin vs. customer endpoints.
* Successful E2E login from React → acquire token → call protected APIs without CORS issues.