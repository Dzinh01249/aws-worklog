---
title: "Worklog Week 5"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

Week 5 Objectives:
- Shifting focus to the Server side. This week's goal is to initialize the framework for the Backend application using Java Spring Boot, while simultaneously designing and planning an isolated virtual network system (Amazon VPC) to protect the project's compute resources from internet threats.

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 15/05 | Accessed Spring Initializr to create a new Spring Boot project. Configured essential dependencies such as Spring Web, Spring Data JPA, Lombok, and the MySQL Driver. Established a standard Multi-tier Architecture directory structure including packages: `controllers` (handling HTTP requests), `services` (containing business logic), `repositories` (database communication), and `models/entities` (data mapping). Built a few basic `/health` APIs for operational checks. | 15/05 | 16/05 | |
| 17/05 | Began designing the cloud network system. Logged into the AWS Console and created a custom Amazon Virtual Private Cloud (VPC) with the CIDR block `10.0.0.0/16`. Planned the VPC into multiple Subnets distributed evenly across 2 Availability Zones to increase redundancy. Specifically, set up 2 Public Subnets (for Load Balancers) with direct internet access, and 2 Private Subnets (for EC2 Backends and RDS) completely isolated from the outside. | 17/05 | 18/05 | |
| 19/05 | Configured network routing components. Provisioned an Internet Gateway (IGW) and attached it to the VPC. Created a Route Table for the Public Subnets routing `0.0.0.0/0` to the IGW. Next, configured a NAT Gateway (placed in a Public Subnet) and adjusted the Route Table of the Private Subnets so that internal backend servers can still safely download software updates from the internet without being vulnerable to inbound attacks. | 19/05 | 20/05 | |
| 21/05 | Established security firewalls via AWS Security Groups. Created a dedicated Security Group for the Application Load Balancer (opening only ports 80/443 globally). Created a second Security Group for the EC2 Backend (opening only port 8080 and accepting traffic exclusively from the Load Balancer's Security Group). Set up strict rules absolutely adhering to the 'Least Privilege' principle to guarantee the highest level of information security for the project. | 21/05 | 21/05 | |

Week 5 Achievements:

- The Spring Boot Backend architectural framework has taken shape, ready for developing complex business logic flows in the coming weeks.
- The VPC network system has been successfully planned, deployed, and routed, creating a robust security fortress.
- Clearly segregated the public zone (accessible externally) and the private zone (strictly for internal data) within the Cloud environment.
