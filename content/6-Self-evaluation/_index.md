---
title: "Self-Assessment"
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

This final report concludes the entire 13-week Workshop series (17/04/2026 – 30/07/2026) within the **AWS First Cloud Journey** program. It stands as a clear demonstration of applying Cloud Computing theory into real-world practice through the **Pet Resort & Care System** project.

Over the 13 weeks of practical labs, our 5-member team collaborated to build a complete 3-Tier architecture. The frontend was built with ReactJS, and the backend logic was handled by Java Spring Boot. The entire platform was deployed on AWS infrastructure: network isolation via VPC, computing through EC2, load balancing with ALB, and data storage using RDS (Multi-AZ) and ElastiCache Redis. These lab sessions not only solidified my setup skills but also deepened my understanding of security (Security Groups, WAF) and infrastructure cost optimization (FinOps).

Frankly speaking, while the current project operates stably, it remains at the MVP (Minimum Viable Product) level. Below is my self-assessment evaluating my competencies after 13 weeks of hands-on experience:

| No. | Criteria | Description | Good | Fair | Avg |
| --- | --- | --- | --- | --- | --- |
| 1 | **Technical Skills** | Mastered the 3-tier model; hands-on configured VPC, EC2, RDS, ALB. Need to explore more on database query optimization. | ☐ | ✅ | ☐ |
| 2 | **Learning Agility** | Quickly grasped AWS Console services; proactively read docs to self-troubleshoot IAM permissions and network connections. | ✅ | ☐ | ☐ |
| 3 | **Proactiveness** | Proposed CloudFront configuration to boost page load speed; proactively redrew architecture diagrams when spotting errors. | ☐ | ✅ | ☐ |
| 4 | **Responsibility** | Consistently wrote full 13-week worklogs; ensured personal tasks didn't delay the team's deployment progress. | ✅ | ☐ | ☐ |
| 5 | **Discipline** | Fully attended all lab sessions and presentations. Sometimes pushed documentation tasks too close to the deadline. | ☐ | ✅ | ☐ |
| 6 | **Progressive Mindset** | Willing to delete resources and start over if misconfigured; unafraid to admit architectural flaws. | ✅ | ☐ | ☐ |
| 7 | **Communication Skills** | Improved ability to discuss technical issues with mentors, though I need more confidence during project defense. | ☐ | ✅ | ☐ |
| 8 | **Team Collaboration** | Clear task division via Trello; seamlessly shared AWS accounts without causing resource conflicts. | ✅ | ☐ | ☐ |
| 9 | **Professionalism** | Adhered to security best practices; always open to expert feedback to refine the system. | ✅ | ☐ | ☐ |
| 10 | **Debugging Mindset** | Reading CloudWatch logs has improved, but tracking down hidden bottlenecks remains a bit slow. | ☐ | ☐ | ✅ |
| 11 | **Project Contribution** | Took primary responsibility for writing Workshop Docs and supported teammates in debugging the backend. | ✅ | ☐ | ☐ |
| 12 | **Overall Evaluation** | Successfully met the 13-week series goals. The project runs smoothly but has room for expansion (e.g., full CI/CD). | ☐ | ✅ | ☐ |

---

### Highlights of the Internship
- **Hands-on Cloud Competence:** Transformed paper architecture into a live system. Confidently navigated VPC routing, IAM permissions, and Load Balancer setups.
- **Solving Real-world Problems:** Understood how to resolve network conflicts and securely connect a Frontend (S3) to a Backend (EC2) residing in a Private Subnet.
- **Documentation Mindset:** Writing worklogs in a workshop-style format helped systemize all knowledge, proving useful for myself and future learners.

### Areas for Improvement
- **Technical Gaps:** Have not fully implemented CI/CD (only basic for Frontend). Backend CI/CD to EC2 is still done manually via SCP.
- **Optimization:** Database Indexing skills to speed up queries aren't solid yet; the system might face bottlenecks during sudden traffic spikes.
- **Soft Skills:** Need to hone my debate skills during technical Q&A with Mentors, and learn to manage time better to avoid crunching in the final weeks.