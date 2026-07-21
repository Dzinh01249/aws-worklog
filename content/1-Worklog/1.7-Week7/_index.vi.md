---
title: "Tuần 7"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

Mục tiêu tuần 7:
- Deploy ứng dụng Backend Java lên Amazon EC2.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 29/05 | Tạo máy chủ Ubuntu Linux EC2 (`t3.micro`) và cấu hình kết nối SSH (Key Pair). | 29/05 | 30/05 | |
| 31/05 | Cài đặt Java JRE trên EC2. Tạo systemd service file để quản lý Spring Boot chạy nền. | 31/05 | 01/06 | |
| 02/06 | Build file `.jar` bằng Maven và dùng SCP để upload lên server EC2. | 02/06 | 03/06 | |
| 04/06 | Chạy systemctl start ứng dụng. Kiểm tra logs bằng journalctl và test API từ trình duyệt. | 04/06 | 04/06 | |

Thành tích tuần 7:

- Backend đã deploy lên Cloud thành công.
- Ứng dụng chạy tự động và ổn định trên EC2 Linux.
