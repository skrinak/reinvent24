# Summary of AWS re_Invent 2024 - Application modernization to meet a growing global demand (IMP211).txt

# AWS re:Invent 2024 - Application Modernization to Meet a Growing Global Demand

## Introduction

- The session focuses on the journey of JustServe.org, a website that connects volunteers with organizations in need, as they migrated from their legacy on-premises infrastructure to a cloud-native architecture on AWS.
- The migration was necessary to support JustServe's growing global demand and expand their reach worldwide.

## About JustServe.org

- JustServe launched in 2012 as a free platform to connect volunteers and organizations, providing opportunities for people to serve their communities.
- Organizations can register and list projects, ranging from large-scale efforts to small projects.
- Volunteers can search for projects based on interests, skillsets, and location, and sign up to help.
- Since its inception, JustServe has grown to over a million users, with over 17,000 organizations listing over 150,000 projects.
- JustServe has expanded to 17 countries and six languages.

## Legacy Architecture Challenges

- Initially, JustServe had a simple three-tier architecture with a load balancer, front-end servers, an API layer, and databases, all hosted in a single data center.
- Serving traffic from a single data center did not align with their global growth plans.
- Serving static assets from front-end web servers led to performance issues for users with limited bandwidth.
- Scaling was a painful, manual process that required weeks of advanced planning and resulted in wasted capacity or insufficient resources.
- The monolithic architecture made it difficult to optimize, extend, and maintain the application.

## Cloud Migration and Modernization

- To address their challenges, JustServe migrated to a cloud-native architecture on AWS.
- They now use CloudFront to serve static assets from S3, improving global user experience and performance.
- The application layer was moved to ECS Fargate, taking advantage of built-in auto-scaling.
- They migrated from a legacy on-premises database to Amazon Aurora and added a DynamoDB caching layer for frequently queried data.
- For new features like a newsletter subscription, they adopted a serverless architecture with API Gateway, Lambda, EventBridge, and SQS.

## Benefits of Cloud Migration

- Scalable and resilient global application capable of handling growing user demand.
- Improved DevSecOps practices with infrastructure as code, CI/CD pipelines, and automated testing environments.
- Cost optimization through ephemeral test environments and consumption-based pricing.
- Ability to seamlessly integrate new features and services.

## Challenges and Lessons Learned

- Optimizing for consumption-based pricing requires discipline in development practices.
- Observability and monitoring are crucial for asynchronous and serverless processes.
- Auto-scaling requires understanding application workloads and load profiles.
- Initialization time becomes important for auto-scaling and serverless resources.
- Choosing the right database for the architecture requires understanding workloads and access patterns.
- Cloud migrations can be complex, requiring proper dependency mapping and communication.
- Cultural shift for development teams accustomed to persistent access and environments.
- Understanding the existing application's components and makeup is essential for migration.
- Identifying business drivers and expected value helps maintain focus during the migration journey.
- Start small and gain experience, as there is no compression algorithm for experience.

## Conclusion

- The session highlights JustServe's successful migration to a cloud-native architecture on AWS, enabling them to meet growing global demand and improve their DevSecOps practices.
- It also provides valuable insights and lessons learned from their migration journey, which can be applied to other organizations embarking on application modernization and cloud migration.