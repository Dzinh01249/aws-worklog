---
title: "Tuần 9"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

Mục tiêu tuần 9:
- Triển khai Load Balancer đảm bảo tính sẵn sàng cao (High Availability).

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 12/06 | Di chuyển máy chủ EC2 vào sâu Private Subnet. Đăng ký EC2 vào Target Group mới. | 12/06 | 13/06 | |
| 14/06 | Tạo Application Load Balancer (ALB) ở Public Subnet để điều phối request tới Backend. | 14/06 | 15/06 | |
| 16/06 | Cấu hình Health Checks (`/api/v1/health`) trên ALB để tự động loại bỏ EC2 bị lỗi khỏi luồng chia tải. | 16/06 | 17/06 | |
| 18/06 | Cập nhật biến môi trường API ở Frontend trỏ về DNS của ALB và test failover. | 18/06 | 18/06 | |

Thành tích tuần 9:

- Thiết lập cân bằng tải chuẩn công nghiệp.
- Hệ thống tự động phát hiện lỗi và duy trì hoạt động.
