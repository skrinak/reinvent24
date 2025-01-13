# Summary of AWS re_Invent 2024 - Anatomy of an AWS Region (ARC204).txt

# Summary of "AWS re:Invent 2024 - Anatomy of an AWS Region (ARC204)"

## Introduction
- This session covers how AWS builds new regions and the lessons that can be applied to architecting resilient systems on AWS.
- It covers the AWS Global Infrastructure, building for resiliency, the evolution of region builds at AWS, and the mechanisms and tooling used in modern region builds.

## AWS Global Infrastructure
- AWS has 34 geographic regions with 108 Availability Zones (AZs), and plans for 6 new regions and 18 additional AZs.
- Regions are divided into partitions (e.g., AWS commercial, AWS GovCloud, AWS China).
- Regions consist of multiple AZs, which are separate data centers located far apart to prevent correlated failures.
- AZs within a region are interconnected with high-bandwidth fiber connections and connected to the AWS Global Backbone Network.

## Building for Resiliency
- AWS designs its infrastructure with resiliency in mind, following a shared responsibility model with customers.
- Customers should understand the scope of services (zonal or regional) and plan operational responses accordingly.
- Testing through game days is recommended to validate recovery procedures.

## Evolution of Region Builds at AWS
- Early region builds used a "bootstrap ninja" approach, with engineers manually configuring the initial infrastructure on-site.
- This approach was not scalable and could not handle dependencies between services running on AWS infrastructure.
- Modern region builds use an existing AWS region (bootstrap region) to provision the new region's infrastructure in parallel with physical data center construction.
- Services are brought up in dependency waves, with each service continuously checking the health of its dependencies before activating.

## Region Build Mechanisms and Tooling
- AWS uses several mechanisms to facilitate collaboration and continuous improvement during region builds:
  - Everything is a ticket (auditable, searchable, discoverable)
  - Operational Readiness Reviews (ORRs) to review operational metrics, alarms, and failure modes
  - Correction of Error (COE) documents to capture lessons learned from incidents (non-punitive)
- Tooling includes project management tools for tracking dependencies and schedules, internal documentation, and centralized programs to solve common issues.
- Leadership engagement and a healthy escalation culture are crucial for resolving risks and delays efficiently.

## Key Takeaways
- Design for resiliency from the ground up, using fault isolation techniques like separate accounts.
- Evaluate when to centralize or distribute problems based on incentives for optimization.
- Capture everything (code, configuration, documentation) in source control for auditability and searchability.
- Measure problems and solutions with data to drive prioritization and validate improvements.
- Engage leadership and foster a culture of healthy escalation to resolve issues quickly.