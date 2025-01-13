# Summary of AWS re_Invent 2024 - SCC Public Health & AWS_ Collaborative public health data platform (PRO208).txt

# AWS re:Invent 2024 - SCC Public Health & AWS: Collaborative Public Health Data Platform

## Summary

### Introduction

- Rajeev Shirguppi (Senior Engagement Manager, AWS Public Sector ProServe) and TJ (Senior Consultant, AWS Public Sector ProServe) presented on implementing a comprehensive public health data platform for the County of Santa Clara, California.
- The mission was to improve and protect the health and well-being of the county's 2 million+ constituents, working with 70 partner agencies and 15 cities.

### Business Challenge

- Epidemiologists and data scientists had to work with siloed and fragmented data, spending more time wrangling data than analyzing it for meaningful insights.
- The goal was to provide a scalable, secure, and cost-effective AWS solution for automated, centralized, and harmonized public health data for analysis and reporting.

### Personas

- **Tom** (Epidemiologist): Needed automated reports with validated data sets for analyzing large, messy data sets.
- **Dr. Santa Clara** (Healthcare Officer): Needed timely access to complete data for decision-making, reporting, and serving constituents.

### Data Sources

- Major data sources included COVID-19 (CalREDIE), immunizations, contact tracing (Cal Connect), syndromic surveillance, and vital statistics (births and deaths).
- In total, 15 data sources were integrated, ingesting over 50 million records weekly.

### Solution Architecture

- Multi-AWS account architecture for isolation and granular security.
- Core account for orchestration using Step Functions and a configurable table for data source parameters.
- Data ingestion, validation, standardization, and PII obfuscation using AWS Glue, Amazon Macie, and Amazon Location Service.
- Data curation with SQL-based ETL (DBT) and ingestion-optimized data vault model (hub and satellite) in Amazon Aurora PostgreSQL.
- Distribution layer with query-optimized dimensional fact tables in Aurora PostgreSQL and S3 data lake.
- Encryption, monitoring, error handling, and CI/CD pipelines using various AWS services.

### AI/ML Use Cases

- **Identity Management**: AWS Glue FindMatches ML transform for deduplicating records and creating a golden record (EMPI) across data sources.
- **Handwritten Form Ingestion**: Amazon Textract for OCR and extracting data from PDF forms, with human-in-the-loop validation using Amazon A2I.

### Business and Technical Outcomes

- Deployed 13 out of 15 data sources, with 150+ ingestion views, 300+ curation and distribution tables.
- Identity management for 6 data sources, and PDF ingestion using Textract.
- Automated integration and deployment, with average processing time under 50 minutes.
- Public dashboards available on the Santa Clara County website.

### Lessons Learned

- Think big, start small, and get excited (roll out with a single data source first).
- Avoid over-complicating and analysis paralysis; stick to decisions and move forward.
- Include data modeling efforts and access to production-grade data in lower environments.
- Finish what you start, working backwards from the business outcome.