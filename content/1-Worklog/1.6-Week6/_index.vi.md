---
title: "Worklog Tuần 6"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

Mục tiêu tuần 6:
- Mục tiêu là tích hợp cơ sở dữ liệu cho hệ thống. Thiết lập Amazon RDS (Relational Database Service) một cách an toàn bên trong mạng nội bộ VPC, sau đó viết code Backend để kết nối, tương tác và quản lý dữ liệu thông qua Object-Relational Mapping (ORM). Sự ổn định của cơ sở dữ liệu là cốt lõi của toàn hệ thống.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 22/05 | Truy cập dịch vụ Amazon RDS và khởi tạo một instance MySQL phiên bản 8.0. Đặc biệt quan trọng: cấu hình DB instance này nằm hoàn toàn bên trong các Private Subnets của VPC đã tạo ở tuần trước. Vô hiệu hóa tùy chọn 'Public access' để không ai trên internet có thể truy cập trực tiếp vào DB. Thiết lập Multi-AZ (Multiple Availability Zones) để đảm bảo tính sẵn sàng cao, tự động failover nếu một zone gặp sự cố. | 22/05 | 23/05 | |
| 24/05 | Tạo một Security Group dành riêng cho RDS, với quy tắc Inbound chỉ mở cổng 3306 và chỉ cho phép lưu lượng mạng (traffic) đi tới từ Security Group của các EC2 Backend. Cập nhật file `application.yml` trong dự án Spring Boot với chuỗi kết nối (JDBC URL), thông tin username và password. Khéo léo ẩn các thông tin nhạy cảm này bằng cách sử dụng các biến môi trường (Environment Variables) thay vì hard-code trực tiếp vào mã nguồn. | 24/05 | 25/05 | |
| 26/05 | Bắt đầu làm việc với Spring Data JPA. Định nghĩa các Entity classes như `User`, `SpaService`, `Booking` và `Pet` với các annotations như `@Entity`, `@Table`, `@OneToMany`. Thiết lập cơ chế tự động sinh schema bảng (auto ddl) để hỗ trợ quá trình phát triển ban đầu. Đào sâu vào việc thiết kế cấu trúc dữ liệu quan hệ, đảm bảo chuẩn hóa dữ liệu, thiết lập các khóa ngoại (foreign keys) và index phù hợp. | 26/05 | 27/05 | |
| 28/05 | Phát triển các API RESTful Controller thực hiện các thao tác CRUD (Create, Read, Update, Delete) cho các đối tượng dịch vụ. Sử dụng Postman để gửi các HTTP requests test các API endpoint này. Sử dụng hibernate log để phân tích các câu lệnh SQL tự sinh, phát hiện và sửa chữa vấn đề 'N+1 queries' phổ biến trong JPA bằng cách sử dụng `@EntityGraph` hoặc các truy vấn `JOIN FETCH` chuyên biệt. | 28/05 | 28/05 | |

Thành tích tuần 6:

- Hệ thống cơ sở dữ liệu quan hệ (RDBMS) đã được thiết lập, cấu hình bảo mật ở mức cao nhất trong Private Subnet.
- Backend Spring Boot đã giao tiếp thành công, đọc ghi dữ liệu trơn tru xuống Amazon RDS thông qua Hibernate/JPA.
- Nhận thức và xử lý được các vấn đề hiệu suất cơ sở dữ liệu liên quan đến ORM, tối ưu hóa quá trình truy vấn.
