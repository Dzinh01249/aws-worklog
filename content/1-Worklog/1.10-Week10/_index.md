---
title: "Worklog Week 10"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

Week 10 Objectives:
- The goal is to provide a professional appearance and comprehensive security for the project by utilizing a memorable Custom Domain and applying HTTPS encryption standards to protect transmitted data. This process will utilize Route 53 DNS services and security certificates from AWS Certificate Manager (ACM).

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 19/06 | Utilized the AWS Route 53 domain registration service (or a third-party provider) to purchase a professional domain name, e.g., `petresort-project.com`. Initialized a Hosted Zone in Amazon Route 53 and updated the Name Servers (NS) to route all DNS resolution traffic for this domain under AWS's management, preparing for more complex record configurations. | 19/06 | 20/06 | |
| 21/06 | Accessed AWS Certificate Manager (ACM) and requested a free Public SSL/TLS Certificate for both the root domain (`petresort-project.com`) and a subdomain (`api.petresort-project.com`). Opted for the DNS Validation method. ACM generated special CNAME records; I proceeded to add these CNAME records to the Route 53 Hosted Zone so AWS could automatically verify domain ownership and issue the certificates. | 21/06 | 22/06 | |
| 23/06 | Integrated the ACM security certificates into the services. Updated the Amazon CloudFront distribution (for Frontend) to use the newly issued SSL certificate, while simultaneously configuring the Viewer Protocol Policy to enforce 'Redirect HTTP to HTTPS'. Next, updated the Application Load Balancer (for Backend), added a Listener Port 443 (HTTPS), attached the ACM certificate to this Listener, and created a Rule to automatically redirect all traffic from Port 80 (HTTP) to Port 443. | 23/06 | 24/06 | |
| 25/06 | Completed the final puzzle piece by connecting the domain name to the AWS services. In Route 53, created Alias Records (A Records). The first record points the root domain (Frontend) straight to the CloudFront distribution's DNS address. The second record (the `api` subdomain) points straight to the Application Load Balancer. Waited for DNS propagation, then tested website access using the custom domain, confirming the secure padlock icon displayed on the browser's address bar. | 25/06 | 25/06 | |

Week 10 Achievements:

- The Pet Resort & Care project now possesses a professional, memorable Domain Name identifier, elevating the project's value.
- The entire data communication flow between end-users, web browsers, CloudFront, and the Backend ALB is encrypted to HTTPS standards, protecting against Man-in-the-middle attacks.
- Fully mastered the automated SSL certificate provisioning flow and intelligent DNS routing record management on the Cloud.
