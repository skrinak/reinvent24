# Summary of AWS re_Invent 2024-Zero-ETL replication to Amazon SageMaker Lakehouse & Amazon Redshift (ANT353-NEW).txt

# AWS re:Invent 2024 - Zero-ETL Replication to Amazon SageMaker Lakehouse & Amazon Redshift

## Summary

### Introduction

- The session discusses the challenges of building data pipelines and replicating data from various applications into data lakes and data warehouses for AI and analytics use cases.
- Nitin Bahadur, Head of Engineering for AWS Glue and Amazon AppFlow, shares his personal experience of wanting to help his daughter with her studies, which led to the realization of the need for a simplified data replication solution.

### Data Integration Challenges

- Data is stored and generated across multiple applications, including SaaS, on-premises, multi-cloud, and hybrid applications.
- Different applications use different protocols (REST, SOAP, JDBC, RPC) and mechanisms for data access and change tracking (full loads, incremental updates, deletes).
- Replicating data accurately requires handling inserts, updates, deletes, and schema changes, which can be complex and application-specific.
- True replication involves capturing all changes, including deletes, to ensure accurate insights and avoid data inconsistencies.

### Zero-ETL Solution

- Zero-ETL is an AWS initiative to eliminate or minimize the need for building custom ETL pipelines for common data ingestion and replication scenarios.
- The new launch expands zero-ETL to support data replication from various applications (Salesforce, ServiceNow, Zendesk, Salesforce Marketing, Facebook, Instagram Ads, Zoho CRM, and SAP) into Amazon SageMaker Lakehouse and Amazon Redshift.
- Zero-ETL simplifies data replication by providing intelligent connectors, handling inserts, updates, deletes, and schema changes, and applying changes to the target (Lakehouse or Redshift) while maintaining data integrity.
- Apache Iceberg is used as the open table format for data lakes, providing benefits like time travel, schema evolution, and data partitioning for query performance.
- For data warehouses (Redshift), changes are applied in a way that does not impact query performance or SLAs.

### Benefits

- Accelerates insights by simplifying and democratizing the ingestion process for application data.
- Cost-effective, with no additional licenses or connector fees, and pay-per-use pricing based on data ingested.
- Simplified maintenance, as AWS manages connector updates, pipeline maintenance, and integration with other AWS services.
- Enables accurate and up-to-date data for AI, analytics, and business decision-making.
- Reduces data integration time and related costs for customers.

### Demonstration

- A demonstration showcases the zero-ETL integration process, connecting to Salesforce, selecting objects, previewing data, and replicating changes (inserts, updates, deletes) into the SageMaker Lakehouse.
- The demo highlights the ability to query the replicated data, view data versions and changes over time using Apache Iceberg's time travel feature, and monitor changes in CloudWatch logs.

### Key Takeaways

- Zero-ETL simplifies data ingestion and replication from various sources, including applications, into data lakes and data warehouses.
- It addresses the complexities of handling inserts, updates, deletes, and schema changes, ensuring accurate and up-to-date data for AI and analytics use cases.
- The solution accelerates insights, is cost-effective, and simplifies maintenance by offloading operational burdens to AWS.
- Customers have reported significant reductions in data integration time and related costs by adopting zero-ETL.

## Conclusion

The session introduces the new zero-ETL capabilities for replicating application data into Amazon SageMaker Lakehouse and Amazon Redshift, addressing common data integration challenges. The solution aims to simplify and accelerate insights by providing a managed and cost-effective way to replicate accurate and up-to-date data from various sources, enabling AI, analytics, and better business decision-making.