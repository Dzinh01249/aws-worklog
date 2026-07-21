---
title: "Worklog Week 11"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

Week 11 Objectives:
- With the system architecture fully defined, this week's goal is to ensure software quality through comprehensive End-to-End Testing, while simultaneously establishing a Monitoring and alerting system, and executing a cloud operational cost optimization campaign.

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 26/06 | Executed a series of End-to-End (E2E) test scenarios playing the role of a real user. Accessed the website via the official domain, performed account registration, browsed the Spa services list, added to cart, and completed the payment/booking flow. Concurrently, logged directly into the MySQL RDS via the DBeaver tool (through an SSH tunnel or Bastion Host) to verify whether the booking data was accurately and consistently stored in the database tables. | 26/06 | 27/06 | |
| 28/06 | Conducted a comprehensive security and access control audit. Re-examined all VPC Security Groups, ensuring no redundant ports were exposed to the public besides port 443 on the ALB. Reviewed the IAM Roles and Policies attached to EC2 and GitHub Actions, strictly adhering to the Least Privilege principle. Adjusted CORS configurations on the Spring Boot Backend to only accept incoming requests (origins) from the Frontend's official custom domain. | 28/06 | 29/06 | |
| 30/06 | Utilized the Amazon CloudWatch service to build real-time system monitoring Dashboards. Focused on critical Metrics such as: EC2 CPU Utilization, RDS Database Connections, and ALB HTTP 5xx Error Rates. Created CloudWatch Alarms to automatically send alert emails via Amazon Simple Notification Service (SNS) to the development team if the Backend server's CPU spikes above 80% for 5 continuous minutes. | 30/06 | 01/07 | |
| 02/07 | Performed cloud financial management. Used the AWS Cost Explorer tool and Billing Dashboard to detail-analyze incurred costs over the past month. Identified several unused RDS Snapshots or Elastic IPs causing waste. Proceeded to delete these redundant resources. Established an additional Billing Alarm to send an emergency alert if the estimated charges for the month risk exceeding the $5 threshold, maintaining total control over the project budget. | 02/07 | 02/07 | |

Week 11 Achievements:

- Confirmed the reliability and stability of the Pet Resort system from the UI down to the Database core through rigorous test scenarios.
- The system is now equipped with automated monitoring and alerting tools, enabling proactive responses to incidents.
- Maximized control and optimization of Cloud infrastructure costs, keeping the maintenance budget safely around the Free Tier level.
