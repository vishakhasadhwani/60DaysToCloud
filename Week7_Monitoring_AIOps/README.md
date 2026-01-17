# Week 7 Monitoring & AIOps - Day2 Operations (Days 48–54)

## Goal

Monitor your systems, visualize their health, and understand the basics of AIOps.

## Time Commitment

1.5–2 hours per day, 5–7 days.

## What To Expect

By the end of Week 7, you should:

- Understand metrics, logs, and traces
- Set up Prometheus + Grafana for basic metrics
- Configure at least one alert condition
- Have a basic idea of what AIOps tools do

You don’t need a full production observability stack.

## Step-by-Step

1. Learn metrics and Prometheus

- Prometheus first steps:
  https://prometheus.io/docs/introduction/first_steps/

  • Run Prometheus locally
  • Scrape basic metrics from an app or node.

2. Visualization with Grafana

- Grafana Cloud (free):
  https://grafana.com/products/cloud/

  • Connect Prometheus as a data source
  • Build a simple dashboard (CPU, memory, request count).

3. Monitor Docker containers

- Tutorial:
  https://devopscube.com/monitor-docker-containers-using-prometheus/ (not getting)

  • Follow guide to monitor containers with Prometheus + Grafana.

4. CloudWatch or cloud native monitoring

- AWS CloudWatch basics:
  https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html

  • View metrics and logs for a resource (EC2 or similar).

5. Intro to AIOps

- AIOps overview:
  https://www.ibm.com/cloud/learn/aiops-explained

  • Understand how AI is used to detect anomalies, reduce noise, and suggest actions.

## Checklist

- You can explain metrics vs logs vs traces
- You have a basic Prometheus + Grafana setup running
- You are viewing at least one dashboard of your own app or system
- You know at a high level what AIOps is trying to solve

## What Won’t Work

- Ignoring monitoring until production.
- Start small, but start early.
