---
title: "Worklog Tuần 8"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:
* Hoàn tất việc đóng gói mã nguồn Spring Boot của dự án Pet Shop thành tệp thực thi độc lập (.jar) ngay trên máy cá nhân.
* Nghiên cứu các giải pháp triển khai Backend lên nền tảng đám mây phù hợp với người mới bắt đầu.
* Chuyển hướng tìm hiểu sang dịch vụ AWS Elastic Beanstalk sau khi nhận thấy việc tự quản trị máy chủ EC2 (Linux) vượt quá kỹ năng hiện tại.

### Nhiệm vụ thực hiện trong tuần:
| Ngày | Nhiệm vụ chi tiết | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - Tạm dừng việc code tính năng mới, bắt đầu tìm hiểu quy trình Build và Đóng gói một ứng dụng Spring Boot.<br>- Đọc tài liệu về Maven Lifecycle (Clean, Compile, Package). | 08/06/2026 | 08/06/2026 | Tài liệu Spring Boot Maven |
| 2 | - Thực hành chạy lệnh `mvn clean package` trên Terminal của VS Code / IntelliJ để đóng gói dự án Backend Pet Shop thành file `.jar`.<br>- Xử lý các lỗi lặt vặt liên quan đến Test Cases khi build file. | 09/06/2026 | 09/06/2026 | StackOverflow / Blog Java |
| 3 | - Tắt công cụ lập trình (IDE), mở Command Prompt của Windows và thử chạy file `.jar` vừa build bằng lệnh `java -jar petshop-backend.jar`.<br>- Kiểm tra lại các API trên Postman để chắc chắn file chạy độc lập tốt. | 10/06/2026 | 10/06/2026 | Java Documentation |
| 4 | - Đọc tài liệu chuẩn bị đưa file `.jar` lên máy chủ AWS EC2.<br>- Nhận ra việc cấu hình EC2 yêu cầu kỹ năng dòng lệnh hệ điều hành Linux (Ubuntu), cài đặt biến môi trường khá phức tạp và dễ gây lỗi hệ thống. | 11/06/2026 | 11/06/2026 | Tài liệu Amazon EC2 Linux |
| 5 | - Thảo luận với nhóm và quyết định chuyển hướng sang tìm hiểu dịch vụ **AWS Elastic Beanstalk** (PaaS) – giải pháp cho phép tải trực tiếp file `.jar` lên thông qua giao diện Web mà không cần gõ lệnh Linux. | 12/06/2026 | 12/06/2026 | AWS Elastic Beanstalk Guide |

### Kết quả đạt được tuần 8:

* **Hoàn thiện kỹ năng đóng gói ứng dụng Local (Application Packaging):**
  * Hiểu được sự khác biệt giữa việc chạy code trực tiếp trên công cụ lập trình (IDE) và chạy ứng dụng đã được biên dịch độc lập.
  * Sử dụng thành công Maven để đóng gói dự án Spring Boot thành một tệp thực thi `.jar` hoàn chỉnh.
  * Đảm bảo ứng dụng backend chạy ổn định trên môi trường Windows local thông qua lệnh `java -jar`, kết nối thành công với cơ sở dữ liệu.

* **Hình thành tư duy lựa chọn dịch vụ đám mây (Cloud Service Selection):**
  * Nắm được sự khác biệt giữa mô hình IaaS (Amazon EC2) và PaaS (AWS Elastic Beanstalk).
  * Đánh giá đúng năng lực cá nhân: Chủ động tạm ngưng sử dụng EC2 thuần túy để tránh rủi ro bảo mật và vận hành do thiếu kinh nghiệm quản trị hệ điều hành Linux.

* **Xác định rõ lộ trình triển khai an toàn cho các tuần tiếp theo:**
  * Cân nhắc phương án sử dụng Elastic Beanstalk cho dự án Pet Shop. Dịch vụ này sẽ tự động khởi tạo EC2, tự cài đặt Java và tự cấu hình mạng ở phía sau, giúp nhóm tiết kiệm thời gian và tránh các lỗi cấu hình hạ tầng mạng phức tạp.