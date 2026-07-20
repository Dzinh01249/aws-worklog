---
title: "Worklog Tuần 11"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

Mục tiêu tuần 11:
- Xây dựng hệ thống giám sát vận hành bằng Amazon CloudWatch và thiết lập cảnh báo tự động qua SNS.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Cài đặt CloudWatch Agent trên EC2, thu thập metrics: CPU Utilization, Memory Usage, Disk I/O. | 06/07/2026 | 07/07/2026 | |
| 2 | Tạo CloudWatch Dashboard tổng hợp hiển thị trạng thái toàn bộ hệ thống: EC2, RDS, ElastiCache, ALB. | 08/07/2026 | 09/07/2026 | |
| 3 | Thiết lập CloudWatch Alarms cho các ngưỡng quan trọng: CPU > 80%, DB Connection > 90%, Error Rate tăng đột biến. | 10/07/2026 | 11/07/2026 | |
| 4 | Tạo SNS Topic và đăng ký email nhận thông báo, kiểm tra luồng cảnh báo tự động khi alarm kích hoạt. | 12/07/2026 | 13/07/2026 | |

Thành tích tuần 11:

- Dashboard giám sát tập trung giúp nhóm theo dõi sức khỏe hệ thống real-time.
- Cảnh báo tự động qua email khi phát hiện bất thường về tài nguyên.
