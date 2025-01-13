# Summary of AWS re_Invent 2024 - Drive innovation by implementing an industrial data strategy (MFG316).txt

# AWS re:Invent 2024 - Drive innovation by implementing an industrial data strategy (MFG316)

## Overview

This session provides a high-level overview of an industrial data strategy and how manufacturers can leverage their data to drive innovation. The speaker, Steve Blackwell, introduces the Industrial Data Fabric (IDF) framework, which is an architectural framework with best practices and patterns to simplify the way manufacturers can ingest, store, contextualize, and act on their industrial data.

## Key Points

### Industrial Data Landscape

- Manufacturers have a vast amount of data from various core systems:
  - CRM (Customer Relationship Management)
  - PLM (Product Lifecycle Management)
  - ERP (Enterprise Resource Planning)
  - MES/MOM (Manufacturing Execution System/Manufacturing Operations Management)
  - Industrial IoT data (PLCs, SCADA, data historians)
  - Connected devices IoT data

- To address quality issues or other use cases, manufacturers need to bring together data from multiple sources to gain meaningful insights.

### Industrial Data Fabric (IDF) Framework

The IDF framework consists of four layers:

1. **Ingest**: Bringing in data from different data sources.
2. **Store**: Storing the ingested data in multiple variations as it goes through its lifecycle.
3. **Contextualize**: Associating and contextualizing data from different sources (e.g., associating non-conformance with IoT data and part data).
4. **Act**: Enabling the use of data from a line of business perspective (e.g., triggering a workflow to create a work order in an MRO system based on predictive maintenance insights).

### Industrial Data Architecture

The industrial data architecture consists of three types of data:

1. **Time Series Data**: Data from PLCs, data historians, etc.
2. **Structured Data**: Data from MES, PLM, ERP, quality management systems, etc.
3. **Unstructured Data**: Video, images, Excel files, CSV files, etc.

The data is classified into hot, warm, and cold categories based on its age and usage:

- **Hot Data**: Data from the point of creation up to 5 minutes, used for real-time alerts and operator notifications.
- **Warm Data**: Data from 5 minutes after creation to the end of a shift or week, used for comparisons, queries, and dashboards.
- **Cold Data**: Data for analytics, machine learning, and BI reporting, further divided into bronze (raw data), silver (curated data for specific use cases), and gold (curated data for consumption by line of business).

### AWS Services and Partners

The presentation highlights various AWS services and partners that can be used to implement the industrial data architecture, such as AWS IoT SiteWise, Amazon Timestream, Amazon RDS, Amazon S3, Amazon SageMaker, AWS Glue, Amazon Neptune, Amazon Redshift, and partners like HighByte, Litmus, Siemens, NetApp, Snowflake, and Databricks.

## Important Conclusion

The session serves as a precursor to the speaker's chalk talk (MFG 301) on the following day, where he will delve deeper into the architectural patterns behind industrial data and its application for generative AI.