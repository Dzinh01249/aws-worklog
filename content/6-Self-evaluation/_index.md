---
title: "Self-Assessment"
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

This self-assessment follows a prompt pattern: I review different knowledge areas learned during the internship, then explain how each area contributed to our group project.

During my 12-week internship at **AWS First Cloud Journey** (from April 2026 to July 2026), I practiced cloud deployment with a 5-member team building the **Pet Resort & Care System**. The app combines e-commerce and pet spa booking, built with ReactJS and Spring Boot, and deployed on AWS using a 3-Tier Architecture. Core services included VPC, EC2, Application Load Balancer, Amazon RDS (Multi-AZ), and ElastiCache (Redis). Through this project, I gained hands-on experience in network infrastructure design, basic security configuration, and cloud cost optimization (FinOps).

I also joined **3 community technical events** on Cloud Architecture, Voice AI, and Career Orientation. These events helped me bridge the gap between academic concepts and practical demands, especially for the team project.

I recognize that our system is still an MVP, with code that needs optimization and security that requires tightening. To reflect objectively, I evaluate myself using the criteria below:

| No. | Criteria | Description | Good | Fair | Average |
| --- | ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | --- | --- | ---------- |
| 1 | **Technical Knowledge and Skills** | Understands 3-Tier architecture and basic AWS services, but still needs deeper performance optimization for the project. | ☐ | ✅ | ☐ |
| 2 | **Learning Ability** | Quickly adapted to new AWS concepts and proactively searched documentation when facing cloud deployment issues. | ✅ | ☐ | ☐ |
| 3 | **Proactiveness** | Researched S3 Pre-signed URLs and updated the architecture diagram after mentor feedback. | ☐ | ✅ | ☐ |
| 4 | **Sense of Responsibility** | Maintained a complete 12-week worklog and followed team tasks to avoid delaying project progress. | ✅ | ☐ | ☐ |
| 5 | **Discipline** | Attended meetings and workshops consistently, though sometimes task management was rushed near deadlines. | ☐ | ✅ | ☐ |
| 6 | **Progressive Attitude** | Willing to redo architecture work and admit design mistakes to improve the project. | ✅ | ☐ | ☐ |
| 7 | **Communication** | Technical presentation is still awkward; I need to improve how I explain decisions to mentors and teammates. | ☐ | ☐ | ✅ |
| 8 | **Teamwork** | Coordinated effectively with 4 other members and shared AWS resources to avoid deployment conflicts. | ✅ | ☐ | ☐ |
| 9 | **Professional Conduct** | Respected AWS community rules, accepted feedback, and maintained a proper team attitude. | ✅ | ☐ | ☐ |
| 10 | **Problem-Solving Mindset** | Cloud debug speed is still slow; backend issues like booking conflicts need more robust handling. | ☐ | ☐ | ✅ |
| 11 | **Contribution to the Project** | Completed infrastructure tasks and wrote deployment guidelines for the Pet Resort project. | ☐ | ✅ | ☐ |
| 12 | **Overall** | Finished the internship with many lessons; the system works but needs further refinement to reach production quality. | ☐ | ✅ | ☐ |

---

### What I Have Achieved During the Internship

**Technical Learning:**
* **Cloud foundations:** I no longer feel lost in AWS. I can configure VPC, subnets, and load balancers, and I apply those configurations directly to our project.
* **Architectural insight:** I experienced how an app that works locally can fail on EC2; this taught me to think more carefully about network and deployment design.
* **Cost awareness:** I learned to manage cloud spending by cleaning unused resources, shutting down idle services, and setting billing alarms for the team project.

**Attitude & Experience:**
* **Community engagement:** Attending 3 technical events gave me real-world context and helped me bring better ideas back to the project team.
* **Documentation discipline:** I kept weekly worklogs and learned how to package project documentation, which improved our team handover quality.
* **Honesty with myself:** I accepted that our product is still early-stage and focused on practical improvements instead of overstating success.

---

### Limitations and Areas for Improvement

**Technical Skills:**
* **Code and database optimization:** Our project logic for cart and scheduling still has sync issues, and I need to learn better DB indexing strategies.
* **Troubleshooting:** When the project fails, I spend too much time in CloudWatch because I have not yet built a centralized logging mindset.
* **CI/CD deficiency:** Deployment remains manual. Introducing GitHub Actions or another automated pipeline is a key next step for the project.
* **Security practice:** We used IAM and Secrets Manager, but sometimes granted roles that were broader than the least privilege ideal.

**Soft Skills & Work Habits:**
* **Communication:** I need to be more confident and concise when explaining why I chose one AWS solution over another.
* **Time management:** I still underestimate the time needed for bug fixes, causing last-minute sprints.
* **Patience:** I sometimes rush to results before fully understanding AWS configuration details.

> **Conclusion:** This internship was a reality check that showed me where I stand in IT. The lessons learned are just the beginning; the project still needs stronger skills in Docker, CI/CD, and advanced system design.