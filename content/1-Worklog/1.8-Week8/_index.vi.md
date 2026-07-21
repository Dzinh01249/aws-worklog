---
title: "Tuần 8"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

Mục tiêu tuần 8:
- Tăng tốc độ truy xuất API bằng hệ thống Caching In-memory với ElastiCache.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Đánh giá các API có tần suất đọc nhiều, ít thay đổi dữ liệu để quyết định áp dụng Cache. | 05/06/2026 | 06/06/2026 | [AWS Caching](https://aws.amazon.com/caching/) |
| 2 | Tạo Redis Cluster bằng Amazon ElastiCache nằm trong Private Subnet. | 07/06/2026 | 08/06/2026 | [Amazon ElastiCache](https://aws.amazon.com/elasticache/) |
| 3 | Bổ sung thư viện `spring-boot-starter-data-redis` vào Backend và cấu hình kết nối. | 09/06/2026 | 09/06/2026 | [Spring Data Redis](https://spring.io/projects/spring-data-redis) |
| 4 | Áp dụng các annotation `@Cacheable`, `@CachePut` và set thời gian hết hạn (TTL) cho data. | 10/06/2026 | 10/06/2026 | [Spring Caching](https://docs.spring.io/spring-framework/reference/integration/cache.html) |
| 5 | Load-test bằng JMeter. Ghi nhận thời gian phản hồi (latency) của API giảm hơn 80%. | 11/06/2026 | 11/06/2026 | [Apache JMeter](https://jmeter.apache.org/) |

Thành tích tuần 8:

- Giảm tải đáng kể cho Database RDS nhờ cơ chế Redis cache hiệu quả.
