# Summary of AWS re_Invent 2024 - Mastering resilience at every layer of the cake (ARC327).txt

# AWS re:Invent 2024 - Mastering Resilience at Every Layer of the Cake (ARC327)

## Summary

### Introduction

- The session focuses on advanced resilience characteristics, features, and patterns in AWS.
- It covers dependencies and considerations for building resilient applications.
- The presentation includes customer case studies, demos, and insights from AWS and customer experiences.

### Key Points

1. **Resilience Layers**
   - The bottom layer is the platform (EC2, S3, etc.) where cloud builders operate.
   - The next layer is the infrastructure (operating systems, databases, etc.).
   - The top layer is where applications run, which is the ultimate goal.

2. **AWS Service Architecture**
   - Zonal services (e.g., EC2, EBS) are built and fail independently in each Availability Zone (AZ).
   - Regional services (e.g., Lambda) are built using zonal services and designed for resilience.
   - Global services have a control plane in a single region and a globally distributed data plane.

3. **Static Stability**
   - Maintaining the same pattern of work without changes, even in case of an AZ loss.
   - Over-provisioning resources across multiple AZs to continue operating without relying on the control plane.
   - AWS Lambda's architecture demonstrates static stability across three AZs.

4. **Resilience Testing**
   - Growing demand for resilience testing, from ad-hoc game days to continuous experimentation.
   - Fault Injection Service (FIS) and Scenario Library help customers test real-life scenarios.
   - Demo: Testing an AZ availability power interruption scenario using FIS.

5. **Resilience Culture**
   - Customers invest in building resilience culture programs, learning from AWS's practices.
   - The Resilience Lifecycle Framework outlines stages: set objectives, design & implement, evaluate & test, operate, and respond & learn.
   - Continuous Operational Excellence (COE) process encourages sharing and learning from failures.

6. **Customer Case Studies**
   - Vanguard: Built a resiliency testing suite, reducing recovery times and increasing availability.
   - United Airlines: Implemented an automated failover solution, "Rapid Recovery," reducing recovery time by 80%.

### Important Conclusions

- Set clear objectives for resilience based on business requirements and cost considerations.
- Leverage AWS services and tools (FIS, Scenario Library, Resilience Hub) for resilience testing and chaos engineering.
- Build a resilience culture by embracing failure learning, sharing COEs, and implementing resilience practices.
- Automate recovery processes and leverage AWS services (Application Recovery Controller, Autoscaling, etc.) for faster failover.
- Continuously evaluate and improve resilience through testing, monitoring, and iterative lifecycle stages.

The session provided valuable insights, best practices, and real-world examples for mastering resilience at every layer of cloud applications using AWS services and a resilience-focused mindset.