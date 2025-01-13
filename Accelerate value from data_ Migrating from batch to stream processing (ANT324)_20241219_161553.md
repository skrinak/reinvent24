# Summary of AWS re_Invent 2024 - Accelerate value from data_ Migrating from batch to stream processing (ANT324).txt

# Summary

## Introduction
- Data processing has evolved from clay tablets to digital records, with modern businesses producing diverse and continuous data streams.
- Business requirements now demand faster insights, AI/ML capabilities, and real-time data processing.
- Batch processing is insufficient for these modern needs, while stream processing can unlock greater value from data.

## Batch vs. Stream Processing
- Batch processing takes periodic snapshots of data and processes it in batches, leading to high latency.
- Stream processing ingests and processes data as it arrives, enabling near real-time insights and better customer experiences.
- Examples illustrate how stream processing outperforms batch processing for use cases like defect detection and AI-powered chatbots.

## Migrating to Stream Processing
### 1. Data Ingestion
- Move from pulling data to event-based mode using Change Data Capture (CDC) tools like AWS DMS or Debezium.
- CDC monitors database transaction logs and streams changes to a messaging system like Amazon MSK (Managed Kafka) or Amazon Kinesis.

### 2. Data Processing
- Use stream processing frameworks like Apache Flink (AWS Managed Service) to continuously process data in motion.
- Flink supports stateful processing, windowing, event correlation, and combining batch and streaming workloads.

### 3. Data Storage
- Write processed data to a data store like a data lake (e.g., Apache Iceberg) for analytics and BI.
- Iceberg supports upserts, schema evolution, and snapshot isolation, suiting streaming workloads.
- Consider append vs. upsert modes, small file issues, and handling concurrent updates.

## Sample Architecture
- A sample architecture integrates various AWS services:
  - Data sources (RDS, microservices) stream data to Amazon MSK or Kinesis.
  - Amazon Managed Streaming for Apache Flink processes data in motion.
  - Flink writes to Apache Iceberg data lake, OpenSearch (dashboards), and user notifications.

## Takeaways
- Streaming enables real-time insights and synchronization with 24/7 data.
- Streaming can satisfy both real-time and traditional BI/reporting use cases.
- AWS streaming tools are mature, cost-effective, and battle-tested for mission-critical workloads.
- Start small with streaming, experiment with provided workshops, and provide feedback.