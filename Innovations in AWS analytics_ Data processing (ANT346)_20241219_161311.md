# Summary of AWS re_Invent 2024 - Innovations in AWS analytics_ Data processing (ANT346).txt

# Summary of AWS re:Invent 2024 - Innovations in AWS analytics: Data processing (ANT346)

## Introduction

- This session covers the announcement of the New SageMaker, a unified platform for all data, AI, and ML services on AWS.
- The New SageMaker platform consists of three key parts:
  1. SageMaker Lakehouse
  2. Unified Governance
  3. SageMaker Unified Studio

## SageMaker Lakehouse

- Brings together data warehousing capabilities of Redshift and data lake capabilities of Amazon S3 with Iceberg.
- Provides a unified consumption interface for data from various sources, including operational databases, SaaS vendors, and federated data sources.
- Utilizes the open-source Apache Iceberg standard for data access.

## Unified Governance

- Integrates the DataZone catalog and governance capabilities into the SageMaker platform.
- Provides business metadata management, data quality management, lineage tracking, and data classification.
- Extends governance capabilities to ML systems and Gen AI guardrails.

## SageMaker Unified Studio (Preview)

- A single experience for all AWS data processing products (EMR, Glue, Athena, MWA, Redshift, SageMaker AI, and Bedrock).
- Key features:
  - Unified Notebook: Polyglot notebook for using various data processing services.
  - Visual ETL: Drag-and-drop interface for building ETL pipelines.
  - Unified Query Editor: Run SQL queries across Redshift and Athena.
  - Data Browser: Access data from the SageMaker Lakehouse, federated sources, and Zero-ETL integrations.
  - Governance Capabilities: Business metadata management, data subscription workflow, and responsible AI features.
  - Amazon Q Integration: Natural language assistance for code generation, explanation, and refactoring.

## Innovations in Data Processing Services

- Performance and Cost Improvements:
  - AWS Managed Spark is 3.9x faster than open-source Spark.
  - Athena Trino engine is 2.77x more performant than open-source.
  - Graviton3 instances offer 20% better performance.
  - Managed Scaling for EMR and MWA for improved cost efficiency.
  - Usage Profiles in Glue for proactive cost control.

- Operational Excellence and Security:
  - Spark Native Fine-Grained Access Control (FGAC) at petabyte scale.
  - Concurrency and Queue Management in Glue and EMR Serverless.
  - Flexible deployment options with EMR (EC2, EKS, Spot, Graviton3, purpose-built instances).

- Gen AI-Powered Innovations:
  - Code generation for Spark and SQL using natural language prompts.
  - Root Cause Analysis for Spark job failures using Gen AI.
  - Automated Spark version upgrade analysis and code migration.

## Customer Use Case: Bridgewater

- Bridgewater is a systematic global macro asset manager that uses models to understand the world's economy and make investment decisions.
- They run over 1,000 models continuously, producing 300 million tables and 19 petabytes of data annually.
- Challenges:
  - Scalable infrastructure for spiky loads and data growth (80% data growth in the last 6 months).
  - Efficient data processing and anticipating user needs through pre-computation.
  - Enabling expert operators to diagnose and understand data anomalies quickly.

- Solutions:
  - Trino as the heart of their data processing, leveraging its relational algebra, UDF capabilities, and scalability.
  - Glue as the data catalog, enabling registration and access across multiple clusters.
  - EMR for flexible cluster configuration and easy upgrades.
  - Visualization tools built on top of Trino and EMR for data exploration and anomaly diagnosis.
  - Pre-computation and caching strategies to anticipate user needs and provide real-time responsiveness.
  - Metadata maintenance jobs to manage the Glue catalog and S3 bucket efficiently.

- AWS has been a transformational partner, enabling Bridgewater to scale their business and data processing capabilities with a small team.