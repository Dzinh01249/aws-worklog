---
title: "Tuần 5"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

Mục tiêu tuần 5:
- Khởi tạo project Backend Spring Boot và thiết lập mạng ảo bảo mật AWS VPC.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Sử dụng Spring Initializr tạo dự án Java. Cấu hình Multi-tier (Controller, Service, Repository). | 15/05/2026 | 16/05/2026 | [Spring Boot](https://spring.io/projects/spring-boot) |
| 2 | Đăng nhập AWS, tạo Amazon VPC dải IP `10.0.0.0/16` kèm 2 Public và 2 Private Subnets. | 17/05/2026 | 18/05/2026 | [Amazon VPC](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html) |
| 3 | Cấu hình Internet Gateway cho Public Subnet và NAT Gateway cho Private Subnet. | 19/05/2026 | 19/05/2026 | [NAT Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html) |
| 4 | Tạo các Route Tables điều hướng mạng tương ứng cho từng vùng Subnet. | 20/05/2026 | 20/05/2026 | [Route Tables](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html) |
| 5 | Thiết lập Security Groups: chặn toàn bộ port không cần thiết, chỉ mở port 80/443 ở public. | 21/05/2026 | 21/05/2026 | [Security Groups](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html) |

Thành tích tuần 5:

- Khung mạng hệ thống (Network Architecture) đã sẵn sàng và bảo mật.
