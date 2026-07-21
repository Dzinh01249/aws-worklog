---
title: "Worklog Tuần 5"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

Mục tiêu tuần 5:
- Dịch chuyển trọng tâm sang phía Server. Mục tiêu tuần này là khởi tạo khung sườn cho ứng dụng Backend bằng framework Java Spring Boot, đồng thời thiết kế và quy hoạch một hệ thống mạng ảo riêng biệt (Amazon VPC) để bảo vệ các tài nguyên tính toán của dự án khỏi các mối đe dọa từ internet.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 15/05 | Truy cập Spring Initializr để tạo một dự án Spring Boot mới. Cấu hình các dependency thiết yếu như Spring Web, Spring Data JPA, Lombok, và MySQL Driver. Thiết lập cấu trúc thư mục đa tầng (Multi-tier Architecture) chuẩn mực bao gồm các package: `controllers` (xử lý HTTP request), `services` (chứa logic nghiệp vụ), `repositories` (giao tiếp database), và `models/entities` (ánh xạ dữ liệu). Xây dựng một vài API `/health` cơ bản để kiểm tra hoạt động. | 15/05 | 16/05 | |
| 17/05 | Bắt đầu thiết kế hệ thống mạng đám mây. Đăng nhập AWS Console và tạo một Amazon Virtual Private Cloud (VPC) tùy chỉnh với dải mạng CIDR `10.0.0.0/16`. Quy hoạch VPC thành nhiều Subnet chia đều trên 2 Availability Zones để tăng tính dự phòng. Cụ thể, thiết lập 2 Public Subnets (dành cho Load Balancer) có khả năng ra internet trực tiếp, và 2 Private Subnets (dành cho EC2 Backend và RDS) hoàn toàn cô lập với bên ngoài. | 17/05 | 18/05 | |
| 19/05 | Thiết lập các thành phần điều hướng mạng lưới. Khởi tạo một Internet Gateway (IGW) và gắn nó vào VPC. Tạo một Route Table cho Public Subnets trỏ `0.0.0.0/0` ra IGW. Tiếp theo, cấu hình NAT Gateway (đặt trong Public Subnet) và điều chỉnh Route Table của Private Subnets để các máy chủ backend ở bên trong vẫn có thể tải các bản cập nhật phần mềm từ internet ra ngoài một cách an toàn mà không bị tấn công ngược vào trong. | 19/05 | 20/05 | |
| 21/05 | Thiết lập tường lửa bảo mật thông qua AWS Security Groups. Tạo một Security Group riêng cho Application Load Balancer (chỉ mở port 80/443 ra toàn cầu). Tạo Security Group thứ hai cho EC2 Backend (chỉ mở port 8080 và chỉ chấp nhận traffic đến từ Security Group của Load Balancer). Thiết lập quy tắc (rule) khắc khe tuân thủ tuyệt đối nguyên tắc 'Least Privilege' nhằm đảm bảo an ninh thông tin ở mức cao nhất cho dự án. | 21/05 | 21/05 | |

Thành tích tuần 5:

- Khung kiến trúc Backend Spring Boot đã thành hình, sẵn sàng cho việc phát triển các luồng xử lý nghiệp vụ phức tạp ở các tuần sau.
- Hệ thống mạng VPC đã được quy hoạch, triển khai và cấu hình định tuyến thành công, tạo nên một pháo đài bảo mật vững chắc.
- Phân tách rõ ràng giữa khu vực public (có thể tiếp cận từ ngoài) và khu vực private (chỉ dành cho dữ liệu nội bộ) trên môi trường Cloud.
