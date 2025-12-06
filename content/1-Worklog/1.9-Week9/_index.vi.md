---
title: "Worklog Tuần 9"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Minh bạch Mạng: Thu thập và phân tích lưu lượng mạng để phát hiện các kết nối bất thường.
* Truy vấn Log: Sử dụng CloudWatch Logs Insights để chạy query trên dữ liệu log khổng lồ.
* Tối ưu Chi phí: Xác định các tài nguyên đang lãng phí và thực hiện "Right Sizing".
* Phân quyền Billing: Cấu hình quyền truy cập Billing cho tài khoản IAM.

### Các công việc cần triển khai trong tuần này:
| Task ID | Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T9.1 | 2 | **VPC - Enable Flow Logs:** <br> - Bật Flow Logs cho VPC <br> - Đích đến: CloudWatch Logs Group `/aws/vpc/flowlogs` | 03/11/2025 | 03/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T9.2 | 2 | **Testing - Generate Deny:** <br> - Thử SSH từ IP không có trong Security Group <br> - Tạo ra các bản ghi REJECT | 03/11/2025 | 04/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T9.3 | 3 | **Logs - Insights Query:** <br> - Viết query đếm số gói tin bị từ chối theo Source IP <br> - `filter action="REJECT" stats count() by srcAddr` | 04/11/2025 | 04/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T9.4 | 4 | **Cost - Compute Optimizer:** <br> - Truy cập Compute Optimizer <br> - Xem khuyến nghị (cần ít nhất 12-24h dữ liệu) | 05/11/2025 | 05/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T9.5 | 5 | **Cost - Cost Explorer:** <br> - Phân tích chi phí theo ngày và dịch vụ <br> - Group by Service <br> - Xác định EC2 hay RDS tốn nhiều tiền nhất | 06/11/2025 | 06/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T9.6 | 6 | **Report & Recommendations:** <br> - Tổng hợp báo cáo chi phí và khuyến nghị tối ưu <br> - Phân tích Flow Logs để tìm vấn đề bảo mật <br> - Đề xuất cải tiến kiến trúc | 07/11/2025 | 07/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 9:

* **Điều tra số:**
  * Đã xác định địa chỉ IP nào đang cố quét port SSH
  * Phát hiện các pattern tấn công
  * Có thể trace được network path

* **Tiết kiệm:**
  * Compute Optimizer chỉ ra instances đang chạy dưới 5% CPU
  * Xác nhận t3.micro phù hợp hoặc có thể gom lại
  * Phát hiện tài nguyên không sử dụng

* **Kỹ năng:**
  * Thành thạo cú pháp query của Logs Insights
  * Kỹ năng quan trọng để xử lý sự cố nhanh
  * Hiểu về VPC Flow Logs format

* **FinOps:**
  * Biết cách phân tích chi phí theo nhiều chiều
  * Hiểu về Cost Allocation Tags
  * Có thể dự báo chi phí hàng tháng


