# Summary of AWS re_Invent 2024 - How Vanguard rebuilt its mission-critical trading application on AWS (FSI322).txt

Here is a comprehensive summary of the transcript in Markdown format:

# AWS re:Invent 2024 - How Vanguard Rebuilt its Mission-Critical Trading Application on AWS

## Introduction

- Vanguard, one of the world's largest investment firms, leveraged AWS to rebuild and modernize their mission-critical trading platform.
- The existing platform was a legacy, on-premises monolithic system that was becoming increasingly expensive to maintain and lacked scalability and resilience.
- The modernization effort aimed to achieve improved scalability, resiliency, agility, customer satisfaction, and reduced total cost of ownership (TCO).

## Vanguard's Growth and Changing Landscape

- Vanguard has over 50 million clients worldwide with $9.9 trillion in assets under management.
- The company has experienced significant growth, with a 100x increase in brokerage trading volume over the last 15 years.
- Factors driving this growth include the rise of ETFs, the elimination of commission fees, the launch of advisory services, and the introduction of new features like tax loss harvesting and direct indexing.
- To meet the increasing demand and changing landscape, Vanguard needed a modern, scalable, and resilient trading platform.

## Modernization Strategy

- Vanguard embarked on a transformative journey to modernize the entire brokerage trading platform from a monolithic architecture to a three-tier architecture comprising a frontend client experience, APIs, and data.
- The new system would be robust, scalable, and comprised of over 100 distributed systems, handling 80 million trades per year and $1 billion in daily notional value.
- The modernization was planned as a multi-year effort, delivering value incrementally to maximize value for Vanguard's business and clients.

## Technical Decisions and Debates

### Database

- Vanguard chose Amazon Aurora PostgreSQL as the primary database for the trade engine, considering factors like data complexity, access patterns, resiliency, and cost.
- To achieve high availability and low RTO/RPO, Vanguard worked closely with the Amazon Aurora team to adopt improved failover and switchover capabilities, including a global writer endpoint.
- Vanguard also implemented a multi-domain database approach, combining accounts, positions, orders, and securities data into a single database for efficient processing.

### Compute

- Vanguard standardized on Amazon ECS and Fargate for hosting modernized microservices, leveraging AWS for heavy lifting and operational simplicity.
- While Amazon EKS was considered, Vanguard opted for ECS due to its simplicity and single-tenant nature, reducing the risk of one application impacting another.
- The decision to use ECS or EKS is periodically reevaluated, and Vanguard also explores the use of AWS Lambda for specific capabilities.

### Messaging

- Vanguard chose Apache Kafka as the messaging platform, leveraging its scalability, performance, and additional message protocols for the trading platform's needs.
- Kafka was deployed in a multi-region architecture, aligning with Vanguard's resiliency goals.
- Other options like Amazon Kinesis and Amazon EventBridge were considered, but Kafka was chosen for its additional capabilities.

## Benefits and Outcomes

### Customer Satisfaction

- Vanguard rethought the client experiences and challenged existing rules and capabilities during the modernization process.
- The modernized platform has received external recognition, including the Web Wealth Management Innovation Award from Celent.
- Internal measures show meaningful increases in client satisfaction, correlating with the progress of modernization.

### Agility and Time-to-Market

- The adoption of product team structures, DevSecOps practices, and modern cloud technologies has significantly improved Vanguard's ability to deliver value rapidly.
- New capabilities like mutual fund trading, dollar-based trading, and automated investment in ETFs were delivered at an accelerated pace.
- Completely new offerings, such as the Cash Plus high-yield cash account, were brought to market in less than 12 months, involving over 80 teams.

### Resiliency and Productivity

- Vanguard has seen a 70% decrease in major incidents while experiencing a 5x improvement in software deployments.
- This was achieved through the use of modern technologies, adoption of resiliency best practices, robust CI/CD pipelines, and an ownership mindset of product teams.

## Reflections and Next Steps

- Vanguard encourages thinking big and fully modernizing stacks to unlock the full benefits of the cloud.
- Remaining flexible and being willing to reevaluate decisions and make pivots along the way is crucial in the rapidly changing cloud environment.
- Modernization is a marathon, not a sprint, especially for mission-critical applications. Incremental value delivery and risk management techniques like blue/green deployments and canary deployments are recommended.
- Future focus areas include increasing personalization in the trade journey, enhancing the client experience through generative AI, expanding the cash offer, and completing the internal crew experience.

Vanguard's mission is to take a stand for all investors, treat them fairly, and give them the best chance for investment success. The modernization effort on AWS aligns with this mission, enabling Vanguard to provide better investment outcomes for its clients.