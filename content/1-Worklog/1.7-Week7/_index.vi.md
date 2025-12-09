---
title: "Worklog Tuần 7"
date: 2025-10-24
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---
### Mục tiêu Tuần 7:

* Khởi tạo repository backend AWS Jewelry và cấu trúc dự án lõi.
* Định nghĩa domain chung (model, enum, payload, utils, API constants) và bật CORS cho SPA CloudFront.

### Các nhiệm vụ trong Tuần 7

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
|-----|-----------|--------------|-----------------|--------------------|
| 1   | Khởi tạo repo Git, thiết lập cấu trúc thư mục (API, Models, Utils, Payload). | 20/10/2025 | 20/10/2025 | Đề xuất `AWSJewelry` |
| 2   | Định nghĩa entity/enum cho sản phẩm, đơn hàng, người dùng; thêm DTO/payload. | 21/10/2025 | 21/10/2025 | Đề xuất `AWSJewelry` |
| 3   | Thêm API constants, mã lỗi, response wrapper; nối helper dùng chung (validation, mapping). | 22/10/2025 | 22/10/2025 | Quy ước nhóm |
| 4   | Cấu hình CORS toàn cục cho domain CloudFront và localhost dev. | 23/10/2025 | 23/10/2025 | Tài liệu AWS |
| 5   | Rà soát nội bộ cấu trúc; chuẩn hóa naming và layout thư mục. | 24/10/2025 | 24/10/2025 | Codebase |

### Thành tựu Tuần 7:
* Scaffold repo với phân tách rõ Models, Payloads, Enums, Utils, API constants bám sát yêu cầu AWS Jewelry.
* CORS cấu hình cho CloudFront/S3 frontend và localhost, cho phép SPA gọi API an toàn.
* Helper chung (response envelope, xử lý lỗi, mapping/validation) được gom trung tâm giảm trùng lặp.
* Bộ domain cơ bản sẵn sàng cho các bước auth, upload và service tiếp theo.