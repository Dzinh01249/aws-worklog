---
title: "Project Proposal"
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Pet Resort & Care System  
### Project Documentation

📄 **[Download Complete Project Proposal (Word Document)](#)**

---

### 1. System Overview

The "Pet Resort & Care System" is an experimental product (Minimum Viable Product - MVP) developed as part of a graduation/internship project. The application is a basic web platform that combines pet product e-commerce with spa service booking.

The team attempted to apply a 3-Tier Architecture on AWS to gain hands-on experience in real-world application deployment. Although we have set up a Multi-AZ environment and utilized core AWS services, the current system is primarily for "learning and testing" purposes and cannot be compared to high-traffic, production-grade Enterprise systems.

---

### 2. Solution Architecture & Tier Details (Experimental Level)

Below is the system architecture diagram that the team sketched and deployed after receiving flow correction feedback from our mentors:

![AWS Architecture Pet Resort System](image_ab600f.jpg)

#### 2.1. Edge & Content Delivery Layer
*   **AWS WAF & CloudFront:** We enabled WAF and CloudFront to get familiar with CDN concepts. However, our WAF rules are mostly basic AWS Managed Rules, as we lack the experience for deep fine-tuning. CloudFront helps load static S3 assets a bit faster, but we occasionally encounter cache errors due to improper invalidation configurations.

#### 2.2. Network & Compute Tier
*   **ALB & EC2 (Auto Scaling):** We use an Application Load Balancer to distribute traffic to EC2 instances (`t3.micro`) located in the Private Subnet. An Auto Scaling Group is configured; however, during actual testing, the scale-out speed is quite slow (taking a few minutes). Therefore, if there is a sudden spike in requests, the server still risks temporary freezing.
*   **NAT Gateway:** To save costs, the team only dared to provision a single NAT Gateway for both Availability Zones. This creates a Single Point of Failure (SPOF), but it is a necessary compromise given our limited student budget.

#### 2.3. Data Tier
*   **Amazon ElastiCache (Redis):** We experimented with Redis to store user sessions and temporary shopping carts. Because our Backend (Spring Boot) cache handling is not perfectly optimized, there are occasional data synchronization issues between the Database and the Cache.
*   **Amazon RDS (MySQL):** We went "all in" to set up a Multi-AZ (Active-Standby) deployment just to observe how automatic failover works. Since we don't have massive demo data, this setup is mainly to gain practical experience in cloud database administration.

#### 2.4. Security & Management Layer
*   We made an effort to avoid hardcoding passwords by experimenting with **AWS Secrets Manager** and **KMS**. However, our IAM Role permissions are sometimes configured a bit too loosely (granting overly broad access to prevent "Access Denied" errors during development).
*   We successfully implemented **Session Manager** instead of opening Port 22 (SSH), a small but valuable security plus we learned from our mentor.

#### 2.5. Cost Optimization (Introductory FinOps)
*   **S3 Endpoint & Pre-signed URL:** Thanks to the documentation, we learned how to allow clients to upload files directly to S3 (using temporary Pre-signed URLs) instead of routing them through EC2. This helps prevent server memory overload and saves a small amount on NAT Gateway data processing fees.

---

### 3. Budget Estimation (The "Survival" Math)
Because the architecture includes several paid services (NAT, RDS, ALB), the team must constantly monitor billing to avoid going broke. We are trying our best to squeeze the estimated current cost to under $130/month.

*Estimated Infrastructure Cost (Monthly - Demo Environment)* 
- *Amazon EC2*: ~$15.00 USD (2 `t3.micro` instances).
- *Application Load Balancer*: ~$18.00 USD.
- *NAT Gateway*: ~$35.00 USD (Only 1 instance).
- *Amazon RDS*: ~$28.00 USD (`db.t3.micro` Multi-AZ).
- *Amazon ElastiCache (Redis)*: ~$12.00 USD (`cache.t4g.micro`).
- *Other Services (WAF, S3, CloudFront, Secrets Manager, etc.)*: ~$12.00 USD.

*Total Budget*: **~$120.00 USD/month**. 
Despite our strict optimizations, this is still a rather "painful" bill for students. The team plans to tear down the RDS and NAT Gateway immediately after the final acceptance presentation to prevent further unexpected charges.

---

### 4. Risk Assessment (Highly Realistic)
*   **Slow Auto Scaling Response (High Probability):** If the grading committee or users spam requests too rapidly, the EC2 instances will likely overload before the Auto Scaling Group has time to spin up new machines.
*   **Backend Code Bugs (Medium Probability):** The spa booking logic occasionally suffers from double-booking bugs because database locking mechanisms are not yet thoroughly implemented.
*   **Budget Overrun (High Probability):** Misconfigured IAM or CloudWatch can sometimes cause recursive API calls, generating hidden usage fees.

---

### 5. Expected Outcomes & Lessons Learned
*   **The Product:** A "workable" web application where basic flows (purchasing, booking) can be executed from start to finish without throwing 500 errors (unless overloaded).
*   **Skills Acquired:** 
    *   Curing "Cloud Blindness": The team manually clicked through the Console, configuring VPCs, Subnets, and Load Balancers instead of just reading theories.
    *   Tasting the Pain: We learned that debugging code locally is easy, but finding errors via CloudWatch Logs when the code is deployed on an EC2 instance hidden behind a Private Subnet is an entirely different struggle.
    *   Although the architecture is still rough and has loopholes, this project is an incredibly valuable stepping stone that helped the team visualize the necessary puzzle pieces for a real-world system.