---
title: "Worklog Week 8"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

Week 8 Objectives:
- Provision Amazon RDS (MySQL) as the relational storage layer and integrate ElastiCache Redis for performance optimization.

| Day | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Create RDS Instance (MySQL 8.0) in Private Subnet with Multi-AZ Standby mode, configure DB Subnet Group and Security Group. | 12/06/2026 | 13/06/2026 | |
| 2 | Connect Spring Boot to RDS via JDBC, run migration scripts to initialize tables, and test CRUD operations via API. | 14/06/2026 | 15/06/2026 | |
| 3 | Provision ElastiCache Redis Cluster in Private Subnet, integrate Spring Boot with Redis via Spring Data Redis. | 16/06/2026 | 17/06/2026 | |
| 4 | Set up cache for Spa service listings and best-selling products, benchmark performance before and after enabling Redis. | 18/06/2026 | 19/06/2026 | |

Week 8 Achievements:

- MySQL database running stably on RDS with Multi-AZ failover mechanism.
- Significantly reduced API response times thanks to Redis cache layer.
