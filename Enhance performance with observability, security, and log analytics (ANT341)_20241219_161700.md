# Summary of AWS re_Invent 2024 - Enhance performance with observability, security, and log analytics (ANT341).txt

Here is a comprehensive summary of the transcript in Markdown format:

# AWS re:Invent 2024 - Enhance performance with observability, security, and log analytics (ANT341)

## Introduction

- Muhammad Ali, Principal OpenSearch SA at AWS, discusses how Amazon OpenSearch Service's features help build observability platforms for peak application performance and reliability.
- Rama Krishna from Cisco shares their journey of migrating to Amazon OpenSearch Service for observability of their WebEx Connect platform.
- Joshua Bright gives a sneak peek into newly launched features and a demo.

## Observability and Performance

- Performance and reliability are critical in sports and technology.
- Observability platforms collect telemetry data (logs, metrics, traces) to understand applications and infrastructure behavior.
- OpenSearch is a powerful tool for storing and analyzing large volumes of telemetry data for observability.
- Amazon OpenSearch Service is a fully managed service to run OpenSearch securely and reliably at scale.

## Instrumentation and Data Collection

- Agents collect telemetry data from applications and forward it to the observability platform.
- OpenTelemetry is a popular vendor-agnostic instrumentation framework supported by AWS.
- OpenTelemetry Collector sends data to OpenSearch Ingestion Service, which buffers, enriches, and stores it in OpenSearch.
- OpenSearch supports tiered storage with hot, warm, and cold tiers, including direct querying of data in S3.

## OpenSearch Dashboard and Analysis

- OpenSearch Dashboard provides a guided user experience with pre-configured widgets for log, trace, and security analytics.
- It offers monitoring, anomaly detection, and alerting capabilities without needing machine learning expertise.
- Trace analytics features like service maps, trace group metrics, and span details help analyze distributed tracing data.
- Log grouping, event context, and Piped Processing Language (PPL) aid in log analysis.
- Natural language query capability allows users to interact with logs using English prompts.
- OpenSearch Security Analytics plugin includes over 3,000 rules for security log analysis and correlation.

## Security and Compliance

- Amazon OpenSearch Service offers robust security features like authentication, fine-grained access control, and encryption.
- It complies with HIPAA, FedRAMP, and SOC standards.

## Cisco's Migration to Amazon OpenSearch Service

- Rama Krishna shares Cisco's journey of migrating WebEx Connect's observability to Amazon OpenSearch Service.
- WebEx Connect is an enterprise Communication Platform as a Service (CPaaS) handling billions of workflow executions and messaging monthly.
- Extensive logging, high throughput, and near real-time access were key requirements for their observability platform.
- They migrated from a self-hosted Elasticsearch setup to Amazon OpenSearch Service in 3-4 months without downtime.
- Benefits included 17% cost reduction, seamless upgrades, and AWS enterprise support for optimizations.

## New Features and Demo

- Joshua Bright demonstrates new features in the OpenSearch UI:
  - Connect to multiple OpenSearch clusters, collections, and external data sources like CloudWatch Logs and Amazon Security Lake.
  - Workspaces to organize dashboards, queries, and assets for teams and applications.
  - Improved user interface with a denser, brighter view and consolidated panes.
  - Unified query experience with SQL, DQL, PPL, and natural language support, including auto-complete.
  - Direct querying of external data sources like CloudWatch Logs and S3.
- The OpenSearch UI dashboard application is free, and there is a free trial for CloudWatch Logs and Security Lake data source connectors.

## Key Takeaways

- Amazon OpenSearch Service provides a robust observability platform for application performance and reliability.
- It offers powerful features for log, trace, and security analytics, with a guided user experience.
- Cisco successfully migrated their WebEx Connect observability to Amazon OpenSearch Service, reducing costs and operational overhead.
- New OpenSearch UI consolidates dashboards, queries, and external data sources into a unified experience with improved usability.