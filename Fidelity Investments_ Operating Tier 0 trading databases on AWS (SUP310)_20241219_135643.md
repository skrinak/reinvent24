# Summary of AWS re_Invent 2024 - Fidelity Investments_ Operating Tier 0 trading databases on AWS (SUP310).txt

Here is a comprehensive summary of the transcript, formatted in Markdown with appropriate headers and bullet points:

# AWS re:Invent 2024 - Fidelity Investments: Operating Tier 0 Trading Databases on AWS

## Introduction

- Presentation by Stephen Clarke (AWS), Manoj Kumar (Fidelity Investments), and Shataksh Sharma (AWS)
- Discusses how Fidelity operates their mission-critical, tier 0 trading databases on AWS
- Covers challenges, resiliency patterns, and the use of AWS Incident Detection & Response (IDR) service

## Challenges in Running Mission-Critical Workloads

- Enterprises face an average of 29 unplanned outages per year, costing $13.5 million annually
- Major problems:
  - Delayed problem detection (relying on end-user feedback)
  - Difficulty identifying the root cause (application, infrastructure, third-party service)
  - Inability to solve critical problems fast enough

## Resiliency Patterns at Fidelity

### Tier Rating and Recovery Objectives

- Tier rating is based on Recovery Time Objective (RTO), Recovery Point Objective (RPO), and availability
- Tier 0 workloads have the lowest RTO and RPO, requiring near-zero data loss

### Active-Active Pattern

- Two-region deployment with bidirectional replication
- Meets most RTO and RPO needs, but potential for data loss due to asynchronous replication

### Global Active-Active Pattern

- Minimum three-node deployment across regions
- Shared-nothing infrastructure with synchronous replication and strong consistency
- Guarantees data protection and zero RPO
- Provides horizontal scalability in real-time

## Failure Mode and Effects Analysis (FMEA)

- Proactive approach to test failure points by manually injecting failures
- Uses AWS Fault Injection Service and Chaos Buffet framework
- Helps understand the impact of failures on the database, application, and recovery processes

## AWS Incident Detection & Response (IDR)

### Motivation for Using IDR

- Challenges in engaging AWS support and identifying the right subject matter experts during incidents
- Need for faster triage and resolution, especially for mission-critical workloads

### IDR Benefits

- Improved observability by defining and correlating metrics and alarms
- Faster resolution with predefined runbooks and single-threaded ownership
- Early warning signals for AWS events that may impact workloads
- Reduced potential for failure through post-incident reviews and resilience evaluations

### IDR Integration and Workflow

- Ingests alarms from CloudWatch, third-party APMs, and other sources
- Automatically opens critical cases and executes response plans
- Provides early notifications and engages AWS experts as needed
- Conducts post-incident reviews and resilience evaluations

### IDR Impact at Fidelity

- Reduced time to engage AWS support from 70 minutes to 1 minute
- Reduced total triage time from 9 hours to 1 hour 10 minutes
- Enabled faster resolution and assessment for early trading hours

## Conclusion

- Fidelity and AWS continue to collaborate on optimizing incident management processes
- IDR helps Fidelity operate their tier 0 trading databases on AWS with improved resiliency and faster incident response