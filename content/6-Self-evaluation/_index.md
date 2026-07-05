---
title: "Self-Assessment"
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

During my 12-week internship at **AWS First Cloud Journey** (from April 2026 to July 2026), I had the opportunity to learn, practice, and experience the real-world challenges of applying cloud computing knowledge to software system deployment.

I collaborated with a 5-member team to develop the **Pet Resort & Care System** project—a web application combining e-commerce and pet spa scheduling. The application was built using ReactJS and Spring Boot (Java) and deployed on AWS following a 3-Tier Architecture. We utilized core services such as VPC, EC2, Application Load Balancer, Amazon RDS (Multi-AZ), and ElastiCache (Redis). Through this project, I took my first steps in network infrastructure design, basic security configuration, and gained a deep awareness of cloud cost optimization (FinOps).

Additionally, I participated in **3 community technical events** regarding Cloud Architecture, Voice AI, and Career Orientation. These events broadened my horizons and helped me clearly see the gap between academic knowledge and corporate reality.

Reflecting on my journey, I acknowledge that the system we built is still at an MVP (Minimum Viable Product) stage, the codebase is not fully optimized, and there are still loopholes. To objectively reflect on my internship process, I would like to self-evaluate based on the following criteria:

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