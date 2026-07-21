---
title: "Tuần 6"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

Mục tiêu tuần 6:
- Tích hợp AWS RDS Database và phát triển API Backend.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 22/05 | Khởi tạo RDS MySQL Multi-AZ đặt bên trong Private Subnet để bảo mật cao nhất. | 22/05 | 23/05 | |
| 24/05 | Tạo Security Group cho RDS (port 3306) chỉ cho phép EC2 Backend kết nối. Cấu hình biến môi trường kết nối DB. | 24/05 | 25/05 | |
| 26/05 | Viết các Entity JPA (`User`, `SpaService`, `Booking`). Thiết kế quan hệ khóa ngoại Database. | 26/05 | 27/05 | |
| 28/05 | Lập trình RESTful API thực hiện CRUD. Khắc phục lỗi N+1 Query trong JPA bằng `@EntityGraph`. | 28/05 | 28/05 | |

Thành tích tuần 6:

- Database RDS đã được bảo vệ và hoạt động ổn định.
- Backend API giao tiếp thành công với Database.
