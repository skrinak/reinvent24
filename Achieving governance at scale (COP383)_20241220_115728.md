# Summary of AWS re_Invent 2024 - Achieving governance at scale (COP383).txt

# Summary

## AWS Cloud Governance: Achieving Governance at Scale

### 1. Introduction to Cloud Governance
- Definition: Rules, processes, and reports to implement best practices according to governance and customer's business objectives
- Use cases: Regulation, Operations, and Management
- Governance services operate at massive scale (e.g., IAM handles over 1 billion API calls per second)

### 2. Core Elements of Governance
#### Multi-Account Structure
- Use multiple AWS accounts as isolated boundaries for different workloads, environments, and teams
- Organize accounts into Organizational Units (OUs) with a logical structure (e.g., Security, Infrastructure, Sandbox, Workloads)
- Apply policies and controls at the OU level, inheriting down to member accounts
- Recommended: Single production Organization, separate test Organization

#### Access Management
- Use AWS IAM Identity Center for centralized access management across accounts and applications
- Integrate with existing identity sources (e.g., Okta, JumpCloud)
- New Root Access Management feature for centralized root user management across accounts

#### Visibility and Monitoring
- Centralize logging with AWS CloudTrail and integrate with AWS Organizations
- Use AWS Security Hub for aggregated security findings and compliance checks
- Implement AWS GuardDuty for threat detection across accounts

#### Controls
- Service Control Policies (SCPs) to restrict actions and API calls across accounts
- New Resource Control Policies (RCPs) to enforce consistent resource access controls
- New Declarative Policies to manage service configurations at scale (e.g., EC2 settings)
- AWS Config for resource configuration management and compliance rules

#### Inventory Management
- AWS Resource Explorer for simplified resource inventory across accounts
- AWS Config for detailed resource configurations, relationships, and history
- Use Config APIs and SQL queries for advanced inventory analysis

#### Cost Management
- Gain visibility into costs with Cost Explorer, Cost and Usage Reports, and QuickSight dashboards
- Optimize costs with AWS Compute Optimizer, AWS Storage Lens, and AWS Cost Optimization Hub
- Implement preventative controls for high-cost actions using SCPs and RCPs

### 3. Customer Story: Workday's Governance Journey
- Evolved from a single AWS Organization to multiple Organizations with replica environments
- Implemented centralized logging, security monitoring, and change management processes
- Leveraged AWS Control Tower, Account Factory, and AWS Identity Center for new dynamic account provisioning
- Shared practical tips on CloudTrail, AWS Config, AWS Organizations, SCPs, Security Hub, GuardDuty, and more

### Key Takeaways
- Establish a solid multi-account structure with logical separation of environments
- Implement centralized access management, visibility, monitoring, and controls
- Leverage AWS governance services (Organizations, IAM, CloudTrail, Config, Security Hub, GuardDuty) at scale
- Adopt new capabilities like RCPs, Declarative Policies, and Root Access Management
- Continuously review and optimize resource inventory and costs
- Learn from customer experiences and best practices for governance at scale