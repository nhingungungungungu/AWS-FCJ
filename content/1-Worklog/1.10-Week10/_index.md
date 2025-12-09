---
title: "Worklog Week 10"
date: 2025-11-14
weight: 1
chapter: false
pre: " <b> 1.10. </b> "
---
### Week 10 Goals:

* Deliver Review service for jewelry products with Cognito-authenticated users.
* Wire persistence and rating aggregation to support storefront UI.

### Tasks for Week 10

| Day | Task | Start Date | End Date | Reference Material |
|-----|------|------------|----------|--------------------|
| 1   | Design review schema (rating, comment, userId, productId, timestamps). | 10/11/2025 | 10/11/2025 | `AWSJewelry` proposal |
| 2   | Implement Review service endpoints (create, update, list, delete) with JWT auth. | 11/11/2025 | 11/11/2025 | API guidelines |
| 3   | Add rating aggregation per product and pagination/filtering for storefront. | 12/11/2025 | 12/11/2025 | Product requirements |
| 4   | Integrate audit logging (user, IP, timestamp) and validation rules. | 13/11/2025 | 13/11/2025 | Team standards |
| 5   | Frontend smoke tests: submit/edit/delete review from SPA against dev API. | 14/11/2025 | 14/11/2025 | Postman/UI tests |

### Achievements of Week 10:
* Review entity and migrations added with rating/comment fields tied to products and Cognito user IDs.
* CRUD endpoints secured via JWT middleware; validation prevents duplicate reviews per user/product.
* Rating averages computed and exposed for product listing/detail pages.
* Audit logging captured for moderation; pagination and sorting ready for storefront consumption.