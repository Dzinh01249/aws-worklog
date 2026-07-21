---
title: "Tuần 9"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

Mục tiêu tuần 9:
- Triển khai tính năng High Availability (HA) với Application Load Balancer (ALB).

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Di chuyển máy chủ EC2 từ Public vào sâu Private Subnet để tăng bảo mật. | 12/06/2026 | 13/06/2026 | [VPC Subnets](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html) |
| 2 | Tạo Target Group và đăng ký các máy chủ EC2 backend vào nhóm này. | 14/06/2026 | 14/06/2026 | [Target Groups](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-target-groups.html) |
| 3 | Tạo Application Load Balancer (ALB) nằm ở Public Subnet để tiếp nhận traffic từ ngoài. | 15/06/2026 | 15/06/2026 | [AWS ALB](https://aws.amazon.com/elasticloadbalancing/application-load-balancer/) |
| 4 | Thiết lập cơ chế Health Checks ping vào `/api/v1/health` để ALB nhận biết máy chủ lỗi. | 16/06/2026 | 17/06/2026 | [ALB Health Checks](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/target-group-health-checks.html) |
| 5 | Đổi biến môi trường API Backend trên Frontend sang dùng DNS của Load Balancer. | 18/06/2026 | 18/06/2026 | [Vite Env Variables](https://vitejs.dev/guide/env-and-mode) |

Thành tích tuần 9:

- Ứng dụng sở hữu kiến trúc chịu tải, loại bỏ Single Point of Failure.
