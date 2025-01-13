# Summary of AWS re_Invent 2024 - Building resilient applications on AWS with Capital One (ARC334).txt

# Summary

## AWS re:Invent 2024 - Building Resilient Applications on AWS with Capital One (ARC334)

### Main Points and Key Insights

#### Guiding Principles

- "Everything fails, all the time." - Werner Vogels, AWS CTO
- Focus on fast detection and response to failures, as you cannot prevent them entirely.

#### Fault Isolation

- Implement physical and logical boundaries in your architecture to isolate failures.
- Use multiple AWS accounts, Availability Zones, and the cellular architecture pattern.
- Smaller fault boundaries lead to smaller blast radiuses when failures occur.

#### Observability

- Observability is crucial for effective resilience and often neglected.
- Implement fine-grained observability aligned with your fault boundaries.
- Use dimensions and granular metrics to detect when customers experience issues.
- Implement composite alarms for overall application health monitoring.
- Conduct regular, proactive operational metrics reviews.

#### Recovery

- Prioritize static stability, where application operations continue despite failures.
- Implement smart retry logic with exponential backoff and jitter.
- Leverage routing around failures through health checks and services like AWS ARC.
- Align recovery actions with deployment processes for consistency.
- Test failure scenarios using AWS Fault Injection Simulator.

#### Capital One's Approach

- Resilience is critical in the financial services sector for customer trust.
- Capital One uses cell-based architectures for increased resilience.
- The authorization platform uses zonal independence cells for low latency.
- The core banking platform uses regional cells for tenant isolation and dynamic tenancy support.
- Deep health checks, fault isolation, and preventing retry storms are key benefits.

### Important Conclusions

- Resilience requires a comprehensive approach, including fault isolation, observability, and recovery mechanisms.
- Align your observability, fault boundaries, and recovery actions for a cohesive resilience strategy.
- Continuously improve and understand your application's requirements and business workflows.
- Implement resilience patterns like cell-based architectures for increased fault isolation and recovery capabilities.
- Leverage AWS services and best practices to build highly resilient, mission-critical applications.