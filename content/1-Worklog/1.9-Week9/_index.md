---
title: "Week 9"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

Week 9 Objectives:
- Implement High Availability (HA) via an Application Load Balancer (ALB).

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Relocate the EC2 instance into the deep Private Subnet for advanced security. | 12/06/2026 | 13/06/2026 | [VPC Subnets](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html) |
| 2 | Create a Target Group and register the backend EC2 servers into this group. | 14/06/2026 | 14/06/2026 | [Target Groups](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-target-groups.html) |
| 3 | Deploy an Application Load Balancer (ALB) in the Public Subnet to route external traffic. | 15/06/2026 | 15/06/2026 | [AWS ALB](https://aws.amazon.com/elasticloadbalancing/application-load-balancer/) |
| 4 | Configure Health Checks (`/api/v1/health`) allowing the ALB to isolate faulty instances. | 16/06/2026 | 17/06/2026 | [ALB Health Checks](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/target-group-health-checks.html) |
| 5 | Update Backend API environment variables on the Frontend to use the ALB's DNS. | 18/06/2026 | 18/06/2026 | [Vite Env Variables](https://vitejs.dev/guide/env-and-mode) |

Week 9 Achievements:

- The application now features a fault-tolerant architecture, eliminating Single Points of Failure.
