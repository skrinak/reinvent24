# Summary of AWS re_Invent 2024 - Demystify and democratize access to your data with a business catalog (ANT202).txt

# AWS re:Invent 2024 - Demystify and democratize access to your data with a business catalog

## Introduction

### Importance of Context and Business Glossary

- Context is crucial for understanding data, just like in archeology where artifacts need context to be properly interpreted.
- A common language and agreed definitions (glossary) are necessary to provide context for data.
- Glossary terms, taxonomy (hierarchy), and ontology (formal definitions) help define and organize data entities and their relationships.

### The Role of a Business Data Catalog

- A business data catalog enriches data with broader context, enabling discovery and understanding.
- It bridges the gap between technical metadata (data types, partitions) and business context (glossary terms, use cases).
- It facilitates the association between data, actions, outcomes, and processes, enabling better data utilization.

## Building a Business Data Catalog on AWS

### Technical Metadata and Data Catalog

- AWS Glue Data Catalog stores technical metadata (schemas, partitions) for structured and semi-structured data.
- Glue Crawlers automate metadata harvesting from data sources.
- Data quality scores can be generated and stored in the Glue Catalog.

### Business Metadata and Data Catalog

- Amazon DataZone and Amazon SageMaker Data Catalog (powered by DataZone) enable business metadata management.
- Key components: metadata creation, data lineage, data quality, business glossary, metadata forms, and domains.
- Business glossaries and metadata forms add context and documentation to data assets.
- Data lineage helps understand data origins and impact analysis.
- Data quality scores from Glue are integrated into the business catalog.

### Metadata Creation and Documentation

- Producers (technical and business) document data assets using glossary terms and metadata forms.
- Metadata forms can be customized and made mandatory for publishing assets.
- Glossary terms can be directly assigned to assets or linked through metadata forms.
- GenAI can generate asset descriptions, summaries, and column-level documentation.

### Data Discovery and Consumption

- Consumers can search and filter data assets based on glossary terms and other metadata.
- Asset details include technical metadata, business context, data quality, and lineage.
- Consumers can request access and subscribe to data assets for consumption.
- Producers can approve/reject access requests and apply filters on data access.

## Customer Testimony: Bristol Myers Squibb

- BMS has been using DataZone for over a year, possibly the first to go into production.
- Key pillars: findable and understandable data, self-service infrastructure, and governed data access.
- Federated approach: central team manages standards, business catalog, and governance workflows; domain teams own local metadata and discovery.
- Progressive metadata completion based on maturity levels (local, cross-domain, enterprise).
- Achieved 5x more AI-ready data products in 18 months, better cost visibility, and reduced approval workflows.
- Future plans: data APIs, analytical product discovery, GenAI-assisted data publishing, chat with data, and codified access governance.

## Conclusion

The presentation covered the importance of a business data catalog in providing context and enabling data discovery and consumption. It showcased AWS services like Glue Data Catalog, DataZone, and SageMaker Data Catalog for managing technical and business metadata, data lineage, and data quality. The customer testimony from Bristol Myers Squibb highlighted their real-world implementation and benefits achieved using DataZone, including increased data product availability, better cost visibility, and streamlined governance processes.