# Summary of AWS re_Invent 2024 - Innovations in AWS analytics_ Zero-ETL and data integrations (ANT348).txt

# AWS re:Invent 2024 - Innovations in AWS Analytics: Zero-ETL and Data Integrations

## Summary

### Introduction

- The session covers innovations in AWS Analytics with a focus on Zero-ETL and data integrations.
- Speakers: Jyoti Aggarwal (Product Manager, Amazon Redshift), Harshida (AWS), and Paul (Motive Technologies).

### Operational Analytics and the Need for Zero-ETL

- More enterprises are becoming data-driven, and data underpins major business transformation initiatives.
- Traditional ETL approaches often fail to meet the requirements for operational analytics and real-time data access.
- AWS is investing in a zero-ETL future to simplify data replication pipelines and provide direct access to data.

### AWS Data Strategy and Zero-ETL

- AWS has a purpose-built data strategy with a broad portfolio of databases and data warehouses, including Amazon Redshift.
- Zero-ETL is a fully managed tool by AWS that securely and efficiently replicates data from various sources to Amazon Redshift without the need for ETL pipelines.
- Zero-ETL supports 12 different sources, including Aurora, MySQL, PostgreSQL, RDS, DynamoDB, and SaaS applications like Salesforce, SAP, ServiceNow, and Zendesk.

### Zero-ETL Demonstrations

- Demos showcased zero-ETL integrations from relational sources (Aurora PostgreSQL), NoSQL sources (DynamoDB), and SaaS applications (Salesforce).
- Key features demonstrated include data filtering, refresh intervals, materialized views, data masking, and monitoring through AWS CloudWatch and Amazon Redshift System Views.

### Patterns and Use Cases with Zero-ETL

- Customers are using zero-ETL for various patterns, including incremental refresh with materialized views, data transformation with tools like DBT and AWS Glue, selective data replication, and role-based access control with dynamic data masking.
- Zero-ETL can be combined with existing ETL pipelines, data sharing, Amazon S3 auto-copy, and Amazon Streaming Ingestion for event-driven data sources.

### Customer Journey: Motive Technologies

- Motive Technologies provides solutions for the physical economy, including AI dash cams, fleet management, and spend management.
- Before zero-ETL, Motive had a complex data pipeline involving multiple sync methods, high latency, and significant operational overhead.
- By adopting zero-ETL, Motive simplified their data pipeline, reduced latency from hours to seconds, reduced effort and costs, and gained better visibility into data replication.
- Motive plans to leverage zero-ETL for their main vehicle message pipeline, migrate to Amazon MSK (Managed Streaming for Apache Kafka), and integrate with SageMaker Lakehouse for easier data migration and analytics.

## Key Insights and Conclusions

- Zero-ETL simplifies data replication pipelines, reduces operational overhead, and provides low-latency access to data for operational analytics.
- AWS offers a comprehensive zero-ETL solution supporting various data sources, including relational databases, NoSQL databases, and SaaS applications.
- Zero-ETL can be combined with other AWS services and tools for data transformation, streaming analytics, and event-driven data processing.
- Customers like Motive Technologies have experienced significant benefits from adopting zero-ETL, including simplified data pipelines, reduced latency, cost savings, and improved visibility into data replication.
- AWS continues to innovate in the zero-ETL space, with recent announcements like zero-ETL for SaaS applications and integration with SageMaker Lakehouse.