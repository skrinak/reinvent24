# Summary of AWS re_Invent 2024 - Saving lives with serverless_ Modernizing transplant matching on AWS (IMP206).txt

# AWS re:Invent 2024 - Saving Lives with Serverless: Modernizing Transplant Matching on AWS (IMP206)

## Summary

### Introduction

- Madhu Bussa (AWS Solution Architect Leader) and David Wroe (NMDP Principal Architect) present NMDP's journey to modernize their donor-matching system using AWS cloud-native technologies.
- NMDP is a global nonprofit that helps save lives by brokering bone marrow transplants for patients with blood cancers and disorders.

### Why Modernization is Essential

- Modernization allows organizations to shift focus from maintaining legacy systems to driving innovation and increasing agility.
- It helps reduce costs, improve performance, and create personalized online experiences for better customer satisfaction.
- AWS recommends the "7 Rs" modernization pathways: Rehost, Rehost+, Relocate, Replatform, Refactor, Repurchase, and Retain.

### NMDP's Modernization Journey

1. **Refactoring to Open Source**
   - Migrated from proprietary technologies to the Hadoop open-source platform.
   - Achieved: Moved away from proprietary licensing.

2. **Rehosting to AWS Cloud**
   - Lifted and shifted the Hadoop workload to AWS.
   - Benefits: Reduced hardware costs, simplified infrastructure management, enabled blue-green deployments, and provided limitless capacity.
   - Challenges: Hadoop did not scale elastically, and cost reductions were not fully achieved.

3. **Refactoring to Serverless**
   - Broke down the application into microservices and moved to AWS Lambda.
   - Migrated databases to Aurora Serverless.
   - Benefits: Achieved elastic scaling, reduced total cost of ownership by almost $1 million per year, improved performance, and gained observability with CloudWatch and X-Ray.
   - Challenges: Cost management, free capacity effect, and continuous delivery testing.

### Key Lessons Learned

- Modernization is not just about technology; it includes the experience and lessons gained throughout the process.
- Each phase (lift and shift, refactoring, serverless) provided significant learnings to optimize systems and processes.
- There is no shortcut to innovation; it's a continuous journey of adapting and unlocking business value.

### Recommendations for Modern Applications

- Modular architecture with domain-driven design
- Serverless as much as possible
- Improved developer agility through automation and standardization
- Programmatic security guardrails
- Decoupled, purpose-built data management systems

### Next Steps for Modernization

- Leverage AWS managed container services (Fargate, ECS, EKS) or serverless technologies (AWS Lambda) based on your application needs.
- Be selective with the applications to modernize, prioritizing those that amplify business outcomes.
- Leverage serverless for operational models to reduce overhead costs.
- Engage AWS and its partners for their expertise in modernization journeys.

### Immediate Next Steps

- Attend recommended sessions at re:Invent featuring non-profit customer speakers.
- Get in touch with your AWS account manager for further guidance.
- Learn more about NMDP, donate, volunteer, or advocate for their cause.
- Explore job opportunities at NMDP.