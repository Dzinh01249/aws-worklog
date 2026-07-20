---
title: "Worklog Tuần 9"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

Mục tiêu tuần 9:
- Thiết lập cơ chế cân bằng tải bằng Application Load Balancer và cấu hình Auto Scaling linh hoạt.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Tạo Target Group đăng ký EC2 Backend, cấu hình Health Check endpoint (/api/health) để theo dõi trạng thái. | 20/06/2026 | 21/06/2026 | |
| 2 | Khởi tạo Application Load Balancer trong Public Subnet, thiết lập Listener Rule phân luồng request đến Target Group. | 22/06/2026 | 23/06/2026 | |
| 3 | Tạo Launch Template từ AMI của EC2 hiện tại, cấu hình Auto Scaling Group với chính sách scale-out/scale-in. | 24/06/2026 | 25/06/2026 | |
| 4 | Mô phỏng tải nặng bằng công cụ stress test, quan sát Auto Scaling tự động cấp phát instance mới. | 26/06/2026 | 27/06/2026 | |

Thành tích tuần 9:

- Backend có khả năng chịu tải cao và tự phục hồi nhờ ALB + Auto Scaling.
- Health Check tự động loại bỏ instance lỗi khỏi nhóm phục vụ.
