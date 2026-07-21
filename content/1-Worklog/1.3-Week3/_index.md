---
title: "Week 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

Week 3 Objectives:
- Deploy the Frontend to AWS using S3 and CloudFront CDN.

| Date | Tasks | Start Date | End Date | References |
|------|-------|------------|----------|------------|
| 1 | Run production build. Create an Amazon S3 Bucket and manually upload the `dist` folder. | 01/05/2026 | 02/05/2026 | [S3 Upload](https://docs.aws.amazon.com/AmazonS3/latest/userguide/upload-objects.html) |
| 2 | Configure JSON S3 Bucket Policy to allow public internet read access (`s3:GetObject`). | 03/05/2026 | 04/05/2026 | [S3 Policies](https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html) |
| 3 | Create an Amazon CloudFront Distribution pointing to S3 for CDN acceleration. | 05/05/2026 | 05/05/2026 | [CloudFront Intro](https://aws.amazon.com/cloudfront/) |
| 4 | Configure Origin Access Control (OAC) to secure S3 from direct non-CDN access. | 06/05/2026 | 06/05/2026 | [CloudFront OAC](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html) |
| 5 | Set up CloudFront Error Pages to return `index.html` for React Router 404 fallbacks. | 07/05/2026 | 07/05/2026 | [CloudFront Error Pages](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/custom-error-pages.html) |

Week 3 Achievements:

- Frontend is live on the internet with extremely fast loading speeds via CDN.
