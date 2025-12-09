---
title: "Worklog Tuần 10"
date: 2025-11-14
weight: 1
chapter: false
pre: " <b> 1.10. </b> "
---
### Mục tiêu Tuần 10:

* Hoàn thiện Review service cho sản phẩm trang sức với người dùng xác thực Cognito.
* Gắn lưu trữ và tính trung bình điểm đánh giá phục vụ giao diện storefront.

### Các nhiệm vụ trong Tuần 10

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
|-----|-----------|--------------|-----------------|--------------------|
| 1   | Thiết kế schema review (rating, comment, userId, productId, timestamps). | 10/11/2025 | 10/11/2025 | Đề xuất `AWSJewelry` |
| 2   | Implement endpoint Review (tạo/sửa/xem/xóa) với JWT auth. | 11/11/2025 | 11/11/2025 | API guidelines |
| 3   | Thêm tổng hợp điểm trung bình theo sản phẩm, phân trang/lọc cho storefront. | 12/11/2025 | 12/11/2025 | Yêu cầu sản phẩm |
| 4   | Tích hợp audit log (user, IP, timestamp) và rule validation. | 13/11/2025 | 13/11/2025 | Chuẩn nhóm |
| 5   | Smoke test frontend: gửi/chỉnh/sửa/xóa review từ SPA tới dev API. | 14/11/2025 | 14/11/2025 | Postman/UI tests |

### Thành tựu Tuần 10:
* Thêm entity/migration Review với rating/comment gắn product và Cognito user ID.
* CRUD Review bảo vệ bởi JWT middleware; chặn trùng review cùng user/sản phẩm.
* Tính điểm trung bình và expose cho danh sách/chi tiết sản phẩm.
* Audit log ghi nhận cho kiểm duyệt; phân trang/sắp xếp sẵn cho storefront.