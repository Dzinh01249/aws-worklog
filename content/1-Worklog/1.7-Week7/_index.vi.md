---
title: "Worklog Tuần 7"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

Mục tiêu tuần 7:
- Triển khai ứng dụng Backend lên Amazon EC2 và cấu hình môi trường máy chủ sản xuất.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Khởi tạo EC2 Instance (Amazon Linux 2023) trong Private Subnet, tạo Key Pair và thiết lập kết nối SSH thông qua Bastion Host. | 04/06/2026 | 05/06/2026 | |
| 2 | Cài đặt môi trường runtime: OpenJDK 17, cấu hình biến môi trường và thông số JVM cho production. | 06/06/2026 | 07/06/2026 | |
| 3 | Build file JAR từ mã nguồn Spring Boot, upload lên EC2 qua SCP và chạy ứng dụng dạng systemd service. | 08/06/2026 | 09/06/2026 | |
| 4 | Kiểm tra kết nối nội bộ từ EC2 đến các dịch vụ khác trong VPC, xác nhận API hoạt động ổn định. | 10/06/2026 | 11/06/2026 | |

Thành tích tuần 7:

- Backend Spring Boot chạy ổn định trên EC2 trong Private Subnet.
- Ứng dụng được quản lý dưới dạng systemd service đảm bảo tự khởi động lại khi gặp sự cố.
