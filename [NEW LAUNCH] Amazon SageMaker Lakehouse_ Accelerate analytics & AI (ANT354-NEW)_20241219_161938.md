# Summary of AWS re_Invent 2024 - [NEW LAUNCH] Amazon SageMaker Lakehouse_ Accelerate analytics & AI (ANT354-NEW).txt

# Summary

## Main Points

1. **AWS SageMaker Lakehouse** is a new launch that aims to unify data lakes and data warehouses, providing flexibility and openness of data lakes with the performance and transactionality of data warehouses.

2. The Lakehouse brings together Amazon S3 data lakes and Amazon Redshift data warehouses, making the data accessible through open Iceberg APIs to any Iceberg-compatible engine like EMR, Glue, Athena, or third-party applications.

3. It offers integrated security controls, including fine-grained permissions at the row, column, and cell levels, for centralized access management.

4. The Lakehouse provides three storage options:
   - General-purpose S3 buckets (existing data lakes)
   - New S3 table buckets (preview) with higher throughput for transactional data lakes
   - Redshift Managed Storage (RMS) for transactional workloads with automatic optimizations

5. It uses the existing Glue Data Catalog as a unified technical catalog, allowing flexible data hierarchies and organization across different storage systems.

6. Zero-ETL capabilities enable ingesting data from various sources, including AWS databases, enterprise applications, and federated queries, directly into the Lakehouse.

7. The Lakehouse is part of the next-generation SageMaker platform, which includes the SageMaker Unified Studio for a unified experience across data processing, SQL analytics, machine learning, and application development.

## Key Insights

- Customers can bring their existing data lakes and Redshift data warehouses into the Lakehouse without data migration, making the data immediately accessible through Iceberg APIs.
- The Lakehouse aims to simplify data management by providing a unified experience and eliminating data silos, inconsistent access controls, and complex architectures.
- It offers storage flexibility, allowing customers to choose the appropriate storage option based on their workload requirements (e.g., RMS for transactional workloads, S3 for data lakes).
- The Iceberg APIs enable interoperability, allowing any Iceberg-compatible engine to access data across different storage systems without creating data copies.
- The integrated security controls and fine-grained permissions ensure consistent access management across all query engines and tools.

## Important Conclusions

The AWS SageMaker Lakehouse addresses common challenges faced by customers in managing data across data lakes and data warehouses. By unifying these systems and providing open APIs, storage flexibility, and integrated security controls, the Lakehouse aims to simplify data management, improve interoperability, and accelerate time-to-value for analytics and AI workloads.