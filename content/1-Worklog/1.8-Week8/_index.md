---
title: "Week 8"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

Week 8 Objectives:
- Accelerate API performance using an In-memory Caching system with ElastiCache.

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Evaluate read-heavy, low-write APIs to decide where to implement Caching. | 05/06/2026 | 06/06/2026 | [AWS Caching](https://aws.amazon.com/caching/) |
| 2 | Provision an Amazon ElastiCache Redis Cluster within the Private Subnet. | 07/06/2026 | 08/06/2026 | [Amazon ElastiCache](https://aws.amazon.com/elasticache/) |
| 3 | Add `spring-boot-starter-data-redis` to the Backend and configure host connections. | 09/06/2026 | 09/06/2026 | [Spring Data Redis](https://spring.io/projects/spring-data-redis) |
| 4 | Apply `@Cacheable`, `@CachePut` annotations and configure Time-To-Live (TTL) for data. | 10/06/2026 | 10/06/2026 | [Spring Caching](https://docs.spring.io/spring-framework/reference/integration/cache.html) |
| 5 | Perform load-testing with JMeter. Query latency successfully reduced by over 80%. | 11/06/2026 | 11/06/2026 | [Apache JMeter](https://jmeter.apache.org/) |

Week 8 Achievements:

- Significantly reduced RDS Database load via an effective Redis caching layer.
