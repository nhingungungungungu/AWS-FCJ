---
title: "Worklog Tuần 8"
date: 2025-10-31
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---
### Mục tiêu Tuần 8:

* Triển khai luồng xác thực JWT với Amazon Cognito cho backend.
* Hoàn thiện Account service sử dụng thuộc tính người dùng Cognito và domain dự án.

### Các nhiệm vụ trong Tuần 8

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
|-----|-----------|--------------|-----------------|--------------------|
| 1   | Tạo Cognito User Pool/App Client; ghi nhận pool ID, client ID, JWKS endpoint. | 27/10/2025 | 27/10/2025 | Tài liệu AWS Cognito |
| 2   | Tích hợp middleware xác thực JWT (public keys Cognito, kid rotation, audience). | 28/10/2025 | 28/10/2025 | AWS SDK docs |
| 3   | Xây Account service: lấy/cập nhật hồ sơ, đăng ký gắn với Cognito, cập nhật thông tin. | 29/10/2025 | 29/10/2025 | Đề xuất `AWSJewelry` |
| 4   | Ánh xạ role/claim (admin/customer) và bảo vệ route bằng middleware/attribute. | 30/10/2025 | 30/10/2025 | Quy ước nhóm |
| 5   | Kiểm thử E2E: đăng nhập → nhận token → truy cập API từ React SPA. | 31/10/2025 | 31/10/2025 | Postman collection |

### Thành tựu Tuần 8:
* Cấu hình Cognito User Pool với SPA client; lưu biến môi trường cho triển khai.
* Middleware JWT xác thực chữ ký, audience, issuer, hết hạn bằng JWKS Cognito.
* Account service cung cấp API xem/cập nhật hồ sơ và đăng ký gắn với danh tính Cognito.
* Bảo vệ route theo role admin/customer; CORS không lỗi khi gọi từ frontend.
* Đăng nhập từ React thành công, lấy token và gọi API bảo vệ trọn vẹn.