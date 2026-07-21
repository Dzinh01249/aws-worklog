---
title: "Worklog Tuần 11"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

Mục tiêu tuần 11:
- Với kiến trúc hệ thống đã định hình hoàn chỉnh, mục tiêu tuần này là đảm bảo chất lượng phần mềm thông qua kiểm thử toàn diện (End-to-End Testing), đồng thời thiết lập hệ thống giám sát cảnh báo (Monitoring) và thực hiện chiến dịch tối ưu hóa chi phí vận hành đám mây.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 26/06 | Thực hiện chuỗi các kịch bản kiểm thử End-to-End (E2E) đóng vai người dùng thực. Truy cập trang web qua tên miền chính thức, thực hiện đăng ký tài khoản, duyệt danh sách dịch vụ Spa, thêm vào giỏ hàng, và hoàn tất luồng thanh toán/đặt lịch. Đồng thời, đăng nhập trực tiếp vào MySQL RDS thông qua công cụ DBeaver (thông qua SSH tunnel hoặc Bastion Host) để xác minh xem dữ liệu booking có được lưu trữ chính xác và nhất quán trong các bảng dữ liệu hay không. | 26/06 | 27/06 | |
| 28/06 | Thực hiện quá trình đánh giá (audit) bảo mật và quyền truy cập toàn diện. Kiểm tra lại toàn bộ các Security Groups của VPC, đảm bảo không có cổng (port) nào bị mở dư thừa ra public ngoài trừ port 443 của ALB. Rà soát lại các IAM Roles và Policies được gắn cho EC2 và GitHub Actions, tuân thủ triệt để nguyên tắc Least Privilege. Chỉnh sửa cấu hình CORS trên Backend Spring Boot để chỉ chấp nhận các request gửi đến (origin) từ chính tên miền tùy chỉnh của Frontend. | 28/06 | 29/06 | |
| 30/06 | Sử dụng dịch vụ Amazon CloudWatch để xây dựng các Dashboard giám sát hệ thống theo thời gian thực (real-time). Tập trung vào các chỉ số Metric quan trọng như: EC2 CPU Utilization, RDS Database Connections, và ALB HTTP 5xx Error Rates. Tạo các CloudWatch Alarms để tự động gửi email cảnh báo thông qua Amazon Simple Notification Service (SNS) tới nhóm phát triển nếu CPU máy chủ Backend tăng vọt quá 80% trong 5 phút liên tục. | 30/06 | 01/07 | |
| 02/07 | Thực hiện quản trị tài chính đám mây. Sử dụng công cụ AWS Cost Explorer và Billing Dashboard để phân tích chi tiết các khoản chi phí phát sinh trong tháng qua. Xác định được một số Snapshot của RDS hoặc các Elastic IP không còn sử dụng gây lãng phí. Tiến hành xóa bỏ các tài nguyên thừa này. Thiết lập thêm một Billing Alarm để gửi cảnh báo khẩn cấp nếu chi phí ước tính (estimated charges) trong tháng có nguy cơ vượt qua ngưỡng 5 USD, giúp kiểm soát hoàn toàn ngân sách dự án. | 02/07 | 02/07 | |

Thành tích tuần 11:

- Xác nhận độ tin cậy và sự ổn định của hệ thống Pet Resort từ giao diện UI cho đến lõi Database thông qua các kịch bản test khắt khe.
- Hệ thống đã được trang bị công cụ giám sát (monitoring) và cảnh báo (alerting) tự động, giúp chủ động phản ứng trước sự cố.
- Kiểm soát và tối ưu hóa tối đa chi phí cơ sở hạ tầng Cloud, giữ ngân sách duy trì quanh mức Free Tier an toàn.
