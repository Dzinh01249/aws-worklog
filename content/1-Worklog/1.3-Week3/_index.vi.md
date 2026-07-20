---
title: "Worklog Tuần 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

Mục tiêu tuần 3:
- Quy hoạch không gian mạng ảo (VPC) và phân vùng rõ ràng giữa các lớp dịch vụ Public/Private.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Khởi tạo Amazon VPC với CIDR Block tùy chỉnh, tạo Internet Gateway gắn vào VPC. | 03/05/2026 | 04/05/2026 | |
| 2 | Phân chia Public Subnet (cho ALB, NAT Gateway) và Private Subnet (cho EC2, RDS, ElastiCache) trên 2 Availability Zone. | 05/05/2026 | 06/05/2026 | |
| 3 | Cấu hình Route Table cho từng lớp Subnet, thiết lập NAT Gateway để Private Subnet truy cập internet một chiều. | 07/05/2026 | 08/05/2026 | |
| 4 | Vẽ lại sơ đồ kiến trúc mạng chi tiết bao gồm luồng dữ liệu vào/ra giữa các Subnet. | 09/05/2026 | 10/05/2026 | |

Thành tích tuần 3:

- Hạ tầng mạng VPC hoàn chỉnh với phân vùng Multi-AZ rõ ràng.
- Luồng traffic an toàn: Internet → Public Subnet → Private Subnet.
