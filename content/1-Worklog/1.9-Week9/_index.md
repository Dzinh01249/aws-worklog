---
title: "Worklog Week 9"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

Week 9 Objectives:
- Set up load balancing with Application Load Balancer and configure flexible Auto Scaling.

| Day | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Create Target Group registering EC2 Backend, configure Health Check endpoint (/api/health) for status monitoring. | 20/06/2026 | 21/06/2026 | |
| 2 | Initialize Application Load Balancer in Public Subnet, set up Listener Rules routing requests to Target Group. | 22/06/2026 | 23/06/2026 | |
| 3 | Create Launch Template from current EC2 AMI, configure Auto Scaling Group with scale-out/scale-in policies. | 24/06/2026 | 25/06/2026 | |
| 4 | Simulate heavy load with stress testing tools, observe Auto Scaling automatically provisioning new instances. | 26/06/2026 | 27/06/2026 | |

Week 9 Achievements:

- Backend capable of handling high traffic and self-healing via ALB + Auto Scaling.
- Health Checks automatically remove faulty instances from the serving pool.
