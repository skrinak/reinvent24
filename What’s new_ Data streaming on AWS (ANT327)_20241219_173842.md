# Summary of AWS re_Invent 2024 - What’s new_ Data streaming on AWS (ANT327).txt

# Summary

## Main Points and Key Insights

### What's Important for Customers in Data Streaming

- **Performance**: Higher throughput and faster scaling are important for handling fluctuating data volumes and spikes.
- **Cost**: Lower overall cost of the streaming solution is desirable.
- **Resilience**: High availability, easy to build resilient applications, and ability to handle failures seamlessly.
- **Ease of Use**: Faster time to value, ease of integration, and ease of operations.

### Key Launches and Innovations

#### Performance and Cost

- **Kinesis Client Library (KCL) 3.0**: Provides better utilization of EC2 instances, reducing compute costs by up to 30%.
- **Amazon Managed Streaming for Apache Flink (MSF)**: Moved to per-second billing, enabling cost savings for jobs not running on hourly boundaries.
- **Amazon MSK Express Brokers**: Delivers up to 3x throughput and 20x faster scaling compared to Apache Kafka brokers, enabling consolidation and cost savings.

#### Availability and Ease of Use

- **Impact Detection and Avoidance**: Design principles to detect and mitigate failures before impacting customers.
- **Real-time Responsiveness**: Kinesis On-Demand Streams now support up to 10 GB/s write and 20 GB/s read throughput, and MSK Express Brokers offer 20x faster rebalancing.
- **Redundant Systems**: Cross-region replication and support for same topic name replication in MSK.
- **Choices**: A portfolio of services to meet different needs and stages of the streaming journey.
- **Sources and Sinks**: Broad range of integrations, including Amazon Data Firehose replicating database changes to Apache Iceberg tables on S3, and a DynamoDB Streams connector for Amazon MSF.
- **Agility**: Support for latest versions of Apache Flink and Apache Kafka, including in-place upgrades and rollbacks.

### Customer Story: Verizon

Verizon migrated from a self-managed Apache Kafka setup to Amazon MSK, addressing challenges like long maintenance windows, data loss, instability of observability platforms, and lack of scalability. The migration to MSK and Apache Kafka Connect on EKS provided benefits such as:

- Scalability and capacity: Easy scale-in and scale-out without downtime.
- Durability and availability: Minimal data loss (less than 0.1%).
- Reliability and maintenance: In-place upgrades and security patches without issues.
- Security: SCRAM and SASL-based authentication.

## Important Conclusions

AWS continues to innovate in the data streaming space, focusing on delivering high performance, cost-effectiveness, resilience, and ease of use for customers. The launches and innovations highlighted in this session aim to address the evolving needs of customers as streaming workloads become increasingly mission-critical. The customer story from Verizon showcases the real-world benefits of migrating to AWS managed services like Amazon MSK and leveraging the broad portfolio of streaming services offered by AWS.