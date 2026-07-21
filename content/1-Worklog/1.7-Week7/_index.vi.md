---
title: "Tuần 7"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

Mục tiêu tuần 7:
- Deploy ứng dụng Spring Boot lên máy chủ ảo EC2.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Khởi tạo EC2 Instance (Ubuntu Server) và tải SSH Key Pair để kết nối. | 29/05/2026 | 30/05/2026 | [Amazon EC2 Setup](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html) |
| 2 | Cập nhật OS, cài đặt môi trường Java (OpenJDK 17) trên máy chủ EC2. | 31/05/2026 | 01/06/2026 | [Install Java Ubuntu](https://ubuntu.com/tutorials/install-jre) |
| 3 | Đóng gói ứng dụng thành file `.jar` bằng Maven và upload lên EC2 bằng lệnh SCP. | 02/06/2026 | 02/06/2026 | [Maven Package](https://maven.apache.org/guides/getting-started/) |
| 4 | Tạo file Systemd Service (`.service`) để cấu hình cho app chạy ngầm và tự khởi động lại khi crash. | 03/06/2026 | 03/06/2026 | [Systemd Services](https://linuxhandbook.com/create-systemd-services/) |
| 5 | Khởi động service, check log bằng `journalctl` và verify API hoạt động từ Postman. | 04/06/2026 | 04/06/2026 | [Journalctl Guide](https://www.loggly.com/ultimate-guide/using-journalctl/) |

Thành tích tuần 7:

- Backend đã chạy ổn định 24/7 dưới dạng Linux service.
