# Summary of AWS re_Invent 2024 - HelloFresh’s data journey_ Insights from scaling to 1 billion meals (SEG207).txt

# HelloFresh's Data Journey: Scaling to 1 Billion Meals

## Introduction

- HelloFresh is a globally integrated food solutions group, operating in 18 markets across three continents.
- They experienced accelerated growth during the COVID-19 pandemic, delivering 1 billion meals in the last year with a total revenue of $7.6 billion.
- This accelerated growth posed challenges in handling the increased data volume and creating a scalable data platform.

## Initial Challenges

- A centralized data team became a bottleneck, overwhelmed by the sheer volume of data and new business contexts.
- Their first attempt at implementing a data mesh approach resulted in a "data mess" due to lack of a proper playbook and investment challenges.
- Key learnings:
  - Selling the idea was successful, but implementation lacked a clear strategy.
  - The existing platform targeted only data engineers, not the entire product team.
  - Lack of domain understanding and a global data model representing the business.

## The Tardis Data Platform

- After going back to the drawing board, HelloFresh developed the "Tardis" data platform, a multi-model unified data platform.
- Key features:
  - Seamless data integration from operational to analytical planes.
  - A global data model representing the business.
  - Easy onboarding through a CLI and UI for creating data products.
  - Abstraction of infrastructure complexities like permissions and Terraform.
  - Cost optimization through multi-tenancy.
  - Automated data modeling for data analysts.
  - Comprehensive training and documentation.

### Architecture

- The platform consists of three planes:
  - Management Plane: Interaction with the platform, onboarding, automation, monitoring.
  - Control Plane: Orchestration and user management (abstracted from users).
  - Data Plane: Ingestion, processing, serving layers, and storage (S3).
- Leverages AWS services like IAM, Glue, EMR (including EMR Serverless and EMR on EKS), and EKS for fault-tolerant cluster architecture.

## Adoption and Impact

- Over 650% growth in data assets created in the current year.
- More than 300% growth in the number of teams using the platform.
- Achieved the target of 15% of all squads in the organization using the platform within the same year.
- Positive user feedback on the user-friendly and intuitive platform.
- Enabled real-time data ingestion, transformation, and advanced modeling through a unified interface.
- Implemented data contracts with pre-flight and post-publish checks for data quality and trust.
- Enabled cost analysis and forecasting for better operational excellence and budgeting.
- Powered customer-centric products like HelloFresh+ with personalized rewards and a synchronized multi-channel experience.

## Key Learnings

- Decentralization should be purposeful, not just a buzzword.
- Involve the entire product team, including non-coders, and ensure they understand their new responsibilities.
- Measure success through adoption and real-life use cases that demonstrate ROI.
- Work backwards from internal and external customer use cases to ensure the platform's value.