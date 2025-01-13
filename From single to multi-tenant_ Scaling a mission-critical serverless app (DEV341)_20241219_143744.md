# Summary of AWS re_Invent 2024 - From single to multi-tenant_ Scaling a mission-critical serverless app (DEV341).txt

# Summary: From Single to Multi-Tenant: Scaling a Mission-Critical Serverless App

## Introduction

- The session discusses the transition from a single-tenant to a multi-tenant architecture for a mission-critical serverless application at PostNL, the Dutch National Postal Service.
- The application, Event Broker E-Commerce (EBE), is an event broker that facilitates decoupling and integration between various producer and consumer applications.

## Single-Tenancy vs. Multi-Tenancy

### Single-Tenancy
- Each consumer has dedicated resources (compute, data, configuration) in the application.
- Advantages:
  - Enhanced security
  - High resilience
  - Customization per consumer
  - Suitable for strict compliance requirements
- Disadvantages:
  - Higher costs due to multiple resources
  - Scaling challenges
  - Longer deployment times
  - Maintenance complexity

### Multi-Tenancy
- Multiple consumers share the same resources in the application.
- Advantages:
  - Cost-effective
  - Better scalability
  - Faster deployments
- Disadvantages:
  - Potential "noisy neighbor" issues (resource contention)

## EBE Migration to Multi-Tenancy

- Constraints: No downtime, no input required from consumers/producers.
- Migration stages:
  1. HTTPS Producer Migration
  2. SQS Producer Migration
  3. SQS Consumer Migration
  4. HTTPS Consumer Migration

### Key Changes
- Replaced individual resources (API endpoints, Lambda functions) with shared components.
- Moved compute resources out of consumer stacks, leaving only infrastructure.
- Introduced shared ingress and egress Lambda functions.
- Utilized DynamoDB for producer and consumer configurations.
- Employed step-by-step migration to ensure no message loss.

## Results and Benefits

- Faster deployments (1 minute vs. 8 minutes for producer/consumer creation).
- No redeployment required for software upgrades (shared components updated).
- Cost savings by removing redundant resources (CloudWatch alarms, AMSEs).
- Better Lambda utilization and optimization opportunities.
- Addressed "noisy neighbor" issues with ESM concurrency control.

## Conclusions

- Start with single-tenancy for simplicity, compliance, and customization requirements.
- Consider multi-tenancy for scaling and cost optimization as the application grows.
- Hybrid architectures (combining single and multi-tenancy) are possible.
- Continuously revise and optimize the architecture as needed.