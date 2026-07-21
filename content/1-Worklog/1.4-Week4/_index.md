---
title: "Week 4"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

Week 4 Objectives:
- Automate the Frontend deployment pipeline (CI/CD) using GitHub Actions.

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Research CI/CD concepts and how GitHub Actions workflows operate. | 08/05/2026 | 09/05/2026 | [GitHub Actions](https://docs.github.com/en/actions) |
| 2 | Create an IAM User with S3/CloudFront rights. Save keys in GitHub Secrets safely. | 10/05/2026 | 10/05/2026 | [GitHub Secrets](https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions) |
| 3 | Write a YAML workflow to checkout code, setup Node.js, and execute `npm run build`. | 11/05/2026 | 11/05/2026 | [Node.js Actions](https://github.com/actions/setup-node) |
| 4 | Add AWS Credentials action and the `aws s3 sync` command for automatic code upload. | 12/05/2026 | 13/05/2026 | [Configure AWS CLI](https://github.com/aws-actions/configure-aws-credentials) |
| 5 | Implement the `aws cloudfront create-invalidation` command to clear cache per deployment. | 14/05/2026 | 14/05/2026 | [CloudFront Invalidation](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Invalidation.html) |

Week 4 Achievements:

- Eliminated manual deployment tasks, significantly reducing human errors.
