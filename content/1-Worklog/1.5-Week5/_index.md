---
title: "Week 5"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

Week 5 Objectives:
- Initialize the Spring Boot Backend and set up a secure AWS VPC network.

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Use Spring Initializr to create the Java app. Setup Multi-tier MVC architecture. | 15/05/2026 | 16/05/2026 | [Spring Boot](https://spring.io/projects/spring-boot) |
| 2 | Log into AWS, create a VPC (`10.0.0.0/16`) with 2 Public and 2 Private Subnets. | 17/05/2026 | 18/05/2026 | [Amazon VPC](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html) |
| 3 | Configure an Internet Gateway for Public Subnets and a NAT Gateway for Private Subnets. | 19/05/2026 | 19/05/2026 | [NAT Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html) |
| 4 | Create dedicated Route Tables to handle routing for the respective Subnet tiers. | 20/05/2026 | 20/05/2026 | [Route Tables](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html) |
| 5 | Set up Security Groups: block unused ports, only allow port 80/443 in the public zone. | 21/05/2026 | 21/05/2026 | [Security Groups](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html) |

Week 5 Achievements:

- Network Architecture framework is highly secure and isolated.
