# Week5 CI/CD Pipelines - Automation (Days 34–40)

## Goal

Automate builds, tests, and deployments using CI/CD.

## Time Commitment

1.5–2 hours per day, 5–7 days.

## What To Expect

By the end of Week 5, you should:

- Understand what CI and CD are
- Be able to write a simple GitHub Actions or Jenkins pipeline
- Automate at least building and testing of your containerized app

You are not expected to design full enterprise pipelines.

## Step-by-Step

1. Learn CI/CD concepts
   • Continuous integration vs delivery vs deployment
   • Stages: build → test → package → deploy.

2. GitHub Actions basics

   Overview:
   https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions

   Node.js workflow example:
   https://github.com/actions/starter-workflows/blob/main/ci/node.js.yml

   • Set up a simple workflow on push to main
   • Steps: checkout → install deps → run tests.

3. Add Docker build

   GitHub Actions with Docker:
   https://docs.github.com/en/actions/publishing-packages/publishing-docker-images

   • Extend your workflow to build a Docker image
   • Optionally push to Docker Hub (if you create an account).

4. Optional: Jenkins basics

   Getting started:
   https://www.jenkins.io/doc/book/getting-started/

• If you prefer, you can replicate the pipeline in Jenkins.

5. Connect CI to your K8s or VM deploy (stretch)
   • Add a job step that deploys updated image via kubectl or SSH script.

## Checklist

- You can explain CI vs CD
- You have at least one working GitHub Actions workflow or Jenkins pipeline
- Your app is built and tested automatically on push

## Projects to try

1. DevOps Two-Tier Flask App
   https://github.com/prashantgohel321/DevOps-Project-Two-Tier-Flask-App

2. Three-Tier Architecture Demo
   https://github.com/LondheShubham153/three-tier-eks-iac

## What Won’t Work

Building pipelines for five tools at once.
Start with one, get it working end-to-end.
