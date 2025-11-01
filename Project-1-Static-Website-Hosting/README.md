# Project 1 – Static Website Hosting on S3

## Goal
Deploy a secure, globally accessible static website using AWS S3, distributed through CloudFront CDN, and mapped to a custom domain via Route 53.

Architecture

Users request the website via domain (Route 53 DNS).
CloudFront delivers content globally via edge locations.
The static files (HTML, CSS, JS) are stored in S3.

AWS Services Used

Amazon S3 – for hosting website files (HTML, CSS, JS)
Amazon CloudFront – for content delivery and caching
Amazon Route 53 – for domain registration and DNS
AWS Certificate Manager (ACM) – for enabling HTTPS
IAM – for secure access contro

 Tools Used
- Amazon S3
- CloudFront
- Route 53
- IAM

 Steps
1. Created an S3 bucket and uploaded static HTML files.
2. Enabled static website hosting and made the bucket public.
3. Configured CloudFront distribution for global caching.
4. Linked domain using Route 53.
5. Set bucket policy and tested site via endpoint URL.

         +-------------------+
         |     User Browser  |
         +---------+---------+
                   |
                   ▼
          +----------------+
          |  CloudFront CDN|
          +--------+-------+
                   |
                   ▼
         +----------------------+
         |     S3 Bucket        |
         | (Static Website)     |
         +----------------------+
                   |
                   ▼
         +----------------------+
         |   Route 53 (DNS)     |
         +----------------------+


