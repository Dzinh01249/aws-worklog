---
title: "Week 7"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

Week 7 Objectives:
- Deploy the Spring Boot Java application onto an EC2 virtual server.

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Launch an EC2 Ubuntu Server (`t3.micro`) and download an SSH Key Pair for access. | 29/05/2026 | 30/05/2026 | [Amazon EC2 Setup](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html) |
| 2 | Update OS packages and install the Java environment (OpenJDK 17) on EC2. | 31/05/2026 | 01/06/2026 | [Install Java Ubuntu](https://ubuntu.com/tutorials/install-jre) |
| 3 | Package the application into a `.jar` via Maven and upload to EC2 using SCP. | 02/06/2026 | 02/06/2026 | [Maven Package](https://maven.apache.org/guides/getting-started/) |
| 4 | Create a Systemd Service file (`.service`) for background execution and auto-restart on crash. | 03/06/2026 | 03/06/2026 | [Systemd Services](https://linuxhandbook.com/create-systemd-services/) |
| 5 | Start the service, check logs using `journalctl`, and verify APIs via Postman. | 04/06/2026 | 04/06/2026 | [Journalctl Guide](https://www.loggly.com/ultimate-guide/using-journalctl/) |

Week 7 Achievements:

- Backend deployed and running stably 24/7 as a Linux service.
