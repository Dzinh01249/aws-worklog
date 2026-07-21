---
title: "Worklog Tuần 9"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

Mục tiêu tuần 9:
- Để ứng dụng có khả năng chịu tải quy mô lớn và đảm bảo tính sẵn sàng cao (High Availability - HA), mục tiêu tuần này là thiết lập một Application Load Balancer (ALB). ALB sẽ đứng phía trước làm cửa ngõ, tiếp nhận và phân phối đều đặn lưu lượng mạng từ người dùng tới nhiều máy chủ EC2 Backend ở phía sau.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 12/06 | Tìm hiểu lý thuyết về Elastic Load Balancing của AWS. Tiến hành tạo một Target Group mới, đây là nhóm sẽ chứa các máy chủ đích (backend servers). Khai báo giao thức là HTTP trên port 8080. Tiếp đó, đăng ký (register) máy chủ EC2 hiện có vào Target Group này. Đồng thời, cấu trúc lại hệ thống bằng cách di chuyển máy chủ EC2 từ Public Subnet vào sâu bên trong Private Subnet để tăng cường bảo mật, không cho phép truy cập trực tiếp từ internet. | 12/06 | 13/06 | |
| 14/06 | Khởi tạo một Application Load Balancer (ALB) thuộc loại Internet-facing, đặt tại các Public Subnets của VPC để nó có thể nhận được traffic từ bên ngoài. Gắn một Security Group cho ALB chỉ cho phép Inbound HTTP (port 80) và HTTPS (port 443). Thiết lập một Listener Rule trên ALB để tự động chuyển tiếp (forward) toàn bộ lưu lượng web hợp lệ đi vào các máy chủ nằm trong Target Group đã thiết lập ở bước trước. | 14/06 | 15/06 | |
| 16/06 | Thiết lập cơ chế kiểm tra sức khỏe hệ thống (Health Checks) cực kỳ quan trọng trên ALB. Cấu hình ALB liên tục ping (gửi request) tới một endpoint API chuyên dụng `/api/v1/health` của Backend cứ mỗi 30 giây. Nếu Backend trả về HTTP Status 200 OK liên tục, ALB sẽ coi máy chủ đó là 'Healthy'. Nếu có lỗi (crash, treo máy), ALB sẽ ngay lập tức ngắt traffic đến máy chủ bị lỗi đó, tránh ảnh hưởng đến người dùng cuối. | 16/06 | 17/06 | |
| 18/06 | Lấy tên miền DNS (DNS name) dài và phức tạp do ALB sinh ra, sau đó quay trở lại dự án Frontend ReactJS, sửa đổi biến môi trường `VITE_API_BASE_URL` trỏ đến DNS name của ALB thay vì Public IP tĩnh của máy EC2 như cũ. Build và deploy lại Frontend lên S3/CloudFront. Tiến hành kiểm thử toàn hệ thống, giả lập các kịch bản lỗi (tắt EC2) để quan sát cơ chế chuyển hướng (failover) tự động của Load Balancer hoạt động. | 18/06 | 18/06 | |

Thành tích tuần 9:

- Thiết kế và triển khai thành công mô hình cân bằng tải (Load Balancing) chuẩn công nghiệp.
- Hệ thống không còn bị phụ thuộc vào một Điểm lỗi duy nhất (Single Point of Failure), nâng cao khả năng chống chịu sự cố (Fault Tolerance).
- Nắm vững cơ chế Health Check tự động, tối ưu hóa quy trình bảo trì hệ thống không gây gián đoạn dịch vụ.
