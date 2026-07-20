---
title: "Worklog Week 11"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

Week 11 Objectives:
- Build operational monitoring system with Amazon CloudWatch and set up automated alerts via SNS.

| Day | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Install CloudWatch Agent on EC2, collect metrics: CPU Utilization, Memory Usage, Disk I/O. | 06/07/2026 | 07/07/2026 | |
| 2 | Create CloudWatch Dashboard aggregating system-wide status: EC2, RDS, ElastiCache, ALB. | 08/07/2026 | 09/07/2026 | |
| 3 | Set up CloudWatch Alarms for critical thresholds: CPU > 80%, DB Connection > 90%, Error Rate spikes. | 10/07/2026 | 11/07/2026 | |
| 4 | Create SNS Topic and subscribe email for notifications, test automated alert flow when alarms trigger. | 12/07/2026 | 13/07/2026 | |

Week 11 Achievements:

- Centralized monitoring dashboard enables real-time system health tracking.
- Automated email alerts when resource anomalies are detected.
