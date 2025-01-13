# Summary of AWS re_Invent 2024 - How an analytics engineer uses AWS in a financial company (DEV212).txt

# AWS re:Invent 2024 - How an Analytics Engineer Uses AWS in a Financial Company (DEV212)

## Summary

### Introduction to Analytics Engineering

- Analytics engineering is a career that bridges the gap between data producers (software engineers, data engineers) and data consumers (data scientists, data analysts).
- It addresses the issue of data scientists spending a significant amount of time (around 70%) on data preparation and visualization tasks, leaving little time for core data science tasks.
- Analytics engineers work on both data production and consumption, organizing data in a logical way for data analysts to easily access and use.

### Skills Required for Analytics Engineering

#### Hard Skills
- Big data (distributed storage, parallel processing)
- Programming languages (SQL, Python, Spark)
- Cloud computing (Terraform, CloudFormation)
- Statistics
- Data visualization and storytelling
- Business knowledge

#### Soft Skills
- Communication
- Conflict resolution
- Creativity
- Critical thinking

#### AWS Services Commonly Used
- Analytics: Glue, EMR, Athena, Redshift, QuickSight, Kinesis
- Orchestration: EventBridge, Step Functions
- Storage: S3
- Security: IAM, Secrets Manager, KMS
- Additional: Lambda, ECS, VPC, Lake Formation, SageMaker, RDS, DynamoDB

### Analytics Engineering in Practice at Itau (Financial Company)

- Itau adopted a data mesh architecture with producer accounts, consumer accounts, and a central control plane account with Lake Formation for governance.
- Analytics engineers help bridge the gap between data engineers (producing data) and data scientists (consuming data).
- Benefits of involving analytics engineers:
  - Better understanding of business problems and translating them into technical solutions
  - Enabling data science teams to take features and models into production faster
  - Building specialized data layers with high-quality features for better machine learning models

### The Future of Analytics Engineering

- With the advent of the AI era and new services like Amazon Q and Amazon Bedrock, analytics engineers are expected to use AI tools to impact businesses with data.
- Analytics engineers will likely build tech products for data teams to consume data and make data-driven business decisions.
- Analytics engineering is projected to be one of the hottest careers in the coming years.

## Key Insights and Conclusions

- Analytics engineering bridges the gap between data producers and consumers, enabling more efficient data utilization and faster time-to-production for machine learning models.
- It requires a diverse set of hard and soft skills, combining technical expertise with business knowledge and communication abilities.
- AWS provides a range of services that support analytics engineering workflows, from data processing and analytics to orchestration and security.
- In the financial sector, analytics engineers play a crucial role in building specialized data layers and enabling data science teams to focus on core tasks.
- As AI continues to evolve, analytics engineers are expected to leverage AI tools to drive data-driven business impact, making it a promising career path for the future.