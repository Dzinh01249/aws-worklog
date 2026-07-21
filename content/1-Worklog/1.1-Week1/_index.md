---
title: "Worklog Week 1"
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

Week 1 Objectives:
- The first week focuses on initializing the project, establishing the foundational Cloud architecture, and rigorously preparing the development environment for the Pet Resort & Care system. The paramount objective is to thoroughly understand business requirements and ensure absolute security for cloud accounts before commencing any coding efforts.

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 17/04 | Conducted a detailed analysis of the Pet Resort & Care system requirements based on the descriptive documentation. Held team meetings to finalize core business flows such as user management, spa service booking, and the pet shopping cart. Constructed Use Case diagrams and outlined the software architecture following a basic Microservices approach for future scalability. Through extensive discussions, the team unanimously selected core AWS services, including Amazon S3 for static Frontend hosting, Amazon EC2 for the Spring Boot Backend, Amazon RDS for a highly consistent relational database, and Amazon VPC to ensure network isolation and enhanced security for the entire project system. | 17/04 | 17/04 | |
| 18/04 | Executed the registration of the AWS Free Tier account and established security layers to protect the Root account. Activated Multi-Factor Authentication (MFA). Applied AWS security best practices by setting up Identity and Access Management (IAM), creating Users and Groups with specific permissions strictly adhering to the Principle of Least Privilege. This preemptively shields the system from security risks right from the initial phase. | 18/04 | 18/04 | |
| 20/04 | Dedicated time to deeply research fundamental Cloud architectures and infrastructure deployment models. Conducted a comparative analysis of the pros and cons among various AWS services to make optimal decisions regarding cost and performance. Finalized the approach of using S3 Static Website Hosting integrated with CloudFront for the ReactJS Frontend, and utilizing EC2 virtual Linux servers connected to an RDS MySQL relational database for the Backend. | 20/04 | 20/04 | |
| 21/04 | Proceeded to set up the local development environment. Installed necessary tools including Node.js for the Frontend, Java JDK 17 and Maven/Gradle for the Spring Boot Backend, along with Git for source code management. Initialized a repository on GitHub, configured branch protection rules such as requiring Pull Requests and Code Reviews to ensure source code quality when working collaboratively. | 21/04 | 21/04 | |
| 22/04 | Researched Hugo - a blazingly fast static site generator framework written in Go. Performed the installation of the Hugo CLI, explored the directory structure, learned how to configure the config.toml/yaml file, and integrated available themes. The purpose of this was to prepare for building a professional internship report documentation website, which will record the entire progress, challenges, and lessons learned throughout the project's lifecycle. | 22/04 | 23/04 | |

Week 1 Achievements:

- Finalized the draft of the overall Cloud architecture diagram for the project, clearly identifying necessary AWS services.
- Successfully and securely set up the AWS account with full IAM/MFA security standards.
- Completely configured the local development environment and Git source code management system, ready for programming.
