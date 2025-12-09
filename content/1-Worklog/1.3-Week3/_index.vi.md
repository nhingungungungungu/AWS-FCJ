---
title: "Worklog Tuần 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Chuyển đổi từ việc tự quản lý cơ sở dữ liệu trên EC2 sang sử dụng các dịch vụ cơ sở dữ liệu được quản lý (Managed Database) như Amazon RDS và DynamoDB nhằm giảm tải vận hành.
* Nắm vững mô hình Multi-AZ, cơ chế sao chép và quy trình failover của RDS.
* Hiểu và thao tác với cơ sở dữ liệu NoSQL DynamoDB, bao gồm thiết kế bảng, thao tác đọc/ghi và sử dụng Indexes.
* Tăng tốc ứng dụng bằng bộ nhớ đệm (Caching) thông qua ElastiCache.
* Tổng hợp kiến thức để xây dựng kiến trúc Web Application có tính sẵn sàng cao (Highly Available).
* Làm quen với AWS Directory Services để mô phỏng môi trường doanh nghiệp.

### Các công việc cần triển khai trong tuần này:
| Task ID | Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T3.1 | 15 | **RDS – Relational Database:** <br> - Triển khai Amazon RDS (MySQL hoặc PostgreSQL) <br> - Kích hoạt Multi-AZ Deployment <br> - Phân tích cơ chế sao chép đồng bộ & failover tự động | 15/09/2025 | 15/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T3.2 | 16 | **RDS – Vận hành & Kết nối:** <br> - Cấu hình Security Group chỉ cho phép EC2 truy cập RDS <br> - Tùy chỉnh Parameter Groups <br> - Cấu hình Automated Backup & tạo Manual Snapshot <br> - Kiểm thử Restore DB để đánh giá RPO | 16/09/2025 | 16/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T3.3 | 17 | **DynamoDB – NoSQL Cơ bản:** <br> - Tìm hiểu tư duy NoSQL <br> - Tạo bảng Users với Partition Key = UserId <br> - So sánh Provisioned vs On-Demand Capacity <br> - Chọn On-Demand cho môi trường dev | 17/09/2025 | 17/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T3.4 | 18 | **DynamoDB – Nâng cao:** <br> - Thực hành PutItem, GetItem, Query, Scan <br> - Đánh giá hiệu năng Query vs Scan <br> - Tạo Global Secondary Index (GSI) để truy vấn theo Email | 18/09/2025 | 18/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T3.5 | 19 | **ElastiCache – In-Memory Cache:** <br> - Triển khai ElastiCache Redis <br> - Áp dụng chiến lược Lazy Loading <br> - Đặt Redis cluster trong Private Subnet | 19/09/2025 | 19/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T3.6 | 20 | **Web Architecture – Highly Available:** <br> - Kết hợp EC2 + RDS Multi-AZ + S3 <br> - Triển khai Application Load Balancer (ALB) <br> - Mô phỏng failover khi 1 AZ gặp sự cố | 20/09/2025 | 20/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T3.7 | 21 | **Directory Services:** <br> - Tìm hiểu AWS Managed Microsoft AD <br> - Tích hợp Windows EC2 vào Domain <br> - Áp dụng GPO để quản lý tập trung | 21/09/2025 | 21/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |

### Kết quả đạt được tuần 3:

* **Cơ sở dữ liệu quan hệ (RDS):**
  * Triển khai thành công DB MySQL/PostgreSQL.
  * Hiểu và kiểm thử cơ chế Multi-AZ Failover.
  * Thiết lập Parameter Groups và cấu hình Backup hoàn chỉnh.

* **Cơ sở dữ liệu NoSQL:**
  * Tạo DynamoDB table đúng chuẩn Partition Key.
  * Phân biệt rõ giữa Query và Scan về chi phí & hiệu năng.
  * Xây dựng GSI để truy vấn linh hoạt hơn.

* **Caching:**
  * Tích hợp Redis để giảm tải truy vấn RDS.
  * Ứng dụng chiến lược Lazy Loading cho hiệu suất tối ưu.

* **Kiến trúc Web HA:**
  * EC2 đa AZ + RDS Multi-AZ + S3 + ALB vận hành đồng bộ.
  * Mô phỏng failover thành công khi 1 AZ ngừng hoạt động.

* **Directory Services:**
  * Hiểu kiến trúc và use-case của AWS Managed Microsoft AD.
  * Tích hợp Windows EC2 vào Domain và áp dụng GPO cơ bản.

* **Tổng kết:**
  * Hoàn thiện nền tảng Database & Application Architecture.
  * Sẵn sàng bước sang tuần 4 với chủ đề Network Scaling, Auto Scaling và Monitoring.
