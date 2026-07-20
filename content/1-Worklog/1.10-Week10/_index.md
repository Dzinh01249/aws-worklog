---
title: "Worklog Week 10"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

Week 10 Objectives:
- Bind custom domain via Route53, provision SSL certificates, and set up automated CI/CD Pipeline.

| Day | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Register Hosted Zone on Route53, create A records (Alias) pointing domain to CloudFront and ALB. | 28/06/2026 | 29/06/2026 | |
| 2 | Request free SSL certificate from AWS Certificate Manager (ACM), verify domain via DNS Validation. | 30/06/2026 | 01/07/2026 | |
| 3 | Attach SSL certificate to CloudFront (Frontend HTTPS) and ALB (Backend HTTPS), redirect HTTP → HTTPS. | 02/07/2026 | 03/07/2026 | |
| 4 | Write GitHub Actions workflow automation: build ReactJS → upload S3 → invalidate CloudFront cache on code push. | 04/07/2026 | 05/07/2026 | |

Week 10 Achievements:

- Entire Pet Resort system accessible via HTTPS with professional domain name.
- CI/CD Pipeline operational: every code commit auto-deploys Frontend to Cloud.
