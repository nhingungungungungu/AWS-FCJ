---
title: "Worklog Tuần 5"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:
Loại bỏ thao tác thủ công, quản lý hạm đội máy chủ quy mô lớn và mã hóa toàn bộ hạ tầng bằng IaC.

### Các công việc triển khai trong tuần này:

| Task ID | Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T5.1 | 01 | **AWS Systems Manager:** <br> - Đảm bảo EC2 có IAM Role AmazonSSMManagedInstanceCore <br> - Dùng Run Command để chạy lệnh hàng loạt không cần SSH <br> - Kích hoạt Inventory để thu thập dữ liệu audit | 01/10/2025 | 01/10/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T5.2 | 02 | **Session Manager:** <br> - Loại bỏ SSH hoàn toàn, đóng port 22 <br> - Truy cập EC2 qua Session Manager (IAM + HTTPS) <br> - Ghi log phiên làm việc vào S3/CloudWatch Logs | 02/10/2025 | 02/10/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T5.3 | 03 | **CloudFormation – IaC:** <br> - Hiểu IaC và hoạt động của CloudFormation <br> - Viết YAML template tạo VPC + EC2 <br> - Thực hành tạo, update, delete Stack + Drift Detection | 03/10/2025 | 03/10/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T5.4 | 04 | **AWS CDK – Cơ bản:** <br> - Tìm hiểu CDK và Imperative IaC <br> - Sử dụng TypeScript/Python định nghĩa hạ tầng <br> - Tạo VPC bằng L2 Construct | 04/10/2025 | 04/10/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T5.5 | 05 | **AWS CDK – Nâng cao:** <br> - Xây dựng Construct tùy chỉnh (ví dụ: StandardS3Bucket) <br> - Tham gia IaC Workshop, xử lý circular dependencies <br> - Quản lý Context và cấu hình môi trường | 05/10/2025 | 05/10/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T5.6 | 06 | **Tagging & Resource Groups:** <br> - Thiết kế chiến lược Tagging (CostCenter, Env, Owner) <br> - Tạo Resource Groups dựa trên Tag | 06/10/2025 | 06/10/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T5.7 | 07 | **Access Control using Tags – ABAC:** <br> - Tìm hiểu ABAC <br> - Viết IAM Policy cho phép Developer Start/Stop EC2 với tag Env=Dev & Owner=User | 07/10/2025 | 07/10/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |

### Kết quả đạt được tuần 5:

* **Systems Manager & Session Manager:**
  * Quản lý hệ thống không cần SSH.
  * Tăng bảo mật truy cập EC2 với cơ chế IAM + HTTPS.
  * Thu thập log & inventory toàn fleet.

* **Infrastructure as Code:**
  * Tự động hóa hạ tầng bằng CloudFormation.
  * Dùng AWS CDK để viết IaC bằng TypeScript/Python.
  * Xây dựng Construct tái sử dụng trong tổ chức.

* **Quản lý tài nguyên:**
  * Áp dụng chiến lược Tagging chuẩn hóa.
  * Xây dựng Resource Groups dựa trên Tag.
  * Kiểm soát truy cập linh hoạt bằng ABAC.

* **Tổng kết:**
  * Hoàn thiện tư duy DevOps & Operational Excellence.
  * Sẵn sàng chuyển sang tuần 6 với chủ đề: CICD, Lambda và Containers.
