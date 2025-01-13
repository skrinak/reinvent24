# Summary of AWS re_Invent 2024 - Achieve seamless and secure data sharing (ANT325).txt

# AWS re:Invent 2024 - Achieve Seamless and Secure Data Sharing

## Overview

This session focused on modern data architecture and leveraging data sharing to scale data analytics and enhance data collaboration within organizations while ensuring security. The key points covered include:

## Challenges in Data Sharing

- **Data Silos**: Data fragmented into multiple repositories, requiring additional ingestion costs and lacking engine interoperability.
- **Data Copies**: Data dispersed, requiring copies and synchronization, leading to reduced analytics accuracy.
- **Fragmented Governance**: Duplicated data access control across different environments, making synchronization difficult.

## AWS Solutions for Data Sharing

- **Data Discovery**: Enable efficient discovery and location of the right datasets, breaking down data silos.
- **Real-time Access**: Minimize delay and enable real-time data access without latency.
- **Data Governance**: Provide robust tools for data governance policies, enabling secure and compliant data sharing within and outside the organization.
- **Security**: Safeguard policies to protect personal and customer information.

## Data Sharing Use Cases

1. **Data Lake**: AWS Glue Data Catalog enables data sharing in a data lake by serving as a single source of truth for metadata and integrating with various services like Athena, Redshift Spectrum, and EMR.

2. **Data Warehouse**: Amazon Redshift data sharing allows sharing live, transactionally consistent data across data warehouses within and across regions, enabling architectures like data mesh and hub-and-spoke.

3. **Lakehouse**: Amazon SageMaker Lakehouse unifies data across Amazon S3 and Redshift, enabling powerful analytics and AI/ML applications on a single copy of data while securing data with AWS Lake Formation.

4. **Data Mesh**: Amazon DataZone empowers data producers and consumers to collaborate, enabling automated discovery, data governance, and federated computational governance.

5. **SageMaker Unified Studio**: The next-generation Amazon SageMaker provides a unified experience for data access, AI governance, and collaboration through the SageMaker Catalog, built on Amazon DataZone.

## Customer Use Case: Occidental Petroleum

Occidental Petroleum (Oxy) built the Oxy Data Analytics Platform (ODAP) using AWS services, enabling cloud scalability, democratized data access, flexible data stores and tools, and a decentralized architecture with federated data governance. Key highlights include:

- Leveraging AWS services like S3, Redshift, IoT SiteWise, DynamoDB, and DataZone for data ingestion, storage, and governance.
- Implementing a data mesh architecture with producer and consumer domains, enabling self-service data access and collaboration.
- Building applications like Delta Cipher, which provides instant natural language access to operational insights using generative AI and data from ODAP.

## Third-Party Data Sharing and Collaboration

- **AWS Data Exchange**: Offers five different ways to license third-party data faster and easier, including data files, Amazon S3, AWS Lake Formation, Amazon Redshift, and APIs.

- **AWS Clean Rooms**: Enables multi-party collaboration without sharing underlying data, using differential privacy, cryptographic computing, and programmatic access.

## Key Takeaways

- AWS provides a comprehensive set of solutions for seamless and secure data sharing, enabling organizations to break down data silos, enhance collaboration, and leverage advanced analytics and AI/ML capabilities.
- The next-generation Amazon SageMaker Unified Studio offers a unified experience for data access, governance, and collaboration, built on Amazon DataZone and the SageMaker Catalog.
- Customer use cases, like Occidental Petroleum's ODAP, demonstrate the power of AWS services in enabling data mesh architectures, federated governance, and innovative applications leveraging generative AI.
- Third-party data sharing and collaboration solutions, such as AWS Data Exchange and AWS Clean Rooms, facilitate secure data sharing and insights gathering without exposing underlying data.