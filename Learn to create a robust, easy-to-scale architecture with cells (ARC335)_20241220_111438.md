# Summary of AWS re_Invent 2024 - Learn to create a robust, easy-to-scale architecture with cells (ARC335).txt

# AWS re:Invent 2024 - Learn to Create a Robust, Easy-to-Scale Architecture with Cells (ARC335)

## Introduction

This session covers the concept of cell-based architecture, its benefits, and how it can help organizations create a more robust and scalable infrastructure. The speakers, Mahmoud Ismail (AWS Specialist Solution Architect) and Paul Rapa (Senior Staff Software Engineer at Slack), discuss the challenges faced by customers, common failure scenarios, and how cell-based architecture can mitigate these issues.

## Typical Customer Journey and Challenges

1. **High-Impact Incidents**: Organizations often start their resilience journey after experiencing high-impact incidents, which raise concerns about the overall resiliency and efficiency of their architecture.

2. **Objectives**: The goal is to reduce the detection and restoration time and increase the mean time between failures (MTBF).

3. **Key Concepts**:
   - **Blast Radius**: Reducing the impact of failures and containing them within a defined boundary.
   - **Observability**: Detecting problems early and mitigating them to reduce mean time to detect (MTTD) and mean time to repair (MTTR).
   - **Deployments**: Reducing the impact of bad deployments and increasing MTBF.

## Common Failure Scenarios

1. **Gray Failures**: Different entities perceive the same issue differently, leading to discrepancies in detection and mitigation.
2. **Network Partial Impairment**: Issues in one Availability Zone (AZ) may be perceived as a regional issue due to cross-AZ load balancing.
3. **Poison Pill**: A client sending a request that triggers an application bug across the entire infrastructure.
4. **Bad Deployments**: Deploying code to the entire infrastructure at once, leading to a widespread impact and challenging rollbacks.

## Cell-Based Architecture

Cell-based architecture involves creating smaller boundaries or cells, with each cell containing a copy of the entire application stack. This approach helps reduce the blast radius and contain failures within a defined boundary.

### Cell Design Options

1. **Multi-AZ Cells**: Cells span across multiple AZs, with cross-AZ load balancing and the ability to leverage native AWS services for automatic recovery.
2. **Single-AZ Cells**: One cell per AZ, providing AZ affinity (traffic remains within an AZ) and more control over AZ failures and mitigation.
3. **Multiple Cells per AZ**: Further reducing the blast radius by creating multiple cells within a single AZ, enabling deterministic scaling and easier testing.

### Cell Observability

Introducing dimensionality (e.g., site, AZ ID, cell ID) in logs and metrics allows for more granular insights into cell performance. Cell observability involves making the observability stack cell-aware, enabling individual cell insights and tracking cell performance independently.

### Deployments

Cell-based architecture introduces the concept of a single unit of deployment, where the entire cell serves as the deployment unit. Deployments can be done in a staggered approach, starting with a single cell and gradually rolling out to the rest of the infrastructure.

### Failover and Mitigation

Services like AWS Route 53 Application Recovery Controller's Zonal Shift can be used to specify an AZ ID and resource ID, effectively taking an impaired AZ out of service and mitigating customer impact.

## Slack's Journey to Cell-Based Architecture

Paul Rapa shared Slack's journey to cell-based architecture, focusing on their egress platform. He discussed the evolution of their architecture, the migration process, the benefits of cell-based architecture, and the challenges they encountered along the way.

### Key Takeaways

1. **Gradual Evolution**: Slack's journey to cell-based architecture took approximately four years, with each evolution solving specific business and technical challenges.
2. **Solving Business Issues**: Each architectural change aimed to solve specific business issues, such as scaling concerns, blast radius reduction, targeted deployments, and AZ evacuation capabilities.
3. **Fit for Workloads**: Cell-based architecture may not be a perfect fit for all workloads. Slack's egress platform, being stateless, was well-suited for an AZ-based architecture.

## Conclusion

Cell-based architecture provides a way to reduce the blast radius, improve observability, and enable more controlled deployments. By creating smaller boundaries and duplicating application stacks within cells, organizations can contain failures, detect issues early, and mitigate customer impact more effectively. However, implementing cell-based architecture requires careful consideration of workload characteristics and may involve gradual evolution over time.