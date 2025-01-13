# Summary of AWS re_Invent 2024 - Architectural best practices throughout the lifecycle (ARC206).txt

# AWS re:Invent 2024 - Architectural Best Practices Throughout the Lifecycle

## Summary

### Introduction

- This is a level 200 session on foundational guidance for long-term success in cloud optimization.
- The speakers are Bradley (cloud optimization team at AWS), Charles (AWS Solutions Architect), and Geoffroy Renaud (Cloud Principal Architect at Accor).

### What is Cloud Optimization?

- Cloud optimization is the act of designing, building, and running workloads to bring the best possible value for your business objectives.
- It involves making trade-offs between factors like cost, reliability, and time to market.
- It applies to technology, people, and processes.
- AWS offers the Cloud Optimization Framework and the Well-Architected Framework as guidance.

### The Journey of Cloud Optimization

- Best practices change over time, and workloads naturally evolve, so continuous optimization is necessary.
- The journey is an incremental process of building maturity across phases:
  - Exploration: Learning cloud concepts, experimenting with small projects, considering governance.
  - Foundational: Developing a cloud strategy, laying foundational infrastructure.
  - Intermediate: Actively designing and architecting on the cloud, implementing governance policies.
  - Advanced: Building, deploying, implementing CI/CD pipelines, conducting regular architecture reviews.
  - Autonomous: Continuous optimization with mature processes and innovation.
- Knowledge sharing across teams is crucial as organizations grow and complexities increase.
- A lifecycle approach is recommended, with phases like Learn, Measure, Identify, Prioritize, and Improve.
- Automated discovery (tools) and conversational discovery (stakeholder discussions) are both important.

### Tools for Cloud Optimization

- **Well-Architected Tool**: Helps with architecture guidance, best practices, measuring improvement, and collaboration. Features include Lenses, Custom Lenses, Profiles, Review Templates, and Milestones.
- **Trusted Advisor**: Provides real-time guidance on cost optimization, security, performance, resilience, and service limits.
- **Service Screener**: An open-source tool that runs automated checks and provides AWS recommendations based on the Well-Architected Framework.
- **AWS Health**: Provides real-time information about AWS service health, account-specific events, and scheduled changes.

### Accor's Cloud Optimization Journey

- Accor is a global leader in the hospitality industry, with over 5,700 hotels and 10,000 restaurants and bars.
- The COVID-19 pandemic disrupted the industry and exposed the necessity for agility, adaptability, and scalability.
- Accor started with a proof of concept, discovered the Well-Architected Framework, and established a Cloud Center of Excellence (Welcome Cloud).
- They moved to a cloud-first strategy, application portfolio management, and a massive lift-and-shift migration to the cloud.
- Architectural Decision Records (ADRs) were used to log decisions, align teams, and manage patterns at scale.
- Knowledge sharing, education, and coaching were emphasized through training, certifications, and sandboxes.
- A feedback loop was established to collect data from various sources, analyze it, and prioritize the roadmap.
- Standardization and automation were achieved through templates, blueprints, technical architecture documents, guardrails, and self-service products.
- Future focus areas include maturing the Cloud Business Office (CBO), finding the right balance between governance and autonomy, and enabling self-service for the Well-Architected Framework.

### Key Takeaways

- Cloud optimization is a continuous journey involving technology, people, and processes.
- Incremental improvement across phases and knowledge sharing are crucial.
- Utilize AWS tools like the Well-Architected Tool, Trusted Advisor, Service Screener, and AWS Health.
- Establish a feedback loop for data collection, analysis, and prioritization.
- Standardize and automate through templates, blueprints, and self-service products.
- Balance governance and autonomy, enabling self-service for teams.