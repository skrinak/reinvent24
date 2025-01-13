# Summary of AWS re_Invent 2024 - Best practices for creating multi-Region architectures on AWS (ARC323).txt

# Summary: Best Practices for Creating Multi-Region Architectures on AWS

## Introduction

- The session covers best practices for creating multi-region architectures on AWS, with a focus on failover strategies.
- It discusses the fundamentals of multi-region architectures, organizational failover strategies, determining when to failover, and recovery best practices.
- The session also includes a case study from Samsung Electronics on their multi-region journey.

## AWS Multi-Region Fundamentals

### 1. Understand the Requirements

- Define and bound your recovery time objectives (RTO) to set appropriate expectations and ensure your architecture can recover within that time.
- Measure and track recovery times accurately, considering the entire process from problem detection to complete recovery.
- Use metrics like Mean Time to Detection (MTTD), Mean Time to Recovery (MTTR), and Mean Time Between Failures (MTBF) to improve availability.

### 2. Understand the Data

- Consider data complexity, replication mechanisms, consistency levels, and acceptable data loss when designing multi-region architectures.
- Ensure your recovery mechanisms align with your recovery point objective (RPO) and RTO.

### 3. Understand Dependencies

- Ensure regions can operate independently without dependencies on other regions.
- Map out critical user stories and dependencies to prioritize architectural changes.
- Recovery actions should be taken from the recovery region without relying on the impaired workload.

### 4. Operational Readiness

- Test failover processes in a controlled fashion to identify issues and areas for improvement.
- Improve observability and monitoring for a 360-degree view of application health.
- Use differential observability to monitor from multiple viewpoints (application, user experience, synthetic monitoring).

## Organizational Failover Strategies

- **Component-Level Failover**: Failing over individual components to a different region (not recommended due to latency, complexity, and reliability issues).
- **Application Failover**: Failing over all components of an application together (reduces complexity but can still lead to varying performance behavior).
- **Dependency Graph Failover**: Failing over connected applications that support a specific user story together (recommended but can be complex to manage dependencies).
- **Portfolio Failover**: Failing over all applications in your portfolio simultaneously (simple but requires significant investment).

## Determining When to Failover

- Create a failover decision tree with clear, unambiguous metrics and thresholds for initiating failover.
- Integrate the decision tree with your overall operational continuity strategies and involve cross-functional stakeholders.
- Plan for scenarios with incomplete information, such as unavailable decision-makers, missing metrics, or ongoing AWS service events.
- Work backward from your bounded recovery time objective to determine when to initiate failover.

## Recovery Best Practices

- Clearly outline disaster declaration procedures, communication protocols, and runbook steps in advance.
- Ensure necessary credentials are available in both primary and secondary regions.
- Regularly review and update credentials as part of testing and planning.

## Samsung Electronics' Multi-Region Journey

- Samsung Account is a core service connecting 1.8 billion users across various Samsung devices and services globally.
- Initially deployed in two regions (EU and US), Samsung added an AP region to distribute traffic load and mitigate the risk of regional impairments.
- Implemented an Active-Active architecture across three regions, with consistent service configurations and data synchronization using Aurora DB, DynamoDB, and self-developed solutions.
- Evaluated traffic routing control methods (Global Load Balancer vs. DNS-based) and chose DNS-based for cost and operational simplicity.
- Leveraged CloudFront's Edge Locations and Route 53's geolocation routing to achieve geo-latency routing and predictable traffic distribution across regions.
- Implemented comprehensive monitoring and observability systems for end-to-end error detection and faster decision-making.
- Conducted functional and stress testing, validating the global disaster recovery architecture in production environments.
- Achieved swift recovery from regional issues and reduced Mean Time to Repair (MTTR) and Mean Time to Detection (MTTD).