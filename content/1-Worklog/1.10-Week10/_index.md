---
title: "Week 10"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

Week 10 Objectives:
- Configure a Custom Domain and enforce HTTPS security certificates.

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Purchase a Custom Domain (`petresort-project.com`) and configure a Route 53 Hosted Zone. | 19/06/2026 | 20/06/2026 | [Amazon Route 53](https://aws.amazon.com/route53/) |
| 2 | Use AWS Certificate Manager (ACM) to request a free SSL certificate via DNS validation. | 21/06/2026 | 22/06/2026 | [AWS ACM](https://aws.amazon.com/certificate-manager/) |
| 3 | Update CloudFront to use the ACM SSL and enforce HTTP to HTTPS redirects. | 23/06/2026 | 23/06/2026 | [CloudFront HTTPS](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-https.html) |
| 4 | Add an HTTPS Listener (port 443) to the ALB and attach the security certificate. | 24/06/2026 | 24/06/2026 | [ALB HTTPS Listeners](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/create-https-listener.html) |
| 5 | Create Route 53 Alias Records mapping the domain to CloudFront and ALB DNS endpoints. | 25/06/2026 | 25/06/2026 | [Route 53 Routing](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-to-cloudfront-distribution.html) |

Week 10 Achievements:

- Entire system communicates over secure HTTPS with a professional domain name.
