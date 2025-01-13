# Summary of AWS re_Invent 2024 - Operate and scale managed Apache Kafka and Apache Flink clusters (ANT342).txt

# Summary

## Introduction
- This session covers operating and scaling managed Apache Kafka and Apache Flink clusters on AWS.
- Apache Kafka and Apache Flink are complementary technologies for building streaming data applications.

## Why Streaming Data?
- Customers want real-time insights for timely business decisions.
- Streaming data helps filter noise and get to the signal quickly, reducing costs.
- Streaming data keeps systems in sync, improving customer experience.

## Apache Kafka
### Challenges of Self-Managing Kafka
- Difficult to set up, scale, and achieve high availability out of the box.
- Operational overhead and infrastructure costs at scale.

### Amazon MSK (Managed Streaming for Apache Kafka)
- AWS's managed service for Apache Kafka, offloading undifferentiated heavy lifting.

### Express Brokers for Amazon MSK
- Eliminates storage management and configuration management.
- Unlimited storage capacity per broker, pay for data retention.
- Simplified provisioning and up to 3x more throughput per broker.
- Single-click vertical and horizontal scaling with minimal impact.
- Designed for mission-critical applications with codified best practices.

### Key MSK Features
- Multi-VPC connectivity for cross-account connectivity.
- MSK Replicator for single-click disaster recovery.

## Apache Flink
### Planning Flink Applications
- Multiple APIs (SQL, Table, DataStream, Process Function) for different use cases.
- Understand Flink's anatomy (JobManager, TaskManagers, checkpointing).
- Provision compute (Kubernetes, YARN) and durable storage (S3).
- Set checkpointing interval and retention policies.
- Monitor and auto-scale based on metrics.

### Scaling Flink Applications
- Increase parallelism (number of parallel task instances) for higher throughput.
- Reconfigure cluster (add nodes, restart job with savepoint) for new parallelism.

### High Availability for Flink
- Redundant TaskManagers with checkpointing for recovery.
- JobManager high availability with ZooKeeper or Kubernetes.

### AWS Managed Streaming for Apache Flink
- Fully managed and serverless Flink service.
- Simple planning and scaling with parallelism configuration.
- Rapid scaling (within 5 minutes) with warm pools.
- In-place version upgrades with automatic rollback.
- Start new jobs with savepoints from previous versions.

## Conclusion
- Streaming data is valuable for real-time insights, cost optimization, and system synchronization.
- Apache Kafka and Apache Flink are powerful but complex to operate at scale.
- AWS Managed Services simplify operations, scaling, and high availability for Kafka and Flink.
- Express Brokers for MSK and Managed Streaming for Apache Flink offer significant advantages over self-managing.