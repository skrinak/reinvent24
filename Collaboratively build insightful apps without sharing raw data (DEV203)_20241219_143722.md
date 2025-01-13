# Summary of AWS re_Invent 2024 - Collaboratively build insightful apps without sharing raw data (DEV203).txt

# AWS re:Invent 2024 - Collaboratively Build Insightful Apps Without Sharing Raw Data (DEV203)

## Summary

### Introduction

- Esra Kayabali, a solutions architect at AWS, and Veliswa Boya, presented on the challenges of data collaboration and how AWS Clean Rooms can help organizations securely collaborate on data insights without revealing raw data.

### Data Collaboration Challenges

- Data fragmentation and silos: Data is scattered across different applications, channels, and partners, creating compatibility and scale challenges.
- Data proliferation: The amount of digital data created is rapidly increasing, making it difficult for companies to understand how data drives business outcomes.
- Evolving data landscape: Organizations need to balance data utilization with privacy concerns in an ever-changing environment.

### AWS Clean Rooms

- AWS Clean Rooms is a secure environment that allows organizations to collaborate on data insights without sharing raw data.
- It enables secure data analysis and insight generation with business partners while protecting sensitive information.
- AWS Clean Rooms addresses the need for secure and efficient data collaboration, analytics, and machine learning.

### Key Benefits and Use Cases

- Enhanced customer insights: Combine data from multiple sources to better understand customer preferences and patterns.
- Optimized marketing and advertising: Partner with media and advertising companies to enhance campaign effectiveness while protecting customer privacy.
- Improved reporting and measurement: Gain deeper business insights through secure analysis of combined data sets from multiple organizations.
- Accelerated research and development: Fast-track product and technology innovation by securely pulling expertise and data across organizations.

### AWS Clean Rooms Setup and Capabilities

- Easy to set up: Create a clean room in minutes using the AWS Management Console or API.
- Data stays in place: Connect existing AWS data sources without moving or uploading data to external environments.
- Configurable data access controls: Customize query restrictions, logging, and analysis rules for each participant.
- Flexible analysis: Use built-in analysis rules or custom SQL queries tailored to specific business needs.
- AWS Entity Resolution integration: Prepare and match related records to improve data across collective data sets.

### Demo: Setting Up an AWS Clean Rooms Collaboration

Veliswa Boya demonstrated the steps to set up an AWS Clean Rooms collaboration:

1. Create a collaboration: Define collaboration details, analysis engine, members, query controls, and result storage.
2. Add members: Invited members accept the collaboration and configure their data sources and analysis rules.
3. Configure data sources: Associate data tables from existing AWS data sources (e.g., S3, Athena, Snowflake) with the collaboration.
4. Define analysis rules: Specify aggregation, list, or custom analysis rules to control how data is analyzed and queried.
5. Run queries: The designated query runner executes queries within the collaboration to gain insights without exposing raw data.

The demo showcased a hypothetical use case where two tech communities (Java User Group and Python User Group) collaborated to analyze the overlap in their member bases to host a joint event.

### Getting Started with AWS Clean Rooms

- Start with a priority use case and a few partners to evaluate the value of collaboration.
- Determine partners, use cases, and success criteria for the AWS Clean Rooms collaboration.
- Predefine roles and responsibilities for setting up, configuring, and running collaborations.
- Evaluate insights and outcomes against success criteria after running collaborations.

## Conclusion

AWS Clean Rooms provides a secure and efficient solution for organizations to collaborate on data insights without sharing raw data. By addressing data fragmentation, proliferation, and privacy concerns, AWS Clean Rooms enables organizations to drive business value through secure data collaboration, analytics, and machine learning while maintaining control over sensitive information.