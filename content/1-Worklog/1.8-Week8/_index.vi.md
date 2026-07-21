---
title: "Worklog Tuần 8"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

Mục tiêu tuần 8:
- Tối ưu hóa hiệu suất ứng dụng để chuẩn bị cho lượng truy cập lớn. Bằng cách triển khai cơ chế In-memory Caching với Amazon ElastiCache (Redis), mục tiêu là giảm tải đáng kể cho cơ sở dữ liệu RDS và giảm độ trễ (latency) của các API trả về nội dung tĩnh hoặc ít thay đổi.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 05/06 | Nghiên cứu tài liệu về các chiến lược bộ nhớ đệm (Caching strategies) và dịch vụ Amazon ElastiCache. Phân tích các endpoint API hiện tại của hệ thống Pet Resort và xác định rằng API lấy 'Danh sách các dịch vụ Spa' là một API có tần suất đọc cực cao (read-heavy) nhưng dữ liệu lại hiếm khi bị thay đổi. Quyết định áp dụng Redis để làm bộ đệm (cache layer) đặt giữa Backend và Database RDS. | 05/06 | 06/06 | |
| 07/06 | Truy cập AWS Console và khởi tạo một Cluster Redis thông qua dịch vụ ElastiCache. Đặt Redis Cluster này vào bên trong các Private Subnets để tối đa hóa tính bảo mật. Thiết lập một Security Group riêng biệt cho Redis Cluster, chỉ cấu hình Inbound Rules cho phép các máy chủ EC2 chứa Backend có quyền kết nối vào qua port mặc định 6379, chặn hoàn toàn mọi nguồn truy cập trái phép khác. | 07/06 | 08/06 | |
| 09/06 | Trở lại môi trường code Spring Boot, thêm dependency `spring-boot-starter-data-redis` và cấu hình kết nối đến host của ElastiCache thông qua biến môi trường. Bật tính năng Caching của Spring bằng annotation `@EnableCaching`. Sử dụng các annotations như `@Cacheable`, `@CachePut`, và `@CacheEvict` trên các hàm xử lý logic lấy danh sách dịch vụ. Cấu hình tỉ mỉ thời gian sống của dữ liệu trong cache (Time-To-Live - TTL) để đảm bảo dữ liệu không bị cũ (stale). | 09/06 | 10/06 | |
| 11/06 | Đóng gói (build) lại file `.jar`, upload và khởi động lại systemd service trên EC2. Sử dụng công cụ Apache JMeter hoặc Postman Runner để thực hiện các bài test chịu tải (Load Testing) nhỏ giọt. Quan sát kỹ lưỡng thời gian phản hồi (Response Time). Ghi nhận kết quả: đối với các yêu cầu (requests) đầu tiên mất khoảng vài trăm milliseconds để lấy từ RDS, các yêu cầu tiếp theo lấy trực tiếp từ Redis trên RAM chỉ mất dưới vài chục milliseconds, giảm độ trễ lên đến hơn 80%. | 11/06 | 11/06 | |

Thành tích tuần 8:

- Tích hợp thành công và hiệu quả công nghệ Redis Cache (thông qua ElastiCache) vào kiến trúc hệ thống tổng thể.
- Xử lý triệt để nút thắt cổ chai (bottleneck) về tốc độ truy xuất cơ sở dữ liệu, giảm thiểu nguy cơ quá tải RDS.
- Cải thiện vượt bậc trải nghiệm người dùng với tốc độ load dữ liệu danh mục dịch vụ gần như ngay lập tức.
