# Summary of AWS re_Invent 2024 - BBVA_ Building a multi-region, multi-country data platform at scale (FSI310).txt

# BBVA: Building a Multi-Region, Multi-Country Data Platform at Scale

## Overview

BBVA, a global financial institution with presence in over 25 countries and 70 million customers, embarked on a strategic partnership with AWS in 2023. The goal was to transform into a data and AI-driven organization by leveraging AWS analytics and AI services to create a new global data platform. This platform would serve as a secure repository for BBVA's operations and customer data, providing automated business and marketing insights to increase operational efficiencies and attract new customers.

## Key Points

### Background
- BBVA's journey with data platforms started with siloed databases, then enterprise data warehouses, and eventually a big data platform called Datio.
- However, Datio faced challenges with complexity and scalability, prompting the move to AWS for unlimited scaling and managed services.
- The new platform, called ADA, is a global, multi-region platform with a unified console for over 6,000 advanced users and 40,000 data consumers.

### Architecture
- ADA combines the data mesh and data lakehouse architectures, using various AWS services like S3, Redshift, Glue Data Catalog, Lake Formation, EMR, and SageMaker.
- The platform is deployed in two regions (Europe and America) to avoid latency and be closer to operational systems.
- It manages over 4 petabytes of data, 30,000 tables, and executes 50,000 processes daily to load data, with a 40% annual growth rate.

### Key Lessons
1. **Complexity**: Migrating everything from on-premises to the new platform while running both in parallel was the most challenging part.
2. **Pre-migration**: Reducing the migration scope by 40% through housekeeping was crucial for project success.
3. **Regulatory Track**: Significant effort was required to convince regulators to move all data to the cloud.
4. **Shutdown**: Designing for the shutdown of the old platform from the beginning was essential.

### Migration Approach
- BBVA executed a parallel phase, running both platforms simultaneously for six months until the cloud data matched the on-premises data.
- A custom transfer system based on EMR and DistCP was developed to move data quickly, achieving rates of 500 TB in 30 hours.
- The goal was to have at least 95% of tables and all critical processes perfect before moving, and they achieved 97%.

### FinDataOps and Cost Management
- A FinDataOps department was created to manage budgeting, billing, cost visibility, governance models, cost protection, and best practices.
- Guardrails were implemented to prevent unintended consumption and provide cost protection and visibility for end-users.
- Custom dashboards based on the Cost and Usage Report (CUR) database were created for cost visibility at various levels.

### Future Roadmap
- Managing unstructured data and improving data sharing and collaboration between sandboxes.
- Integrating online inference with SageMaker and implementing a feature store.
- Exploring new data formats like Iceberg and real-time processing with Amazon Kinesis.
- Adopting services like EMR Serverless and Glue Data Quality for faster data engineering.

## Conclusion

BBVA's ADA platform showcases a successful large-scale migration of a global financial institution's data platform to AWS. The project leveraged various AWS services and architectures, implemented robust cost management strategies, and paved the way for future innovations in data and AI capabilities.