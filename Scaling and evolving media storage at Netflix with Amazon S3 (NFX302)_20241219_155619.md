# Summary of AWS re_Invent 2024 - Scaling and evolving media storage at Netflix with Amazon S3 (NFX302).txt

# Summary: Scaling and Evolving Media Storage at Netflix with Amazon S3

## Introduction

- Esha and Ankur from Netflix's content infrastructure and solutions team discussed Netflix's media storage, its evolution, scale, and data lifecycle management solution.
- They covered the Netflix studio ecosystem, the Content Drive platform, its architecture, design concepts, and statistics, as well as the data lifecycle management solution.

## Netflix Studio Ecosystem

- Netflix has pioneered the studio in the cloud, enabling artists to work globally on creating content.
- Media assets go through various stages and transformations during production and post-production.
- Netflix stores these assets as objects in Amazon S3, along with essential metadata.
- Artists and applications expect a file-folder interface to access and work with these assets seamlessly.

## Content Drive: Studio Metadata Management Platform

- Content Drive is a metadata abstraction layer on top of Amazon S3, providing a file-folder metadata abstraction.
- It enables rapid file operations, dynamic access control, data transfers, and rich file-folder notifications.
- Key features include:
  - File-folder interface for seamless access and operations (create, manage, copy, move, delete, download, share)
  - Dynamic access control based on projects, stages, assets, workflows, applications, or users
  - Collaboration and sharing capabilities across departments
  - Support for disparate media features and enhancements

### Architecture and Design

- Components: REST/GraphQL API layer, file service, access control, data transfer, persistence, event handling
- Core entities: CNodes (files, folders, workspaces, partitions, sequences, snapshots)
- Design concepts: Parent-child hierarchy, unique file path invariant, distributed transactions, normalized data locations, strong consistency, complex queries
- CNode lifecycle states: Created, available, checksum verified, soft deleted, recovered, archived, restored, purged
- Workspace types: User/personal, project/application-owned, team
- Authorization based on workspace type and access control lists

### Evolution and Hybrid Storage

- Content Drive will support hybrid storage in the context of Netflix's global studio, with files potentially located across cloud, vendor environments, and on-premises infrastructure.
- It will enable operations like uploading, backing up, verifying, and managing files across these locations.

### Statistics and Optimizations

- As of October 2024, Content Drive has 14.5 billion nodes, 848K workspaces, and creates 50 million new nodes per week.
- Daily active visits on Content Drive-backed UI pages range from 50K to 60K users across various production departments.
- Optimizations include distributed caching, follower reads, time-based user IDs for node ID generation, concurrent batch write support, and performance improvements through query optimizations.

## Data Lifecycle Management Solution

### Challenges and Requirements

- Explosive growth in content volume (doubling year-over-year) and associated storage/access costs
- Increasing volume of unused or "dark" data, leading to inefficiencies
- Requirements: Policy-based automation, security, real-time insights, object-level granularity, data integrity, secure deletion, auditing, easy retrieval, ad-hoc bulk movements

### Solution Architecture

- Components: Policy manager, Content Drive (storage metadata layer), storage lifecycle manager, S3 abstraction layer
- Policy manager translates business context into lifecycle requests
- Content Drive maintains separation between metadata and data, enabling efficient lifecycle operations
- Storage lifecycle manager orchestrates lifecycle operations (archive, restore, purge) asynchronously and in a distributed manner
- S3 abstraction layer interacts with S3 for object tagging and transitions

### Cost Optimization and Impact

- Short-term: Asset migration to Amazon S3 Glacier Instant Retrieval (20-30% cost reduction)
- Long-term: Policy-based storage lifecycle management (projected 70% cost savings)
- Intelligent retention rules and moving cold data to cost-effective storage tiers

### Statistics and Future Initiatives

- Archived 77 petabytes, temporarily restored 200 terabytes, purged 33 petabytes
- Future initiatives: Hybrid storage lifecycle management, intelligent tagging system, metadata tiering

## Conclusion

- Content Drive is a cloud-native solution for media asset management at Netflix, enabling content ingestion, metadata management, lifecycle policies, and access control.
- It achieves cost optimizations through intelligent utilization of S3 storage tiers, backed by fine-grain pattern analysis.
- More details can be found on the Netflix Tech Blog.