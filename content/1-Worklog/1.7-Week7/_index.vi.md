---
title: "Worklog Tuần 7"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

Mục tiêu tuần 7:
- Mục tiêu trọng tâm là đưa ứng dụng Backend đã code xong từ máy local lên chạy thực tế trên môi trường đám mây AWS. Quá trình này đòi hỏi việc thiết lập một máy chủ ảo EC2 chạy Linux, cài đặt môi trường Java, và cấu hình để ứng dụng chạy ổn định, tự phục hồi.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 29/05 | Sử dụng AWS Console để khởi tạo một máy chủ ảo Amazon EC2 (Elastic Compute Cloud) sử dụng hệ điều hành Ubuntu Server. Chọn instance type `t3.micro` phù hợp với Free Tier. Khởi tạo và tải về an toàn một SSH Key Pair (file `.pem`). Gắn máy chủ EC2 này vào Public Subnet (để dễ dàng quản lý trong giai đoạn test) và áp dụng Security Group đã thiết kế ở tuần 5. Kết nối (SSH) vào máy chủ thông qua Terminal/PuTTY. | 29/05 | 30/05 | |
| 31/05 | Thực hiện cập nhật các package hệ thống của Ubuntu bằng `apt update` và `apt upgrade`. Tiến hành cài đặt môi trường thực thi Java (Java Runtime Environment - JRE 17) thông qua OpenJDK. Soạn thảo một file cấu hình service (Systemd Unit File) nằm ở `/etc/systemd/system/pet-resort.service`. File này chỉ định cách hệ điều hành Linux sẽ khởi động file `.jar` của Spring Boot, quản lý logs, và đặc biệt là tự động khởi động lại ứng dụng nếu bị crash hoặc khi máy chủ bị reboot. | 31/05 | 01/06 | |
| 02/06 | Quay lại môi trường phát triển local, sử dụng Maven (`mvn clean package`) để đóng gói ứng dụng Spring Boot thành một file thực thi duy nhất (`.jar`). Sử dụng lệnh SCP (Secure Copy) hoặc các công cụ đồ họa như WinSCP/FileZilla kết hợp với SSH Key để upload an toàn file `.jar` có dung lượng hàng chục MB này từ máy tính cá nhân lên thư mục `/opt/pet-resort/` trên máy chủ ảo EC2. | 02/06 | 03/06 | |
| 04/06 | Kích hoạt và khởi động ứng dụng thông qua systemd bằng các lệnh `systemctl enable` và `systemctl start`. Theo dõi quá trình khởi động và đọc log trực tiếp thông qua lệnh `journalctl -f`. Kiểm tra cấu hình kết nối từ máy EC2 đến máy chủ cơ sở dữ liệu RDS trong Private Subnet. Cuối cùng, thực hiện gọi thử các API từ một trình duyệt/Postman bên ngoài internet thông qua địa chỉ Public IP của máy EC2 để xác minh hệ thống hoạt động hoàn hảo. | 04/06 | 04/06 | |

Thành tích tuần 7:

- Chuyển đổi thành công một ứng dụng Backend từ môi trường phát triển cục bộ sang chạy thực tế trên máy chủ ảo Linux (EC2).
- Ứng dụng được thiết lập chạy nền như một system service chuyên nghiệp, có khả năng tự động phục hồi khi gặp lỗi.
- Hiểu rõ quy trình đóng gói, truyền tải file an toàn và quản trị server Linux ở mức cơ bản.
