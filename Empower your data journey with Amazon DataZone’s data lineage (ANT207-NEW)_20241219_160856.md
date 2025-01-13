# Summary of AWS re_Invent 2024 - Empower your data journey with Amazon DataZone’s data lineage (ANT207-NEW).txt

# Summary

## Main Points

1. **Data Lineage and its Importance**
   - Data lineage helps organizations understand the origin, movement, and transformation of data across their ecosystem.
   - It enables trust in data, impact analysis, troubleshooting, and governance.
   - Establishing data lineage is challenging due to the complexity of data ecosystems and the use of multiple tools and technologies.

2. **OpenLineage**
   - OpenLineage is an open-source standard and framework for capturing data lineage metadata.
   - It provides a specification and protocol for data pipelines to emit lineage events during execution.
   - It enables interoperability between different data processing frameworks and lineage consumers.
   - OpenLineage promotes extensibility through facets and a facet registry.

3. **Amazon DataZone and Data Lineage**
   - Amazon DataZone is a data management service that now supports data lineage based on the OpenLineage standard.
   - DataZone captures lineage events from AWS services like AWS Glue, Amazon Redshift, and third-party tools like dbt.
   - It provides a rich UI experience to visualize lineage diagrams, track data movement, and understand data transformations.
   - DataZone supports column-level lineage and versioning for troubleshooting and impact analysis.

4. **Customer Use Case: San Diego Gas & Electric**
   - SDG&E has implemented a data mesh architecture on AWS, with DataZone as the central governance platform.
   - They use DataZone for lineage, cataloging, glossary, and access controls.
   - SDG&E has developed a solution to capture lineage for on-premises data using AWS services and OpenLineage.
   - Lineage is crucial for compliance, building trusted data products, and establishing quantifiable trust in data.

5. **Integration with SageMaker Unified Studio**
   - DataZone powers the governance layer of the newly launched SageMaker Unified Studio.
   - Users can access data lineage and understand data origins within the SageMaker Unified Studio environment.

## Key Insights

- OpenLineage provides a standardized approach to capturing and sharing data lineage metadata, enabling interoperability across various data processing frameworks and lineage consumers.
- Amazon DataZone leverages the OpenLineage standard to provide a comprehensive data lineage solution, addressing key use cases such as trust, impact analysis, troubleshooting, and governance.
- Customers like San Diego Gas & Electric have successfully implemented DataZone as part of their data mesh architecture, enabling end-to-end data governance and lineage tracking, including on-premises data sources.
- The integration of DataZone with SageMaker Unified Studio brings data lineage capabilities to the machine learning and AI workflow, ensuring trust and transparency in data used for model development and deployment.

## Important Conclusions

- Data lineage is a critical aspect of data governance and data management, enabling organizations to establish trust, ensure compliance, and make informed data-driven decisions.
- The OpenLineage standard and Amazon DataZone provide a comprehensive solution for capturing, visualizing, and leveraging data lineage across various data sources, processing frameworks, and consumption points.
- Customers can benefit from the integration of DataZone with other AWS services and third-party tools, enabling end-to-end data lineage tracking and governance across their entire data ecosystem.
- The adoption of data lineage solutions like DataZone and OpenLineage can drive organizational adoption, knowledge sharing, and ultimately optimize the value derived from data assets.