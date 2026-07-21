---
title: "Worklog Week 6"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

Week 6 Objectives:
- The objective is to integrate the database for the system. Securely set up Amazon RDS (Relational Database Service) within the internal VPC network, then write Backend code to connect, interact, and manage data via Object-Relational Mapping (ORM).

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 22/05 | Accessed the Amazon RDS service and provisioned a MySQL version 8.0 instance. Crucially important: configured this DB instance to reside entirely within the Private Subnets of the VPC created last week. Disabled the 'Public access' option so no one on the internet can directly access the DB. Enabled Multi-AZ (Multiple Availability Zones) to ensure high availability and automatic failover should one zone experience an outage. | 22/05 | 23/05 | |
| 24/05 | Created a dedicated Security Group for RDS, with an Inbound rule opening only port 3306 and allowing network traffic exclusively from the Security Group of the EC2 Backends. Updated the `application.yml` file in the Spring Boot project with the connection string (JDBC URL), username, and password information. Cleverly concealed this sensitive information by utilizing Environment Variables instead of hard-coding them directly into the source code. | 24/05 | 25/05 | |
| 26/05 | Started working with Spring Data JPA. Defined Entity classes such as `User`, `SpaService`, `Booking`, and `Pet` with annotations like `@Entity`, `@Table`, `@OneToMany`. Configured the auto DDL schema generation mechanism to aid the initial development process. Delved deep into designing the relational data structure, ensuring data normalization, and setting up appropriate foreign keys and indexes. | 26/05 | 27/05 | |
| 28/05 | Developed RESTful Controller APIs performing CRUD (Create, Read, Update, Delete) operations for service objects. Used Postman to send HTTP requests to test these API endpoints. Utilized hibernate logs to analyze auto-generated SQL statements, detecting and resolving the common 'N+1 queries' problem in JPA by employing `@EntityGraph` or specialized `JOIN FETCH` queries. | 28/05 | 28/05 | |

Week 6 Achievements:

- The Relational Database Management System (RDBMS) has been established with the highest level of security configuration in a Private Subnet.
- The Spring Boot Backend successfully communicated, smoothly reading and writing data to Amazon RDS via Hibernate/JPA.
- Recognized and handled database performance issues related to ORMs, optimizing the query process.
