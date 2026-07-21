---
title: "Tuần 6"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

Mục tiêu tuần 6:
- Triển khai Database RDS và viết API kết nối CSDL bằng Spring Data JPA.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Tạo instance Amazon RDS (MySQL) Multi-AZ đặt bên trong Private Subnet. | 22/05/2026 | 23/05/2026 | [Amazon RDS](https://aws.amazon.com/rds/) |
| 2 | Cấu hình Security Group cho RDS (mở port 3306) và kết nối DB từ Spring Boot qua biến môi trường. | 24/05/2026 | 25/05/2026 | [Spring DB Connect](https://spring.io/guides/gs/accessing-data-mysql/) |
| 3 | Tạo các lớp Entity JPA (`User`, `Service`, `Booking`) và ánh xạ quan hệ bảng. | 26/05/2026 | 26/05/2026 | [Spring Data JPA](https://spring.io/projects/spring-data-jpa) |
| 4 | Viết các RESTful API chuẩn thao tác dữ liệu (CRUD). Dùng Postman để test API nội bộ. | 27/05/2026 | 27/05/2026 | [Building REST API](https://spring.io/guides/tutorials/rest/) |
| 5 | Phân tích logs, tối ưu câu lệnh truy vấn Hibernate bằng `@EntityGraph` để tránh N+1 Query. | 28/05/2026 | 28/05/2026 | [JPA EntityGraph](https://www.baeldung.com/jpa-entity-graph) |

Thành tích tuần 6:

- API Backend đã thao tác mượt mà với cơ sở dữ liệu trên Cloud.
