---
title: "Worklog Week 4"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

Week 4 Objectives:
- Week 4 aims to modernize the development process by eliminating time-consuming manual deployments. The goal is to establish a fully automated CI/CD (Continuous Integration / Continuous Deployment) pipeline using GitHub Actions for the Frontend application.

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 08/05 | Began by deeply researching the concepts of CI/CD and how GitHub Actions operates. Learned about the `.github/workflows` directory structure, the concepts of workflows, jobs, steps, and actions. Created new AWS IAM Access Keys and Secret Keys with permissions restricted only to specific S3 and CloudFront resources, then securely stored them in GitHub Repository Secrets to protect cloud credentials. | 08/05 | 09/05 | |
| 10/05 | Initiated writing the YAML workflow file for the automated process. The script is set to automatically trigger upon any `push` or `pull_request` to the `main` branch. The steps include: checking out source code, setting up the Node.js 18 environment, installing dependencies (`npm ci`), running linter checks, executing the production build command, and finally using the `aws-actions/configure-aws-credentials` action to prepare for S3 upload. | 10/05 | 11/05 | |
| 12/05 | Added the AWS CLI command `aws s3 sync` to the workflow to synchronize the build directory to the S3 Bucket, deleting old, non-existent files. However, noticing users were still hitting old caches from CloudFront, I added a crucial step: executing the `aws cloudfront create-invalidation --paths '/*'` command immediately after S3 upload. This ensures CloudFront purges all caches at Edge Locations, forcing the delivery of the latest content. | 12/05 | 13/05 | |
| 14/05 | Executed a series of practical tests: modified text on a React component on the local machine, committed, and pushed to GitHub. Opened the Actions tab on the repository to monitor the running steps in real-time. Waited for the pipeline to report success (green tick), then reloaded the live website in the browser to confirm that the changes were reflected instantly without any further manual intervention. | 14/05 | 14/05 | |

Week 4 Achievements:

- Fully automated the process of pushing the latest source code from local to the production cloud environment.
- Minimized the risk of human error during operations, saving tens of minutes every time a UI update is desired.
- Deeply understood and successfully applied CI/CD principles, turning GitHub Actions into a powerful asset in the software development lifecycle.
