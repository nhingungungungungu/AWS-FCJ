---
title: "Worklog Tuần 11"
date: 2025-11-21
weight: 1
chapter: false
pre: " <b> 1.11. </b> "
---
### Mục tiêu Tuần 11:

* Khởi tạo Lightsail instance và PostgreSQL managed cho backend.
* Chuẩn bị pipeline/biến môi trường triển khai API AWS Jewelry.

### Các nhiệm vụ trong Tuần 11

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
|-----|-----------|--------------|-----------------|--------------------|
| 1   | Tạo Lightsail instance (tk giang), cấu hình mạng, SSH key, firewall. | 17/11/2025 | 17/11/2025 | Tài liệu AWS Lightsail |
| 2   | Cấp PostgreSQL Lightsail; tạo DB/user, cấu hình parameter, lưu connection string. | 18/11/2025 | 18/11/2025 | Tài liệu AWS Lightsail |
| 3   | Harden máy (update, firewall), cài runtime và reverse proxy. | 19/11/2025 | 19/11/2025 | Playbook nhóm |
| 4   | Chuẩn bị file môi trường (.env) cho DB, Cognito, S3, Secrets Manager. | 20/11/2025 | 20/11/2025 | Đề xuất `AWSJewelry` |
| 5   | Build thử và deploy test trên Lightsail; kiểm tra kết nối DB và migration. | 21/11/2025 | 21/11/2025 | Ghi chú triển khai |

### Thành tựu Tuần 11:
* Tạo instance Lightsail (user giang) với SSH bảo mật và firewall mở đúng port API.
* Dựng PostgreSQL managed, tạo DB/user riêng; kiểm tra kết nối từ instance thành công.
* Máy chủ được harden, cài stack runtime và reverse proxy sẵn sàng host API.
* Biến môi trường chuẩn bị đầy đủ cho Cognito, S3, DB, Secrets Manager để triển khai.