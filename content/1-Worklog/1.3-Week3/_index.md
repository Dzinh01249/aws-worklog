---
title: "Worklog Week 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

Week 3 Objectives:
- Plan virtual network infrastructure (VPC) and clearly zone service layers into Public/Private segments.

| Day | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Initialize Amazon VPC with custom CIDR Block, attach Internet Gateway to VPC. | 03/05/2026 | 04/05/2026 | |
| 2 | Divide Public Subnets (for ALB, NAT Gateway) and Private Subnets (for EC2, RDS, ElastiCache) across 2 Availability Zones. | 05/05/2026 | 06/05/2026 | |
| 3 | Configure Route Tables for each Subnet tier, set up NAT Gateway for one-way internet access from Private Subnet. | 07/05/2026 | 08/05/2026 | |
| 4 | Redraw detailed network architecture diagram including data flow in/out between Subnets. | 09/05/2026 | 10/05/2026 | |

Week 3 Achievements:

- Complete VPC network infrastructure with clear Multi-AZ zoning.
- Secure traffic flow: Internet → Public Subnet → Private Subnet.
