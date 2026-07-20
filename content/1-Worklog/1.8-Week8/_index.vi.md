---
title: "Worklog Tuần 8"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

Mục tiêu tuần 8:
- Khởi tạo Amazon RDS (MySQL) làm lớp lưu trữ quan hệ và tích hợp ElastiCache Redis để tối ưu hiệu năng.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Tạo RDS Instance (MySQL 8.0) trong Private Subnet với chế độ Multi-AZ Standby, cấu hình DB Subnet Group và Security Group. | 12/06/2026 | 13/06/2026 | |
| 2 | Kết nối Spring Boot với RDS qua JDBC, chạy migration script khởi tạo bảng và kiểm thử các thao tác CRUD qua API. | 14/06/2026 | 15/06/2026 | |
| 3 | Khởi tạo ElastiCache Redis Cluster trong Private Subnet, tích hợp Spring Boot với Redis qua Spring Data Redis. | 16/06/2026 | 17/06/2026 | |
| 4 | Thiết lập cache cho danh sách dịch vụ Spa và sản phẩm bán chạy, benchmark hiệu năng trước và sau khi bật Redis. | 18/06/2026 | 19/06/2026 | |

Thành tích tuần 8:

- Cơ sở dữ liệu MySQL hoạt động ổn định trên RDS với cơ chế dự phòng Multi-AZ.
- Giảm đáng kể thời gian phản hồi API nhờ tầng Redis cache.
