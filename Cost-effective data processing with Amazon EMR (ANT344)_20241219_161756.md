# Summary of AWS re_Invent 2024 - Cost-effective data processing with Amazon EMR (ANT344).txt

# AWS re:Invent 2024 - Cost-effective Data Processing with Amazon EMR

## Summary

### Overview of AWS Data Processing and Analytics Services
- AWS provides comprehensive access to data using open-source software, query engines, and tools for building, including Notebooks, visual ETL, and query editors.
- It supports popular frameworks like Apache Spark, Ray, and Python for transforming or preparing data at any scale.
- Real-time access to data is provided through streaming frameworks like Apache Flink and Spark Streaming.
- SQL engines like Trino are available for querying and analytics.
- Orchestration of these tools is possible without managing infrastructure, using managed workflows for Apache Airflow.
- Integration with Amazon SageMaker is available for data preparation, integration, troubleshooting, debugging, and code generation.

### Amazon EMR
- Amazon EMR provides performance-optimized runtimes for Apache Spark and Trino, enabling the best price-performance for big data and analytics.
- It offers flexibility in deployment options, including EC2, EKS, and serverless.
- EMR has best-in-class security with native fine-grain access control on Spark, improved CV handling, and TLS endpoint support.
- EMR stays current, making new open-source releases available within 30 days.

### Key Pillars for Cost-effective Data Processing

#### Scalability
- EMR provides flexibility in specifying up to 30 different instances during cluster provisioning and various allocation strategies.
- It supports large clusters with over 4,000 nodes and 500 different instance types.
- EMR offers real-time provisioning insights, such as insufficient capacity errors and timeouts.
- Automatic replacement of unhealthy nodes is supported, with graceful decommissioning and provisioning of new instances.
- Real-time alerts, events, and integration with existing observability and monitoring solutions are provided.

#### Price Performance
- EMR's optimized runtimes for Apache Spark and Trino offer significant performance improvements over open-source versions.
- Optimizations are enabled by default and are adaptive based on workloads, data, and infrastructure.
- EMR automatically tunes configurations like shuffle partitions, join selection, and executor sizing for optimal performance.
- It reduces S3 interaction by pushing down filters, parallelizing data access, and prefetching data.

#### Ease of Use
- EMR handles undifferentiated heavy lifting tasks like native integration with orchestration and observability systems.
- It provides a unified studio for data processing, generative AI, and machine learning.
- Flexibility across deployment options (EC2, EKS, serverless) is offered.
- Managed scaling with advanced scaling options (cost or performance optimization) is supported.

### Innovations in Practice

#### Choosing the Best EMR Deployment Model
- EMR on EC2 and EMR on EKS have EC2 costs (hourly pricing) and EMR service costs (hourly, ~25% of EC2 costs).
- EMR Serverless has no EC2 costs but consumption-based service costs based on vCPU and memory usage.
- Utilization is a key factor in determining the most cost-effective option, with a 70% utilization being the break-even point for On-Demand pricing.

#### Balancing Purchase Options and Instance Flexibility
- Use a mix of On-Demand and Spot instances on the same cluster for stability and cost savings.
- Diversify across Availability Zones, instance sizes, generations, and families for better Spot capacity and lower costs.
- Shorter Spark task runtimes (< 120s) are more effective on Spot due to less impact from interruptions.

### Roblox's Journey to Cost-effective Data Processing

#### Scale of Roblox's Data Platform
- Hundreds of petabytes of data stored in S3, increasing by tens of petabytes monthly.
- Trillions of events generated daily by internal services.
- Tens of thousands of active pipelines running.

#### Scaling Out EMR
- Moved from a shared cluster setup to scaling out by team and workload type.
- Developed internal tooling for self-provisioning EMR clusters and ensuring configuration consistency.
- Implemented blue/green deployments for zero-downtime updates.

#### Cost Savings Strategies
- Enabling S3 Intelligent Tiering for cold data.
- Migrating to newer EBS volume types (e.g., GP3) for better performance and cost.
- Consolidating clusters where possible and using Savings Plans for minimum compute usage.
- Automating job tuning and cluster auto-tuning to optimize resource utilization.
- Providing visibility into team-level efficiency and cost through internal portals.

#### Job Auto-tuning
- Automatically tunes job configurations (memory, executors) based on historical runs to optimize resource usage.
- Reverts to previous configurations if tuning fails to avoid disruptions.

#### Cluster Auto-tuning
- Adjusts managed auto-scaling configurations dynamically based on application and container pending metrics.
- Creates backpressure to hold clusters up as long as possible and minimize scaling up/down.

## Key Takeaways

- Always use the latest EMR release version for performance improvements.
- Use Instance Fleets and prioritized allocation strategy to diversify instances for better capacity and cost.
- Consider advanced managed scaling for balancing cost and performance optimization.
- Evaluate utilization when choosing EMR deployment options (EC2, EKS, serverless) based on cost.
- Mix On-Demand and Spot instances, favoring Spot for shorter Spark task runtimes.
- Implement automation for job tuning, cluster auto-tuning, and visibility into team-level efficiency and cost.