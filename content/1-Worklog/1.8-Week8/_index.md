---
title: "Worklog Week 8"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:
* Complete the packaging process of the Pet Shop Spring Boot source code into an executable archive (.jar) on the local environment.
* Research beginner-friendly cloud deployment solutions for hosting the backend application.
* Pivot research focus towards AWS Elastic Beanstalk after recognizing that manually managing an EC2 Linux server exceeds current technical capabilities.

### Tasks carried out this week:
| Day | Detailed Task | Start Date | Completion Date | Reference Material |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - Pause feature development to study the Build and Packaging lifecycle of a Spring Boot application.<br>- Read documentation covering Maven Lifecycles (Clean, Compile, Package). | 08/06/2026 | 08/06/2026 | Spring Boot Maven Docs |
| 2 | - Practice executing the `mvn clean package` command within the VS Code / IntelliJ terminal to build the Pet Shop backend into a `.jar` file.<br>- Resolve minor build failures related to skipped Test Cases. | 09/06/2026 | 09/06/2026 | StackOverflow / Java Blogs |
| 3 | - Close the IDE completely, open Windows Command Prompt, and execute the generated binary using the `java -jar petshop-backend.jar` command.<br>- Retest API endpoints via Postman to ensure stable standalone execution. | 10/06/2026 | 10/06/2026 | Java Documentation |
| 4 | - Review documentation for deploying the `.jar` file onto an Amazon EC2 instance.<br>- Realized that provisioning bare-metal EC2 requires Linux (Ubuntu) command-line skills and complex environment variable setups, posing a high risk of operational failure. | 11/06/2026 | 11/06/2026 | Amazon EC2 Linux Docs |
| 5 | - Discussed with the team and decided to pivot towards researching **AWS Elastic Beanstalk** (PaaS) – a managed service that allows direct `.jar` file uploads via the Web UI without requiring Linux command-line expertise. | 12/06/2026 | 12/06/2026 | AWS Elastic Beanstalk Guide |

### Week 8 Achievements:

* **Mastered Local Application Packaging Skills:**
  * Understood the operational difference between running source code inside an IDE versus executing an independently compiled binary.
  * Successfully utilized Apache Maven to compile and package the Spring Boot project into a complete, standalone `.jar` executable.
  * Ensured the backend application runs stably on the local Windows environment using the `java -jar` protocol, successfully connecting to the local database.

* **Developed Cloud Service Evaluation Mindset:**
  * Grasped the fundamental differences between IaaS (Amazon EC2) and PaaS (AWS Elastic Beanstalk) deployment models.
  * Accurately assessed personal technical limitations: proactively chose to bypass raw EC2 provisioning to avoid security and operational risks associated with a lack of Linux OS administration experience.

* **Defined a Safe Deployment Roadmap for Upcoming Weeks:**
  * Aligned on using AWS Elastic Beanstalk for the Pet Shop backend. This managed service handles EC2 provisioning, Java installation, and network configuration automatically under the hood, saving the team time and mitigating complex infrastructure setup errors.