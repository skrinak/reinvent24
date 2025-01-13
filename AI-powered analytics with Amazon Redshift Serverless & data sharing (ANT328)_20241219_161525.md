# Summary of AWS re_Invent 2024 - AI-powered analytics with Amazon Redshift Serverless & data sharing (ANT328).txt

# Summary

## Amazon Redshift Serverless & Data Sharing

### Introduction

- The session explores scalable multi-warehouse architectures with Amazon Redshift Serverless and seamless data sharing, enabling organizations to collaborate, innovate, and grow.
- It covers advanced concepts on building multi-warehouse architectures, real-world examples, and a demo showcasing the capabilities.

### Key Points

#### Amazon Redshift Serverless
- Automatically provisions and scales capacity, allowing customers to pay only for what they use.
- Enhancements include support for AWS PrivateLink, AI-driven scaling and optimization (up to 10x better price-performance), expanded RPU range (up to 1024 RPU), and expanded regional availability.

#### Amazon Redshift Data Sharing
- Enables sharing live transactional data across multiple data warehouses without copying data.
- Supports sharing data between provisioned clusters and serverless endpoints, within the same account, across accounts, or across regions.
- Facilitates use cases like workload isolation and chargeback.
- Recent enhancements include incremental materialized views, scope permissions, granular object-level permissions, and support for data lake tables.

#### Multi-Warehouse Writes through Data Sharing
- Generally available feature that allows writing to Redshift databases from different Redshift warehouses with just a few clicks.
- Enables scaling ETL workloads and processing with data sharing.
- Facilitates collaboration on shared datasets across teams.

#### AI-Driven Scaling and Optimization
- Automatically scales compute resources based on workload requirements and user-defined price-performance targets (cost optimization, performance optimization, or balanced).
- Employs workload forecasting, query forecasting, and machine learning models to make intelligent scaling decisions in near real-time.
- Provides consistent performance and optimizes cost or performance based on user preferences.

### Real-World Examples
- Logistics company: Implemented a multi-warehouse architecture with separate serverless endpoints for different data sets and workloads, improving performance and cost efficiency.
- Workforce management company: Consumed data from operational data stores using Amazon MSK into serverless, with data sharing for external and internal users, resulting in cost savings and better performance.
- Financial company: Deployed a true data mesh architecture with serverless instances, provisioned clusters, and data sharing for near real-time fraud detection analytics, meeting SLAs and achieving cost savings.

### Customer Journey: Hilton
- Hilton implemented a serverless architecture with data sharing to support a critical application with high concurrency and low-latency requirements.
- Evolved from a monolithic cluster to a multi-node serverless cluster with data sharing, achieving workload isolation, faster time to insights, reduced administrative overhead, enhanced productivity, chargeback capability, improved performance, and scalability.
- Demonstrated significant business value, including meeting SLAs, cost optimization, and self-service capabilities for business units.

### Best Practices
- Define ownership, appoint data stewards, and implement security and governance models for multi-warehouse architectures.
- Implement data mesh architectures for real-time data sharing and democratization of data access.
- Leverage AI-driven scaling and optimization, Amazon Redshift query monitoring rules (QMRs), and data security best practices.
- Implement cost management strategies, including AWS anomaly detection, automated reporting, and cost control capabilities in Redshift Serverless.
- Continuously gather feedback from users and evolve practices over time.
- Leverage Amazon Workload Replicator or Test Drive to test the conversion from monolithic to multi-warehouse architectures.

## Conclusion
The session provided a comprehensive overview of Amazon Redshift Serverless and Data Sharing capabilities, along with real-world examples and best practices for building scalable, intelligent, and cost-effective multi-warehouse architectures. The customer journey from Hilton demonstrated the significant business value achieved through the implementation of these technologies.