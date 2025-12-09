---
title: "Worklog Week 7"
date: 2025-10-24
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---
### Week 7 Goals:

* Bootstrap AWS Jewelry backend repository and core project structure.
* Define shared domain model (entities, enums, payloads, utils, API constants) and enable CORS for SPA frontend on CloudFront.

### Tasks for Week 7

| Day | Task | Start Date | End Date | Reference Material |
|-----|------|------------|----------|--------------------|
| 1   | Initialize Git repository, set up solution folders (API, Models, Utils, Payload). | 20/10/2025 | 20/10/2025 | `AWSJewelry` proposal |
| 2   | Define base entities/enums for jewelry, orders, users; add DTO/payload contracts. | 21/10/2025 | 21/10/2025 | `AWSJewelry` proposal |
| 3   | Add API constants, error codes, response wrappers; wire shared helpers (validation, mapping). | 22/10/2025 | 22/10/2025 | Team guidelines |
| 4   | Configure global CORS for React frontend domain (CloudFront) and local dev origins. | 23/10/2025 | 23/10/2025 | AWS docs |
| 5   | Internal review of base structure; adjust naming conventions and folder layout. | 24/10/2025 | 24/10/2025 | Codebase |

### Achievements of Week 7:
* Repository scaffolded with clear separation for models, payloads, enums, utils, and API constants aligned to AWS Jewelry requirements.
* CORS configured for CloudFront/S3 frontend and localhost to allow authenticated SPA calls.
* Shared helpers (response envelope, error handling, mapping/validation) centralized to reduce duplication.
* Base domain objects ready for subsequent auth, upload, and service layers.