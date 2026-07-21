---
title: "Worklog Week 7"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

Week 7 Objectives:
- The central goal is to migrate the completed Backend application from the local machine to run live on the AWS cloud environment. This process requires setting up an EC2 virtual Linux server, installing the Java environment, and configuring the application to run stably with self-healing capabilities.

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 29/05 | Used the AWS Console to provision an Amazon EC2 (Elastic Compute Cloud) virtual server using the Ubuntu Server operating system. Selected the `t3.micro` instance type, suitable for the Free Tier. Generated and securely downloaded an SSH Key Pair (`.pem` file). Attached this EC2 server to a Public Subnet (for ease of management during the testing phase) and applied the Security Group designed in week 5. Connected (SSH) to the server via Terminal/PuTTY. | 29/05 | 30/05 | |
| 31/05 | Updated Ubuntu system packages using `apt update` and `apt upgrade`. Proceeded to install the Java Runtime Environment (JRE 17) via OpenJDK. Drafted a service configuration file (Systemd Unit File) located at `/etc/systemd/system/pet-resort.service`. This file instructs the Linux OS how to start the Spring Boot `.jar` file, manage logs, and crucially, automatically restart the application if it crashes or when the server reboots. | 31/05 | 01/06 | |
| 02/06 | Returned to the local development environment, used Maven (`mvn clean package`) to package the Spring Boot application into a single executable file (`.jar`). Used the SCP (Secure Copy) command or graphical tools like WinSCP/FileZilla combined with the SSH Key to securely upload this multi-megabyte `.jar` file from the personal computer to the `/opt/pet-resort/` directory on the EC2 virtual server. | 02/06 | 03/06 | |
| 04/06 | Enabled and started the application via systemd using `systemctl enable` and `systemctl start` commands. Monitored the startup process and read live logs using the `journalctl -f` command. Verified the connection configuration from the EC2 instance to the RDS database server in the Private Subnet. Finally, performed test calls to the APIs from an external browser/Postman over the internet via the EC2 instance's Public IP to confirm the system operates flawlessly. | 04/06 | 04/06 | |

Week 7 Achievements:

- Successfully transitioned a Backend application from a local development environment to running live on a Linux virtual server (EC2).
- The application is configured to run in the background as a professional system service, capable of auto-recovery upon errors.
- Mastered the processes of packaging, secure file transfer, and basic Linux server administration.
