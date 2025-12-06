---
title: "Worklog Tuần 10"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Xây dựng API: Tạo RESTful API cho ứng dụng quản lý sách (Book Store).
* Logic Serverless: Viết các hàm Lambda thực hiện CRUD (Create, Read, Update, Delete).
* Lưu trữ NoSQL: Thiết kế bảng DynamoDB hiệu năng cao.
* Tích hợp: Kết nối API Gateway -> Lambda -> DynamoDB.

### Các công việc cần triển khai trong tuần này:
| Task ID | Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T10.1 | 2 | **DynamoDB - Create Table:** <br> - Tạo bảng `Books` với Partition Key là ISBN (String) <br> - Cấu hình chế độ On-Demand Capacity | 10/11/2025 | 10/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T10.2 | 2 | **IAM - Lambda Role:** <br> - Tạo Role cho Lambda <br> - Quyền: PutItem, GetItem, Scan trên bảng Books <br> - Quyền ghi log CloudWatch | 10/11/2025 | 11/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T10.3 | 3 | **Lambda - Function Logic:** <br> - Viết hàm `add_book` (Python) nhận JSON và ghi DynamoDB <br> - Viết hàm `get_books` để đọc dữ liệu | 11/11/2025 | 12/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T10.4 | 4 | **API Gateway - REST API:** <br> - Tạo API `BookStoreAPI` <br> - Tạo resource `/books` và method POST, GET <br> - Tích hợp với Lambda functions | 12/11/2025 | 13/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T10.5 | 5 | **API Gateway - Deploy:** <br> - Deploy API ra Stage `dev` <br> - Lấy Invoke URL | 13/11/2025 | 14/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T10.6 | 6 | **Testing - Postman:** <br> - Gửi POST request thêm sách <br> - Gửi GET request kiểm tra danh sách trả về | 14/11/2025 | 14/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 10:

* **Sản phẩm:**
  * Một backend API hoàn chỉnh hoạt động
  * Không cần bất kỳ máy chủ nào (No EC2)
  * Truly serverless architecture

* **Hiệu năng:**
  * Tốc độ phản hồi cực nhanh (< 100ms)
  * Khả năng chịu tải hàng nghìn request/giây mặc định
  * Auto scaling không cần cấu hình

* **Chi phí:**
  * Gần như $0 trong giai đoạn phát triển
  * Nhờ Free Tier của Lambda và DynamoDB
  * Pay-per-request model

* **Kiến trúc:**
  * Hiểu về Microservices architecture
  * Event-driven programming
  * API-first design
  * NoSQL data modeling


