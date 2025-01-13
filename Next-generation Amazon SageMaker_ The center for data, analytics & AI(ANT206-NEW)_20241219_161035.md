# Summary of AWS re_Invent 2024-Next-generation Amazon SageMaker_ The center for data, analytics & AI(ANT206-NEW).txt

# Summary of AWS re:Invent 2024 - Next-generation Amazon SageMaker

## Introduction

The session introduces the next generation of Amazon SageMaker, which is designed to address the evolving needs of customers in the era of generative AI. The key components of the next-generation SageMaker are:

1. **SageMaker Unified Studio**: A unified development environment for data processing, SQL analytics, machine learning, and generative AI app development.
2. **SageMaker Catalog**: An enterprise-wide catalog for data and ML assets with governance capabilities like PII detection, data quality, and data lineage.
3. **SageMaker Lakehouse**: A unified lakehouse catalog across Redshift, S3-based data lakes, and federated data sources, enabling access to data across the entire data estate.

## SageMaker Unified Studio

The SageMaker Unified Studio is a unified development environment that provides:

- Integrated tools for data processing (Spark, SQL), machine learning, and generative AI app development.
- Integration with Amazon Q for code generation, data exploration, and natural language interactions.
- Git integration for version control and collaboration.
- Project-based development, allowing users to group code, data, ML assets, and compute resources.
- Responsible self-service compute provisioning.
- Integration with existing AWS services and third-party tools.

### Key Concepts

- **Domains**: Model your organization, accounts, and workloads.
- **Projects**: Group resources (code, data, ML assets, compute) for end-to-end analytics or AI applications.
- **Project Roles**: Define access permissions for project members within each account.
- **Environments**: Enable additional capabilities and compute resources for projects.
- **Blueprints**: Provision resources within projects in a governed manner.
- **SageMaker Catalog**: Publish and subscribe to data and ML assets across accounts and regions.

## SageMaker Catalog and Lakehouse

- **SageMaker Catalog**: An enterprise-wide catalog for data and ML assets, with governance capabilities like PII detection, data quality, and data lineage.
- **SageMaker Lakehouse**: A unified lakehouse catalog across Redshift, S3-based data lakes, and federated data sources, enabling access to data across the entire data estate.

## Guest Speaker: Chris Jackson (olympics.com)

Chris Jackson, from olympics.com, shared their unique challenges and how the next-generation SageMaker can help address them:

- Unpredictable and bursty workloads during the Olympics, requiring rapid provisioning of resources.
- Increasing number of data workers (up to 1,000) requiring access to data.
- Complex web of partner organizations, necessitating robust governance and access controls.
- Extensive use of AI and generative AI, demanding scalable infrastructure.

## Conclusion

The next-generation Amazon SageMaker aims to provide a unified experience for data, analytics, and AI development, with embedded governance and the ability to break down data silos across the entire data estate. It addresses the evolving needs of customers in the era of generative AI and enables organizations to adapt and adopt this technology efficiently.