## Week1 Cloud Foundations – Basics (Days 6–12)

## Goal

Understand how the cloud platforms are structured (regions, services, IAM, billing) and deploy at least one static site.

## Time Commitment

1.5–2 hours per day, 5–7 days.

## What To Expect

By the end of Week 1, you should:

- Be familiar with the console of at least one cloud provider
- Know what regions, AZs, compute, storage, networking, and IAM are
- Have deployed a static site once (even if you follow a guide closely)

You’re not expected to understand every service in the console.

## Step-by-Step

1. Pick a primary cloud (AWS/Azure/GCP)
   Choose one cloud as your main. The others are just context for now.

2. Intro path in your chosen cloud (2–3 sessions)
   AWS:
   https://explore.skillbuilder.aws/learn/course/134/aws-cloud-practitioner-essentials

   Azure:
   https://learn.microsoft.com/en-us/training/paths/az-900-describe-cloud-concepts/

   GCP:
   https://www.skills.google/course_templates/695

   Watch/complete modules on:
   • Regions / zones
   • Compute (VMs)
   • Storage (buckets / blobs)
   • Networking basics
   • IAM basics

3. Explore the console (1 session)
   • Log into your chosen cloud’s web console.
   • Find:
   • Compute section (EC2/VM/Compute Engine)
   • Storage section (S3/Blob/Cloud Storage)
   • IAM section
   • Click around and read labels. No need to create anything yet.

4. Deploy a static website (1–2 sessions)
   Example on AWS S3:
   https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html
   • Create a bucket
   • Enable static website hosting
   • Upload a simple index.html
   • Access it via the given URL

5. Look at billing/costs (short session)
   • Open the billing dashboard
   • Confirm free tier / very low usage
   • Get comfortable with where costs appear.

## Checklist

- You can describe what a region and AZ are
- You can name the compute and storage services in your chosen cloud
- You have deployed at least one static site
- You know where the billing dashboard lives

## Practice Resources

AWS:
https://explore.skillbuilder.aws/learn/course/134/aws-cloud-practitioner-essentials
https://docs.nginx.com/nginx/deployment-guides/amazon-web-services/ec2-install-nginx/
https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html

Azure:
https://learn.microsoft.com/en-us/training/paths/az-900-describe-cloud-concepts/
https://learn.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-portal

GCP:
https://www.cloudskillsboost.google/paths/15
https://cloud.google.com/storage/docs/hosting-static-website

OCI:
https://learn.oracle.com/ols/course/oracle-cloud-infrastructure-foundations/35673
https://docs.oracle.com/en/learn/install_nginx_ol8/index.html
https://docs.oracle.com/en-us/iaas/Content/Object/Tasks/usingcloudshellforhosting.htm

## What Won’t Work

Jumping straight into certifications or videos without touching the console.
Open the dashboard, create, and delete — that’s how it clicks.
