---
title: "Tuần 8"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

Mục tiêu tuần 8:
- Tối ưu hiệu năng bằng bộ nhớ đệm ElastiCache (Redis).

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 05/06 | Phân tích hiệu năng và quyết định dùng Redis để cache API danh sách dịch vụ Spa (read-heavy). | 05/06 | 06/06 | |
| 07/06 | Tạo Redis Cluster trên AWS ElastiCache đặt trong Private Subnet và giới hạn cổng 6379. | 07/06 | 08/06 | |
| 09/06 | Tích hợp Spring Data Redis, thêm các annotation `@Cacheable`, `@CacheEvict` và thiết lập TTL. | 09/06 | 10/06 | |
| 11/06 | Deploy lại EC2 và dùng JMeter test tải. Độ trễ truy vấn giảm hơn 80% do không cần gọi DB. | 11/06 | 11/06 | |

Thành tích tuần 8:

- Tích hợp Redis Cache thành công.
- Tăng cường hiệu năng API và giảm rủi ro quá tải DB.
