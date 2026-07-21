---
title: "Worklog Week 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

Week 3 Objectives:
- Officially deploy the entire built Frontend source code to a live network environment. Combine the use of Amazon S3 for static storage and Amazon CloudFront as a Content Delivery Network (CDN) to guarantee lightning-fast page load speeds anywhere in the world.

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 01/05 | Executed the Vite production build command (`npm run build`) to generate the `dist` folder containing fully minified and optimized static files. Accessed the AWS Console, created a new Amazon S3 Bucket. Exercised particular caution in configuring Block Public Access, deciding to disable it temporarily or use an appropriate bucket policy. Proceeded to manually upload the entire `dist` folder to the newly created S3 Bucket. | 01/05 | 02/05 | |
| 03/05 | Wrote and applied an S3 Bucket Policy in JSON format. This policy was carefully designed to only permit `s3:GetObject` permissions from external environments, completely blocking any unauthorized attempts to edit or delete files. Configured the static S3 endpoint and test-accessed the website via the default URL provided by S3 to ensure all resources loaded successfully. | 03/05 | 04/05 | |
| 05/05 | Provisioned an Amazon CloudFront Distribution to serve the Frontend globally. Specified the newly created S3 Bucket as the Origin Server. Established Origin Access Control (OAC) to secure S3, ensuring S3 only accepts requests routed through CloudFront. Configured Cache Behaviors, TTL (Time To Live), and Error Pages routing rules to return `index.html` in the event React's client-side routing encounters a 404 error. | 05/05 | 06/05 | |
| 07/05 | Utilized the Google Lighthouse tool in Chrome DevTools to comprehensively evaluate the performance, Accessibility, and SEO of the website after CDN deployment. Proceeded to fine-tune CloudFront by enabling automatic Brotli and Gzip compression features. Re-evaluated page load speeds, noting significantly reduced bandwidth usage and noticeably improved First Contentful Paint (FCP) times. | 07/05 | 07/05 | |

Week 3 Achievements:

- The Frontend of the Pet Resort & Care application officially and successfully 'Went Live', accessible smoothly via the internet.
- The application leverages the power of CDN (CloudFront) to cache data at Edge Locations, delivering lightning-fast access speeds to users.
- Accumulated practical experience in solving Single Page Application (SPA) routing issues on S3/CloudFront.
