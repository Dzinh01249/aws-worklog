---
title: "Self-Assessment"
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

This capstone essay summarizing my 12-week internship at the **AWS First Cloud Journey** program (04/2026 – 07/2026) serves as empirical evidence of the transformation from theoretical cloud computing concepts into highly practical technological solutions.

Within the framework of researching and developing the **'Pet Resort & Care System'**—a multi-service platform integrating e-commerce and pet care scheduling management—I collaborated with a team of 5 members to design and implement a distributed system based on a 3-Tier Architecture. The interactive frontend interface was developed using ReactJS, while the backend business logic micro-architecture was built on the Spring Boot (Java) platform. The system operates on the Amazon Web Services (AWS) infrastructure, utilizing core services such as Virtual Private Cloud (VPC) to ensure network spatial isolation, Elastic Compute Cloud (EC2) combined with an Application Load Balancer for workload orchestration, alongside a relational database Amazon RDS (Multi-AZ configuration) and ElastiCache (Redis) to enhance High Availability and optimize data retrieval performance. Through project practice, I have consolidated my mindset on network structural design, information security methodologies (Cloud Security), and particularly the strategic awareness of operational cost optimization (FinOps) in a distributed environment.

In addition to highly specialized technical activities, I actively participated in **three academic seminars and technology symposia** revolving around Cloud Architecture, Voice Artificial Intelligence (Voice AI), and Career Development Orientation. These forums not only served as catalysts in expanding my technological horizon but also helped me explicitly quantify the disparity between the academic environment and the rigorous technical demands of corporate enterprises.

Through the lens of objective self-reflection, I am profoundly aware that the current system architecture remains constrained to the limits of a Minimum Viable Product (MVP). The source code still possesses substantial room for refactoring to attain a higher degree of algorithmic optimization, and the system necessitates more comprehensive security auditing measures. In order to transparently present my competencies and provide a multidimensional perspective on the achievements obtained post-internship, I would like to outline my self-analysis and capability assessment based on the following system of practical criteria:

| No. | Criteria | Description | Good | Fair | Average |
| --- | ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | --- | --- | ---------- |
| 1 | **Technical Knowledge and Skills** | Understand the flow of a 3-Tier architecture, know how to configure basic VPC, EC2, and RDS, but lack deep performance optimization skills. | ☐ | ✅ | ☐ |
| 2 | **Learning Ability** | Quickly adapted to new concepts on the AWS Console, proactively searched for documentation when facing network drops or permission errors. | ✅ | ☐ | ☐ |
| 3 | **Proactiveness** | Voluntarily researched how to set up S3 Pre-signed URLs and updated the Architecture Diagram when receiving feedback from mentors. | ☐ | ✅ | ☐ |
| 4 | **Sense of Responsibility** | Maintained a complete 12-week worklog, closely followed assigned tasks in the team to avoid delaying the overall progress. | ✅ | ☐ | ☐ |
| 5 | **Discipline** | Attended team meetings and workshops regularly; however, sometimes tasks were piled up close to the deadline. | ☐ | ✅ | ☐ |
| 6 | **Progressive Attitude** | Willing to scrap the old architecture diagram and redraw it when realizing the flow was wrong; unafraid to admit the system's weaknesses. | ✅ | ☐ | ☐ |
| 7 | **Communication** | Conveying technical ideas is sometimes awkward; public speaking and presentation skills with mentors need significant improvement. | ☐ | ☐ | ✅ |
| 8 | **Teamwork** | Coordinated smoothly with the other 4 members, knew how to share AWS resources to avoid stepping on each other's toes during deployment. | ✅ | ☐ | ☐ |
| 9 | **Professional Conduct** | Respected the rules of the AWS community, listened to feedback, and maintained a proper attitude in a team environment. | ✅ | ☐ | ☐ |
| 10 | **Problem-Solving Mindset** | Debugging skills on the Cloud via CloudWatch are still slow; handling backend bugs like "double-booking" is not yet thoroughly resolved. | ☐ | ☐ | ✅ |
| 11 | **Contribution to the Project** | Completed assigned tasks regarding infrastructure architecture and wrote the deployment guidelines (README) for the Pet Resort project. | ☐ | ✅ | ☐ |
| 12 | **Overall** | Completed the internship with many hard-earned lessons; the system runs but needs a lot of refinement to meet actual production standards. | ☐ | ✅ | ☐ |

---

### What I Have Achieved During the Internship

**Technical Learning:**
* **Curing "Cloud Blindness":** Manually configured virtual networks (VPC), subnetting, and load balancers instead of merely learning theories on paper.
* **Architectural Lessons:** Understood the harsh difference between code running smoothly on Localhost versus code crashing when thrown onto an EC2 instance (hidden behind a Private Subnet).
* **Cost Awareness (FinOps):** Developed a healthy "fear of costs", learned how to clean up unused Snapshots, shut down idle NAT Gateways, and set up Billing Alarms.

**Attitude & Experience:**
* **Community Engagement:** Attended 3 AWS technical events/meetups, expanding my network and getting exposed to large-scale problems faced by real enterprises.
* **Documentation Discipline:** Maintained weekly Worklogs and learned how to package project documentation (even though it was time-consuming and sometimes tedious).
* **Honesty with Myself:** Dared to face the reality that our system still risks crashing under heavy load spam, rather than writing a report with inflated results.

---

### Limitations and Areas for Improvement

**Technical Skills:**
* **Code & Database Optimization Mindset:** The business logic code (e.g., cart handling, scheduling) is not yet optimal, still causing sync errors. I do not yet know how to properly index the Database for faster querying.
* **Weak Troubleshooting:** When the system crashes, I often spend way too much time fumbling through CloudWatch Logs because I haven't learned how to set up centralized logging.
* **Lack of CI/CD:** Deployments are still quite manual. The failure to integrate a professional automated CI/CD pipeline (like Jenkins or GitHub Actions) is a major shortcoming.
* **Security:** Although we used IAM and Secrets Manager, out of fear of breaking the app, the team sometimes granted overly broad IAM Roles that violate the Least Privilege principle.

**Soft Skills & Work Habits:**
* **Communication and Presentation:** I tend to lose confidence and over-explain when mentors challenge my technical decisions (e.g., why choose this service over another).
* **Time Management:** I often underestimate the time needed to fix a bug (thinking it takes 1 hour, but it actually takes a whole day), leading to last-minute sprints near the deadline.
* **Patience:** Sometimes I am too eager to see immediate results (like forcing Auto Scaling to run instantly) without deeply understanding the underlying AWS configuration principles.

> **Conclusion:** This internship was like a "wake-up call" that helped me soberly realize exactly where I stand in the IT industry. What I have achieved is just the ABCs. The journey ahead requires me to study much more seriously, particularly focusing on Containerization (Docker), CI/CD automation, and advanced system design thinking.