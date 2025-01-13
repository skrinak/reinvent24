# Summary of AWS re_Invent 2024 - Maximize efficiency and reduce costs with Amazon OpenSearch Service (ANT347).txt

# Summary

## Amazon OpenSearch Service Overview

- OpenSearch is an open-source search and analytics platform licensed under Apache 2.0.
- Amazon OpenSearch Service is a managed version of OpenSearch, providing scalability, security, and availability on AWS.
- Amazon OpenSearch Serverless is a serverless deployment option, decoupling compute from storage.

## Cost Optimization Strategies

### Vector Search Workloads

- Vector search workloads are memory-intensive, and costs are driven by memory requirements.
- Use vector quantization techniques (color, binary, product quantization) to reduce vector dimensions and memory footprint.
- Approximate k-NN search with algorithms like IVF and HNSW can provide a good trade-off between accuracy, speed, and cost.
- Scalar quantization and approximate k-NN offer the best balance of speed, accuracy, and cost for vector search workloads.

### Amazon OpenSearch Serverless

- Serverless architecture separates compute and storage layers, allowing independent scaling.
- Specialized collection types (time series, search, vector search) optimize infrastructure and sharding strategies.
- Automatically scales up and down based on workload spikes, reducing operational overhead.

### Amazon OpenSearch Ingestion Service

- Fully managed data ingestion service powered by Data Prepper (open-source data collector).
- Integrates with popular data sources (Kafka, OpenTelemetry, S3, databases) and provides out-of-the-box transformations.
- Offers 38+ blueprints (templates) for quick setup of ingestion pipelines.
- Automatically scales to handle workload demand, accelerating integration with other services.

### Amazon OpenSearch Service (Provisioned)

- OR1 instances with segment replication and remote storage (S3) improve indexing throughput and price-performance.
- Use Graviton instances (R6gd, R7gd) for better memory bandwidth, compute performance, and networking bandwidth.
- Intel Xeon Scalable instances offer up to 30% better price-performance and lower storage latency.
- Consider reserved instances (RI) for up to 48% savings over on-demand pricing.
- Upgrade from I3 to IM4gn instances for higher storage density and cost savings.

### Storage Tiering and Zero ETL

- Leverage hot, warm (UltraWarm, OR1), and cold (Zero ETL, S3) storage tiers for cost optimization.
- Zero ETL enables direct querying of data on S3 without ingesting, using serverless compute.
- Optimize with skipping indexes, materialized views, and covering indexes for S3 data.

### Efficient Cost Optimization Patterns

- Use Amazon S3 events with OpenSearch Ingestion Service to write logs directly to S3.
- Leverage OR1, Zero ETL, and OpenSearch Ingestion Service for a low-cost pattern, writing data to S3 and querying from there.

## Trellix Use Case

- Trellix, a cybersecurity company, achieved over 35% cost savings by migrating to Amazon OpenSearch Service.
- Challenges included billions of events ingested daily, petabytes of data to search, and operational overhead.
- Optimizations included using UltraWarm and warm nodes, reducing replicas, tuning sharding strategies, and leveraging OR1 instances.
- Implemented index state management policies, monitoring, and compression with OpenSearch Ingestion Service.
- Improved indexing performance by 40% and enabled near-real-time data availability.

## Key Takeaways

- Leverage Amazon OpenSearch Serverless for operational simplicity and reduced overhead.
- Optimize vector search workloads using quantization techniques and approximate k-NN search.
- Utilize Amazon OpenSearch Ingestion Service for streamlined data ingestion and integration.
- Consider provisioned instances (OR1, Graviton, Intel Xeon Scalable) and reserved instances for cost savings.
- Implement storage tiering with hot, warm, and cold tiers (UltraWarm, Zero ETL, S3) for cost optimization.
- Explore efficient cost optimization patterns like S3 events with OpenSearch Ingestion Service and OR1 with Zero ETL.