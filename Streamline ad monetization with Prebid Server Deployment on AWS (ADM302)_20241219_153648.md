# Summary of AWS re_Invent 2024 - Streamline ad monetization with Prebid Server Deployment on AWS (ADM302).txt

# Summary: Streamline Ad Monetization with Prebid Server Deployment on AWS

## Introduction

- Stephanie Layser, Worldwide Head of Publisher Ad Tech at AWS, and Mike Olson, Software Development Manager for AdTech and MarTech Solutions, presented a session on streamlining ad monetization with Prebid Server deployment on AWS.

## Customer Problem

- More omnichannel content providers are connecting directly with ad platforms to gain advantages such as:
  - Transparent auction mechanisms
  - Ability to modify decision logic
  - Full ownership of log-level data
  - Optimization towards product performance

## What is Prebid Server?

- Prebid Server is the most popular unified auction solution based on OpenRTB.
- It is an open-source, configurable solution that runs a transparent auction and connects to various bidders.
- Customers wanted to deploy Prebid Server but found the infrastructure challenging, leading to the development of the AWS solution.

## Prebid Server Deployment on AWS

- AWS provides a scalable, cost-efficient solution to deploy Prebid Server on your own AWS infrastructure.
- Key benefits:
  - Scalable to handle high-volume, low-latency workloads
  - Cost-effective deployment
  - Full control over decisioning logic and ownership of transaction data
  - Simple integration with BI tools and AWS services
  - Open-source and community-driven codebase

## Solution Architecture

- The solution includes a prepackaged, production-ready deployment of Prebid Server, fully supported and maintained by AWS.
- It handles the entire lifecycle of a Prebid auction request, from client-side to bidder integration and metrics collection.
- Key components include CloudFront, AWS WAF, ECS (Fargate), EFS, S3, AWS Glue, Athena, and CloudWatch.

## Getting Started

- Deploy using pre-generated CloudFormation templates or a CDK project (available on GitHub).
- Configure Prebid Server, including bidder adapters, client-side setup, and ad server integration.
- Monitor and maintain the deployment.

## What's Next?

- Incorporating customer feedback and adding support for video, AMP, and mobile.
- Building a transactional data layer to enable real-time decisioning and traffic shaping.
- Collaborating with customers to define and develop new features.

The session provided a comprehensive overview of the Prebid Server Deployment on AWS solution, its architecture, benefits, and future roadmap, enabling customers to streamline their ad monetization efforts.