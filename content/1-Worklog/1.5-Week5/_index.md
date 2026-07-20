---
title: "Worklog Week 5"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

Week 5 Objectives:
- Push Frontend to Amazon S3, integrate CloudFront global CDN, and establish WAF protection layer.

| Day | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Create S3 Bucket, enable Static Website Hosting, upload ReactJS build, and configure Bucket Policy for public access. | 19/05/2026 | 20/05/2026 | |
| 2 | Initialize CloudFront Distribution pointing to S3 Origin, configure cache behavior and TTL for optimal page load speed. | 21/05/2026 | 22/05/2026 | |
| 3 | Create Web ACL on AWS WAF attached to CloudFront, enable SQL Injection, XSS protection, and Rate Limiting rules. | 23/05/2026 | 24/05/2026 | |
| 4 | Audit and tighten Security Groups across all service tiers, test load speed via CloudFront domain. | 25/05/2026 | 26/05/2026 | |

Week 5 Achievements:

- Pet Resort Frontend live via S3 + CloudFront with fast global load times.
- Application protected by WAF layer against common attacks and deny-by-default Security Groups.
