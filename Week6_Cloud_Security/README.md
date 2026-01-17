# Week6 Cloud Security IAM & Secrets (Days 41–47)

## Goal

Secure access, identities, and secrets in your cloud setup.

Time Commitment

1.5 hours per day, 5–7 days.

## What To Expect

By the end of Week 6, you should:

- Understand IAM, roles, policies, and least privilege
- Know how to store secrets securely
- Enable basic logging/auditing (CloudTrail or equivalent)

You’re not expected to be a security engineer, just not reckless.

## Step-by-Step

1. Learn IAM fundamentals

- Official AWS IAM best practices:
  https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html

- Concepts: user, role, policy, group
- Principle of least privilege.

2. Create limited IAM roles/users

- Create a user without admin rights
- Attach an S3-only policy or similar minimal permission
- Test access.

3. Learn secrets management

- Secrets Manager tutorial:
  https://docs.aws.amazon.com/secretsmanager/latest/userguide/tutorials_basic.html

- Store a dummy DB password
- Retrieve it securely (CLI or SDK).

4. Learn KMS basics

- AWS KMS:
  https://docs.aws.amazon.com/kms/latest/developerguide/overview.html

- Understand customer-managed keys vs AWS-managed keys
- See how encryption at rest works.

5. Enable CloudTrail and review logs

- CloudTrail setup:
  https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-create-and-update-a-trail.html

- Turn on a trail
- Perform a few actions and see them show up in logs.

6. Read about cloud security patterns

## OWASP Cloud Security: MUST READ

    https://owasp.org/www-project-cloud-native-application-security-top-10/

## Checklist

- You can explain IAM user vs role vs policy
- You have created a non-admin IAM user or role
- You have used a secrets manager once
- You have enabled or explored cloud audit logs

## What Won’t Work

Using admin roles for everything.
If you can’t explain “least privilege,” you’re doing security wrong.
