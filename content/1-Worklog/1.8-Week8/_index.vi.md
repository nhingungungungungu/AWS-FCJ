---
title: "Week 8 Worklog"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Tối ưu hóa chi phí (FinOps) bằng công cụ theo dõi, phân tích và tối ưu tài nguyên.
* Xây dựng mô hình mạng nâng cao cho môi trường đa VPC và phân tách workload.
* Tăng mức độ chủ động trong quản trị hạn ngạch, giám sát mạng và phân quyền thanh toán.

### Tasks to be carried out this week:

| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T8.1 | 22 | **Cost Explorer & CUR – Cost Analysis:** <br> - Phân tích chi phí theo Service/Region/Tag <br> - Kích hoạt Cost & Usage Report (CUR) <br> - Truy vấn CUR bằng Athena | 22/10/2025 | 22/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.2 | 23 | **Compute Optimizer – Right-Sizing:** <br> - Phân tích instance over-provisioned <br> - Gợi ý giảm size dựa trên dữ liệu lịch sử <br> - Thu thập thêm RAM metrics qua CloudWatch Agent | 23/10/2025 | 23/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.3 | 24 | **Savings Plans & Reserved Instances:** <br> - So sánh Compute SP vs EC2 Instance SP <br> - Lập chiến lược mua SP 1 năm cho Base Load <br> - Phân tích chi phí & mức độ linh hoạt | 24/10/2025 | 24/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.4 | 25 | **Service Quotas – Quản lý hạn ngạch:** <br> - Kiểm tra quota vCPU, VPC, NAT… <br> - Thiết lập cảnh báo khi đạt 80% quota <br> - Tạo yêu cầu tăng hạn mức chủ động | 25/10/2025 | 25/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.5 | 26 | **Transit Gateway – Advanced Networking:** <br> - Kết nối 3 VPC + VPN vào TGW <br> - Thiết kế mô hình Hub-and-Spoke <br> - Cấu hình route tách biệt Dev & Prod | 26/10/2025 | 26/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.6 | 27 | **VPC Flow Logs – Network Monitoring:** <br> - Kích hoạt Flow Logs cho VPC <br> - Phân tích traffic REJECT <br> - Xác định SG/NACL chặn kết nối | 27/10/2025 | 27/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.7 | 28 | **Billing Delegation – Phân quyền Thanh toán:** <br> - Tạo Billing IAM Role cho Finance Team <br> - Áp dụng Separation of Duties <br> - Giới hạn truy cập vào tài nguyên kỹ thuật | 28/10/2025 | 28/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.8 | 29 | **EBS Lifecycle – Snapshot Automation:** <br> - Tự động hóa Snapshot với DLM <br> - Giữ 7 ngày backup gần nhất <br> - Bật Anomaly Detection cho backup | 29/10/2025 | 29/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.9 | 30 | **Tổng kết tháng 10:** <br> - Đánh giá mức độ vận hành chuyên nghiệp <br> - Hệ thống tối ưu, bảo mật, DR-ready <br> - Sẵn sàng cho giai đoạn hiện đại hóa | 30/10/2025 | 30/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |

### Week 8 Achievements:

* Phân tích chi phí chi tiết với Cost Explorer & CUR và truy vấn dữ liệu bằng Athena.  
* Tối ưu hóa tài nguyên EC2 bằng Compute Optimizer dựa trên dữ liệu thực tế.  
* Xây dựng chiến lược tiết kiệm dài hạn với Savings Plans & Reserved Instances.  
* Chủ động kiểm soát hạn ngạch với cảnh báo trước 80% usage.  
* Thiết kế mạng nâng cao với Transit Gateway thay thế mô hình VPC Peering chằng chịt.  
* Giám sát mạng chuyên sâu bằng VPC Flow Logs để xác định lỗi kết nối.  
* Áp dụng phân quyền thanh toán an toàn cho Finance Team.  
* Tự động hóa quản lý Snapshot và phát hiện bất thường backup.  
