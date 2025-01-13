# Summary of AWS re_Invent 2024 - Scaling to new heights with Amazon Redshift multi-cluster architecture (ANT339).txt

Here is a comprehensive summary of the transcript, formatted in Markdown with appropriate headers and bullet points:

# AWS re:Invent 2024 - Scaling to new heights with Amazon Redshift multi-cluster architecture

## Overview

- The session covers multi-cluster architectures in Amazon Redshift and how they help solve problems around scale and resource contention.
- Reference architectures are provided to help apply multi-cluster patterns in unique ways.
- Behind-the-scenes look at what enables multi-cluster architectures in Redshift.
- GE Aerospace's journey of moving from on-premises to AWS and scaling with Redshift multi-cluster architecture.
- Demo showcasing the challenges with single-cluster architectures and the benefits of multi-cluster architectures.

## Multi-Cluster Architectures: Solving Scale and Resource Contention

### Single-Cluster Architecture Challenges

- Multiple workloads (ingestion, reporting, BI, data science) sharing the same compute resources.
- Resource contention and interference between workloads.
- A single bad query can impact the entire workload, causing performance degradation.
- Difficulty in cost allocation and chargeback for different workloads or tenants.

### Multi-Cluster Architecture Benefits

- Separate compute endpoints for different workloads or tenants.
- Ability to size compute resources based on unique workload requirements.
- Isolation of workloads, reducing resource contention and blast radius of bad queries.
- Easier cost allocation and chargeback based on tagged endpoints.
- Scalability by adding more compute endpoints without data movement.

### Reference Architectures

#### Hub-and-Spoke Architecture

- Central "hub" for data ingestion and writes.
- Multiple "spokes" for different consumer workloads (reporting, BI, data science).
- Consumers can access the same data without copies or movement.

#### Departmental Architecture

- Each department or organizational silo has its own compute endpoint.
- Data ownership and governance by individual departments.
- Ability to share data across departments while maintaining control.
- Unified view of data across departments for customer 360 analysis.

## Enabling Multi-Cluster Architectures

- Redshift's managed storage layer optimized for analytics.
- Massively parallel compute layer with provisioned or serverless options.
- Mix and match of serverless and provisioned compute based on workload needs.
- Intelligent auto-scaling of compute resources.
- Compute layers can span across AWS accounts and regions.
- Transactionally consistent data access across compute layers.

## GE Aerospace's Journey with Redshift Multi-Cluster Architecture

### Modern Demands and Challenges

- Increasing demand from users and new workloads.
- Wide and deep tables (flight reports) alongside traditional analytics.
- Shrinking latency windows for report generation.
- Scaling out beyond a single cluster to meet demands.

### Evolution of Redshift Architecture

- Initially, a conventional on-premises monolith (2014-2021).
- Moved to the cloud and split writers (data owners) and readers (data consumers) (Q1 2021 - Q4 2022).
- Introduced cloud scale-out pattern with line-of-business Redshift clusters (Q1 2024).
- Evolved to a cloud data ecosystem with a hub-and-spoke and mesh design.

### Key Learnings and Takeaways

- Don't just lift and shift; engage with customers and tweak the design.
- Analyze workloads deeply to identify hotspots and opportunities for dedicated compute.
- Monitor metrics that matter to customers (queue times, running/queued queries).
- Expose and assess cost metrics to encourage better code refactoring.
- Design the ecosystem to map to business functions and collaboration patterns.
- "Own your base, rent your spike" – provision cost-effective resources for predictable workloads, and use advanced technologies like concurrency scaling for unpredictable spikes.

### Looking Ahead

- Continued momentum in data sharing and collaboration across teams.
- Teams understanding their roles as data producers or consumers.
- Line-of-business clusters resetting the gravity of data systems.
- Integration with generative AI workloads through the Redshift and SageMaker Lakehouse.

## Demo: Multi-Cluster Architecture for a Retail Firm

### Challenges with a Single-Cluster Architecture

- Multiple business units (sales, finance, marketing, support) sharing a monolithic compute.
- Resource contention and queuing due to various ingestion and querying workloads.
- Impact of a single bad query on overall workload performance.
- Difficulty in cost allocation for different business units.

### Benefits of a Multi-Cluster Architecture

- Separate endpoints for each business unit, sized based on unique requirements.
- Isolated ingestion and querying workloads, reducing resource contention.
- Smaller blast radius of bad queries, impacting only the specific endpoint.
- Ability to scale up or down individual endpoints based on needs.
- Simplified cost allocation and chargeback using tags and Cost Explorer.

### Redshift-to-Redshift Data Sharing

- Sharing a common table (Customer 360) across multiple compute endpoints.
- Creating a datashare with insert privileges on the common table.
- Granting access to the datashare to other business units.
- Consuming endpoints creating local database instances pointing to the datashare.
- Concurrent loading into the shared table with transactional consistency.

### Centralized Data Governance with Lake Formation

- Publishing data tables to the Data Catalog (within the same or centralized account).
- Creating a catalog and attaching an IAM role with appropriate privileges.
- Granting table-level or column-level access to specific roles or users.
- Federated users can access shared data without additional setup.

## Best Practices and Steps for Multi-Cluster Architectures

### Best Practices

- Create separate endpoints for each workload or group.
- Size endpoints based on unique workload requirements (or use AI-driven serverless scaling).
- Use Lake Formation for centralized data governance and permissioning management.

### Steps to Convert from Single-Cluster to Multi-Cluster

1. Perform a snapshot and restore for each workload or group.
2. Repoint consuming applications to the separate endpoints.
3. Drop unrelated schemas from the separate endpoints.
4. Share data from the ingestion endpoint (hub) to the consuming endpoints (spokes).

## Useful Resources

- [Blog 1 URL]
- [Blog 2 URL]
- [Blog 3 URL]