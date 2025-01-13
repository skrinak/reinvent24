# Summary of AWS re_Invent 2024 - Monitor and manage data quality (ANT343).txt

# AWS re:Invent 2024 - Monitor and manage data quality (ANT343)

## Summary

### Introduction

- The session emphasizes the importance of data quality in today's data architectures and how it is a critical component of data governance.
- Data quality is essential for improved decision-making, operational efficiency, and better user experience.

### Modern Data Approach on AWS

- AWS offers a modern data approach with four tiers: storage, data governance, act (build models, ETL pipelines), and experiences (dashboards, AI agents).
- Data governance focuses on three pillars: understand (metadata, cataloging), curate (data management, pipelines), and protect (data security, access).
- AWS services like AWS Glue, AWS Lake Formation, Amazon SageMaker, and Amazon DataZone support data governance and quality on AWS.

### AWS Glue Data Quality

- AWS Glue Data Quality offers a serverless, scalable, and high-performing platform for building data quality rules using open-source frameworks like deequ.
- It provides rule recommendations, built-in rules and actions, support for data at rest and in transit, anomaly detection, and data profiling.
- The Data Quality Definition Language (DQDL) allows authoring rules in an open and shareable format.
- Anomaly detection combines rule-based and machine learning-based data quality checks, providing insights and rule recommendations.

### Customer Use Case: Vanguard

- Vanguard built a custom data platform called G42, powered by AWS Glue Data Quality, to address their data quality needs.
- G42 has three layers: interaction (rule authoring, result review), orchestration (job queuing, monitoring), and execution (running Glue jobs, processing results).
- Vanguard uses DQDL and custom SQL for defining data quality rules and assigns them to workflows and data domains.
- The platform supports various data quality dimensions like consistency, veracity, completeness, and timeliness, using reference data and variance checks.
- Vanguard learned the importance of platforming (integrating data quality into operational processes), handling dynamic data, and choosing between detection or prevention of low-quality data.

### Key Insights and Conclusions

- Data quality is foundational for organizations and essential for decision-making, operations, and user experience.
- AWS Glue Data Quality offers a scalable and serverless platform for building data quality rules, anomaly detection, and data profiling.
- The Data Quality Definition Language (DQDL) enables open and shareable rule authoring.
- Combining rule-based and machine learning-based data quality checks through anomaly detection provides comprehensive data quality monitoring.
- Integrating data quality into operational processes, handling dynamic data, and deciding between detection or prevention of low-quality data are important considerations.
- Customer use cases, like Vanguard's G42 platform, demonstrate the practical implementation and benefits of AWS Glue Data Quality.