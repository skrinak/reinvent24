# Summary of AWS re_Invent 2024 - Fortifying the news pipeline_ AP_s resilient media supply chain on AWS (IMP204).txt

Here is a comprehensive summary of the transcript, formatted in Markdown with appropriate headers and bullet points:

# AWS re:Invent 2024 - Fortifying the News Pipeline: AP's Resilient Media Supply Chain on AWS

## Introduction

- The Associated Press (AP) is one of the most trusted sources of fast, accurate, and objective news in the world, with a mission to keep the public informed about global events.
- AP has been a leader in the news industry since 1846, constantly adopting cutting-edge technologies to process, create, and distribute news.
- AP's partnership with AWS aims to build a resilient architecture that allows them to stay up and running during major news events and traffic spikes.

## AP's Technology Platform

- AP has a custom-built platform that runs on AWS, responsible for:
  - Receiving content from journalists in the field (text, photos, videos)
  - Processing and distributing the content globally
  - Providing access to customers through web portals and APIs

- The platform follows a serverless architecture pattern, using services like API Gateway, Lambda, S3, SQS, and SNS.
- Content distribution is event-driven, with services communicating through a serverless pub-sub message bus.

## The Journey to the Cloud

- Initially, AP lifted and shifted their on-premises systems to AWS, but realized that this approach had limitations:
  - Costs didn't decrease significantly, and in some cases, increased.
  - Management burdens of operating instances persisted.

- AP realized that refactoring and rewriting applications to be cloud-native was necessary to fully leverage the scale and capabilities of AWS.

## The Need for Multi-Region Resilience

- As AP's serverless footprint grew, they observed:
  - Software changes were more likely to cause issues than hardware failures.
  - Services within a region have a higher degree of interconnectivity, leading to cascading failures.
  - Software-oriented outages tended to last longer than hardware-related ones.

- These observations led AP to the decision to run all critical workloads in a minimum of two AWS regions for resilience.

## Evaluating Multi-Region Deployment

- The decision to go multi-region requires careful evaluation, considering factors such as:
  - Tolerance for replication latency and inconsistency
  - Consistency models of data storage services
  - Maturity of the development process (CI/CD, testing, etc.)

- Data replication strategy is crucial and can make or break a multi-region solution if it's too complex or unmanageable.

## AP's Multi-Region Implementation

- AP initially tried using S3 cross-region replication but found the SLA did not meet their latency tolerance.
- They emulated S3 events with their own software and used DynamoDB global replication for faster data replication.
- For regional health checks, AP implemented a pattern where applications call a health endpoint to learn the closest healthy region.
- AP moved global DNS management out of AWS Route 53 to avoid control plane dependencies during outages.

## Key Takeaways

1. **App Modernization Innovation Accelerates Beyond Lift and Shift**: AP started with a lift-and-shift approach but realized the need for cloud-native modernization to fully leverage AWS capabilities.

2. **Multi-Region Requires Careful Evaluation**: Not every workload needs to be multi-region. Adding unnecessary complexity can be detrimental if the workload is not architected properly.

3. **Aggressively Pursue Simplicity**: AP customized known patterns and best practices from AWS to meet their specific needs, keeping solutions as simple as possible.

## AWS Services and Best Practices for Resilience

- AWS Resilience Hub: Manage and improve the resilience posture of workloads, define resilience goals, and implement recommendations.
- AWS Fault Injection Simulator: Run controlled chaos engineering experiments to identify failures before they become outages.
- Amazon Application Recovery Controller: Prepare for and complete faster recovery for applications running on AWS, including multi-AZ and multi-region recovery.
- AWS Elastic Disaster Recovery Service (DRS): Minimize downtime and data loss by quickly recovering servers on AWS in case of disruptions.
- Observability tools (CloudWatch, X-Ray, Container Insights, etc.): Continuously monitor infrastructure, applications, and networks.
- Control plane and data plane operations: Design disaster recovery operations to avoid control plane dependencies.
- Chaos engineering principles: Inject failures and non-failure events to test and harden the resilience of workloads.

## Next Steps

- Read the latest headlines, breaking news, and videos at APNews.com and download the AP mobile app.
- Attend other related sessions at the event, featuring non-profit customers discussing natural disaster recovery, data governance, and more.
- Connect with AWS account managers for further assistance and guidance.