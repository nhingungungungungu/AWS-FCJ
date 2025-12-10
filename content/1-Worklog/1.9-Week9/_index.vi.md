---
title: "Worklog Tuần 9"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Làm chủ Docker và các nền tảng điều phối container hàng đầu của AWS: ECS và EKS.
* Triển khai, tự động hóa và vận hành ứng dụng container bằng CI/CD.
* Hiểu lựa chọn giữa ECS (Fargate) và EKS (Kubernetes) cho các kịch bản khác nhau.

### Các công việc cần triển khai trong tuần này:

| Task ID | Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T9.1 | 1 | **Docker Fundamentals:** <br> - Containerization with Docker <br> - Viết Dockerfile tối ưu (Multi-stage build) <br> - Tạo ECR repo và docker push image private | 01/11/2025 | 01/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T9.2 | 2 | **Amazon ECS & Fargate:** <br> - Triển khai ECS với Fargate <br> - Định nghĩa Task (CPU/RAM) <br> - Tạo Service và tích hợp ALB | 02/11/2025 | 02/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T9.3 | 3 | **ECS với IaC (CDK):** <br> - Áp dụng CDK cho ECS <br> - Sử dụng ApplicationLoadBalancedFargateService (L3 Construct) | 03/11/2025 | 03/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T9.4 | 4 | **Amazon EKS – Setup:** <br> - Khởi tạo EKS cluster (eksctl / CDK EKS Blueprints) <br> - Cấu hình Managed Node Groups | 04/11/2025 | 04/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T9.5 | 5 | **Triển khai ứng dụng trên EKS:** <br> - Viết manifests (Deployment, Service, Ingress) <br> - Cài AWS Load Balancer Controller để tạo ALB từ Ingress | 05/11/2025 | 05/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T9.6 | 6 | **CI/CD cho Container:** <br> - Xây dựng pipeline: CodeCommit → CodeBuild → CodeDeploy <br> - Thực hành Blue/Green deployment cho ECS/EKS | 06/11/2025 | 06/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T9.7 | 7 | **ROSA – Red Hat OpenShift on AWS:** <br> - Tìm hiểu ROSA (Managed OpenShift) <br> - Trường hợp sử dụng: migrate OpenShift on-prem → AWS | 07/11/2025 | 07/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |

### Kết quả đạt được tuần 9:

* Hiểu sâu Dockerfile tối ưu và quản lý image private trên ECR.  
* Triển khai container serverless bằng ECS Fargate và tích hợp ALB.  
* Tự động hóa triển khai ECS bằng CDK (L3 Construct).  
* Khởi tạo EKS cluster, quản lý Node Groups và deploy ứng dụng K8s bằng manifest.  
* Thiết lập CI/CD cho workflow container và thực hành Blue/Green deployment.  
* Nắm được use-case ROSA cho doanh nghiệp dùng OpenShift on-premise.
