---
title: "Worklog Tuần 12"
date: 2025-11-28
weight: 1
chapter: false
pre: " <b> 1.12 </b> "
---
### Mục tiêu Tuần 12:

* Deploy backend API lên Lightsail và xử lý lỗi sau triển khai.
* Xác nhận end-to-end: auth, upload, review, account, DB.

### Các nhiệm vụ trong Tuần 12

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
|-----|-----------|--------------|-----------------|--------------------|
| 1   | Build & publish backend; cấu hình systemd/reverse proxy trên Lightsail. | 24/11/2025 | 24/11/2025 | Ghi chú triển khai |
| 2   | Chạy migration, seed dữ liệu cơ bản; kiểm tra kết nối và healthcheck. | 25/11/2025 | 25/11/2025 | Đề xuất `AWSJewelry` |
| 3   | Cấu hình domain + HTTPS (ACM/CloudFront) cho API; cập nhật CORS. | 26/11/2025 | 26/11/2025 | Tài liệu AWS |
| 4   | Regression test (auth, account, review, upload); theo dõi log/metrics. | 27/11/2025 | 27/11/2025 | Postman, CloudWatch |
| 5   | Sửa lỗi sau deploy (CORS, lệch thời gian JWT, đường dẫn file, env); retest. | 28/11/2025 | 28/11/2025 | CloudWatch logs |

### Thành tựu Tuần 12:
* Backend deploy lên Lightsail với reverse proxy + systemd; healthcheck đạt.
* Migration PostgreSQL chạy thành công; secrets/env đồng bộ cho Cognito, S3, DB.
* HTTPS và CORS tinh chỉnh cho CloudFront/SPA; domain truy cập end-to-end.
* Regression pass cho login, account, review, upload.
* Khắc phục xong lỗi CORS, lệch hạn JWT, path S3 sau triển khai.