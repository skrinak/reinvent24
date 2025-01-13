# Summary of AWS re_Invent 2024 - New York Life_ Data platform modernization to generative AI innovation (FSI324).txt

# AWS re:Invent 2024 - New York Life: Data platform modernization to generative AI innovation

## Introduction

This session covers New York Life's journey of modernizing their data platform and leveraging it for generative AI (gen AI) innovation. The speakers are:

- Scott Semanchik, Lead Architect at New York Life
- Boris Simanovich, Head of MLOps at New York Life
- Jimmy (AWS Solutions Architect)

## New York Life: Overview and Data Strategy

- New York Life is the nation's largest mutual life insurance company, focused on delivering exceptional experiences to agents and policyholders.
- Their data strategy aims to activate the power of data through enterprise AI and data products for meaningful business impact.
- The strategy is built on four pillars:
  1. Scale data foundation and technology
  2. Elevate data intelligence through AI and analytics
  3. Transform culture to data-driven decision-making
  4. Enable proactive and personalized experiences

## Data Platform Modernization

### Legacy Platform Challenges

- Existing Hadoop on-premises data lake reaching end-of-life
- Limited vendor support and deprecated platform
- Lack of ACID capabilities and performance limitations
- New requirements for diverse data personas and access

### Cloud Migration Approach

- Adopted a lakehouse architecture with S3 as the data lake and Redshift as the data warehouse
- Rearchitected and reengineered components, as well as lift-and-shift
- Collaborated with enterprise cloud platform team and departmental SREs
- Established architectural best practices and principles

### Data Ingestion and Processing

- Built a Glue framework with patterns for ingesting data (e.g., DMS, CDC, file ingestion)
- Implemented delta detection, standardization, and tokenization (PII/PHI) using Protegrity
- Maintained type 2 history in the data lake, with ongoing conversion to Iceberg format
- Leveraged Glue Data Catalog and AWS Lake Formation for access management

### Data Consumption

- Lifted and shifted data stage for ETL, with plans to migrate to Informatica IDMC
- Implemented Redshift clusters for ETL/ELT, data sharing, and segregated compute
- Integrated with operational data store (Amazon Aurora) for near real-time analytics

### Enabling Generative AI

- Centralized high-quality and reliable data in the data lake
- Ingested and processed unstructured data (e.g., Salesforce, Adobe, SharePoint)
- Implemented data governance and tagging for model usage
- Maintained data lineage and provenance

## MLOps and Generative AI Platform

### Guiding Principles

- Scalability (EKS)
- Automation (CI/CD pipelines)
- Reproducibility and versioning
- Governance and monitoring
- Modularity
- Security (data, LLM, and IP protection)
- Democratization of data science tools and platforms

### Development Architecture

- Data lake account for datasets (structured and unstructured)
- SageMaker Studio for exploratory data analysis
- GitHub for versioning and ML engineering templates
- ML pipelines for deployment to EKS

### Operational Architecture

- Modular architecture with separate teams for UI, AI solutions, and gen AI solutions
- OpenSearch serverless for vector database
- DynamoDB for storing prompts, completions, and model metrics
- Access to Bedrock for scaling and model selection

## Claims Management Experience: A Gen AI Use Case

### Problem Statement

- Highly manual process for generating custom letters based on complex medical records
- Legal exposure due to inconsistencies in letter writing
- Poor customer experience with long turnaround times and lack of clarity

### Solution Approach

- Collaborated with data team, business partners, AWS, and executive alignment
- Optimized data platform for unstructured data
- Built MLOps platforms and tooling
- Utilized LLMs for letter generation, guided by prompts and instructions

### Benefits

- Increased efficiency (from hours to minutes)
- Reduced legal risk through consistent tone and fact-based generation
- Improved customer experience with faster, more concise, and readable letters
- Leveraged Experience-Based Acceleration (EBA) from AWS for rapid delivery

## Lessons Learned

- Design for scale, but build iteratively
- Prioritize architectural reviews and follow AWS best practices
- Treat foundational models as commodities; focus on your data
- Fail fast and pivot quickly
- Break down organizational silos and foster collaboration
- Be firm on the vision, but flexible in execution
- Embrace change and innovate rapidly

## Conclusion

The session highlights New York Life's successful transformation journey, leveraging AWS services and best practices to modernize their data platform and enable generative AI innovation. The key takeaways emphasize the importance of collaboration, iterative development, architectural reviews, and embracing change to drive innovation.