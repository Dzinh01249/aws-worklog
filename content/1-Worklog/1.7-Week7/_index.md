---
title: "Worklog Week 7"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

Week 7 Objectives:
- Deploy the Backend application to Amazon EC2 and configure the production server environment.

| Day | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Launch EC2 Instance (Amazon Linux 2023) in Private Subnet, create Key Pair and establish SSH connection via Bastion Host. | 04/06/2026 | 05/06/2026 | |
| 2 | Install runtime environment: OpenJDK 17, configure environment variables and JVM parameters for production. | 06/06/2026 | 07/06/2026 | |
| 3 | Build JAR file from Spring Boot source, upload to EC2 via SCP, and run application as systemd service. | 08/06/2026 | 09/06/2026 | |
| 4 | Verify internal connectivity from EC2 to other VPC services, confirm API operates stably. | 10/06/2026 | 11/06/2026 | |

Week 7 Achievements:

- Spring Boot Backend running stably on EC2 within Private Subnet.
- Application managed as systemd service ensuring auto-restart on failures.
