# Summary of AWS re_Invent 2024 - SaaS storage strategies_ Scaling, securing & tuning multi-tenant data (SAS306).txt

# AWS re:Invent 2024 - SaaS Storage Strategies: Scaling, Securing & Tuning Multi-Tenant Data

## Summary

### Introduction

- The session covers best practices, patterns, and guidance for implementing, scaling, securing, and optimizing multi-tenant data and storage in SaaS applications built on AWS.
- It discusses the key factors for a great SaaS storage architecture: security, scalability, and efficiency.

### Multi-Tenancy Deployment Models

- Silo model: Dedicated databases or infrastructure for each tenant, providing natural security boundaries but inefficient resource utilization.
- Pool model: Multiple tenants share common resources, efficient but more complex architecture and isolation challenges.
- Bridge model: A mix of silo and pool models.

### Access Patterns and Isolation

- AWS IAM authentication with temporary credentials works well for siloed environments but has limits in pooled environments.
- Secrets Manager can be used for credential management in pooled environments.
- Token Vending Machine (TVM) pattern can provide scoped credentials for multi-tenant environments.
- Isolation context (IAM policies, policy engines) is needed in addition to deployment models for proper data isolation.

### Scaling Strategies

#### Vertical Scaling

- Adding more resources (CPU, memory, storage) to a single database instance.
- Efficient but has finite limits.

#### Connection Management

- RDS Proxy can reuse connections across multiple sessions, enabling more connections to the database.
- RDS Data API provides an HTTP API interface to Aurora, managing connections and allowing session variables.

#### Horizontal Scaling

- Read Replicas: Offload read traffic to replicas, up to 15 for Aurora.
- Sharding: Manually partition data across multiple database instances (shards).
- Amazon Aurora Serverless v2: Managed sharding solution for PostgreSQL.

### Efficiency and Performance

- Query optimization techniques (micro-batching, pre-aggregation).
- Table partitioning using the tenant ID as the partition key.
- Collocating tenant data on the same set of disks or storage instances.

### Backup and Restore

- Native backup tools operate at the disk layer, backing up all tenants together in shared environments.
- Separation of tenant data can be done during backup (performance impact) or restore (operational complexity).
- Backup separation benefits: compliance, data deletion, off-boarding tenants.

### Fairness and Tenant Isolation

- Rate limiting upstream in the application (e.g., API Gateway usage plans).
- Tenant migration between storage instances for noisy neighbors or tier changes.

### Data Modeling

- Associate tenant ID with every data item for isolation, backups, and migration.
- Aim for efficiency by collocating data and using secondary indexes or views.
- Consider common access patterns and duplicating data for better query performance.
- Plan for upstream request limiting in the application design.

### Key Takeaways

- Efficiency is crucial for SaaS scalability and profitability.
- Stretch storage architecture as far as possible before implementing complex scaling approaches like sharding.
- Collocate tenant data using the tenant ID for operational benefits.
- Implement fairness mechanisms like rate limiting and tenant migration.
- Provide feedback and share challenges through surveys and GitHub repositories.

## Conclusion

The session provided a comprehensive overview of strategies, patterns, and best practices for scaling, securing, and optimizing multi-tenant data and storage in SaaS applications built on AWS. It covered deployment models, access patterns, isolation, scaling techniques, efficiency, backups, fairness, and data modeling considerations specific to SaaS environments.