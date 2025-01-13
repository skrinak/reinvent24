# Summary of AWS re_Invent 2024 - Allianz Germany_ Accelerating legacy migration with generative AI (FSI323).txt

# AWS re:Invent 2024 - Allianz Germany: Accelerating Legacy Migration with Generative AI

## Overview

This session discusses how Allianz Germany leveraged generative AI and serverless architecture to accelerate the migration of legacy data from their old system to a new system. The traditional approach of manual data migration was proving to be time-intensive and inefficient, prompting the need for a more innovative solution.

## Key Points

### Project Scope

- Automatic or semi-automatic migration of 10,000 remaining contracts from the legacy system to the new system.
- Extraction of up to 150 attributes from contract documents (PDFs).
- Contracts are treated as the ground truth, rather than relying on data from the legacy system.
- Data quality varies between Allianz's own contracts and third-party contracts.

### Approach

- Serverless architecture for scalability and efficiency.
- Batch processing pipeline with daily uploads of relevant documents.
- Utilization of AWS services like S3, Step Functions, Lambda, and Amazon Bedrock.
- Integration of Claude 3.5 Sonnet (generative AI) for attribute extraction.
- Aggregation and ranking of extracted data to ensure the most up-to-date information.
- Human-in-the-loop principle with business users validating and accepting/declining extracted attributes.

### Benefits

- Significant time savings compared to traditional manual migration.
- Higher business user acceptance and involvement.
- Accuracy of up to 84% for certain data attributes.
- Rapid prototyping and evaluation through collaboration with AWS experts and Allianz data scientists.
- Scalable and serverless architecture for efficient processing.

## Takeaways

- Combine automated AI extraction with human-in-the-loop validation for optimal data quality.
- Develop an evaluation framework for prompt tuning and rapid iteration.
- Involve business users and leverage their domain knowledge throughout the process.
- Address data quality challenges, such as document classification, through careful data selection and business user input.

## Conclusion

Allianz Germany's innovative approach to legacy migration, leveraging generative AI and serverless architecture, has proven to be a disruptive and efficient solution. By treating contract documents as the ground truth and combining AI extraction with human validation, they have achieved significant time savings, higher data quality, and better business user acceptance.