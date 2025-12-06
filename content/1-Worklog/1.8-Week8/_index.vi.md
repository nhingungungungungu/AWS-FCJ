---
title: "Worklog Tuần 8"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Tự động hóa Hạ tầng: Tái tạo lại kiến trúc mạng (VPC) và máy chủ (EC2) bằng code.
* Hiểu bản chất: Nắm vững cấu trúc CloudFormation (Parameters, Resources, Outputs).
* Công cụ Hiện đại: Làm quen với AWS CDK và quy trình cdk init, cdk synth, cdk deploy.
* Quản lý Vòng đời: Thực hành xóa sạch (Destroy) và tạo lại (Deploy) toàn bộ stack trong vài phút.

### Các công việc cần triển khai trong tuần này:
| Task ID | Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T8.1 | 2 | **CloudFormation - Write Template:** <br> - Viết file `vpc.yaml` định nghĩa VPC <br> - Bao gồm: Subnet, Internet Gateway, Route Table | 27/10/2025 | 27/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T8.2 | 2 | **CloudFormation - Deploy Stack:** <br> - Upload file lên CloudFormation Console <br> - Tạo stack `FCJ-VPC-Stack` <br> - Kiểm tra tài nguyên được tạo | 27/10/2025 | 28/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T8.3 | 3 | **CDK - Init Project:** <br> - Cài đặt AWS CDK <br> - Khởi tạo dự án TypeScript: `cdk init app --language typescript` | 28/10/2025 | 28/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T8.4 | 4 | **CDK - Define S3:** <br> - Trong `lib/stack.ts`, thêm code tạo S3 Bucket <br> - Bật versioning và encryption (L2 Construct) | 29/10/2025 | 29/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T8.5 | 5 | **CDK - Deploy:** <br> - Chạy `cdk deploy` <br> - Quan sát quá trình tạo ChangeSet và thực thi | 30/10/2025 | 30/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T8.6 | 5 | **IaC - Drift Detection:** <br> - Thay đổi thủ công tag của S3 bucket trên Console <br> - Chạy Drift Detection để phát hiện sự sai lệch | 30/10/2025 | 31/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T8.7 | 6 | **IaC - Cleanup:** <br> - Chạy `cdk destroy` để xóa toàn bộ tài nguyên <br> - Đảm bảo không sót chi phí | 31/10/2025 | 31/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 8:

* **Tốc độ:**
  * Có thể dựng lại toàn bộ môi trường mạng chỉ trong 2 phút chạy lệnh
  * Thay vì 30 phút click chuột thủ công
  * Giảm thiểu human errors

* **Kiểm soát:**
  * Code hạ tầng được lưu trong Git
  * Xem lại lịch sử thay đổi (Ai đã sửa Subnet? Tại sao?)
  * Code review cho infrastructure changes
  * Version control cho infrastructure

* **Trải nghiệm:**
  * CDK trực quan và viết ít code hơn CloudFormation thuần túy
  * Nhờ các Construct cấp cao (L2, L3)
  * Có type checking và autocomplete
  * Dễ test infrastructure code

* **Kỹ năng:**
  * Hiểu về Infrastructure as Code (IaC)
  * Nắm vững CloudFormation template structure
  * Thành thạo AWS CDK với TypeScript
  * Biết cách sử dụng Drift Detection

* Sử dụng AWS CLI để thực hiện các thao tác cơ bản như:

  * Kiểm tra thông tin tài khoản & cấu hình
  * Lấy danh sách region
  * Xem dịch vụ EC2
  * Tạo và quản lý key pair
  * Kiểm tra thông tin dịch vụ đang chạy
  * ...

* Có khả năng kết nối giữa giao diện web và CLI để quản lý tài nguyên AWS song song.
* ...


