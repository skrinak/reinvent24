# Summary of AWS re_Invent 2024 - Chaos engineering_ A proactive approach to system resilience (ARC326).txt

# AWS re:Invent 2024 - Chaos Engineering: A Proactive Approach to System Resilience

## Summary

### Introduction

- Chaos engineering is a discipline of experimentation where faults are intentionally injected into systems to gain confidence in their ability to recover from turbulent conditions.
- It helps verify assumptions and biases that engineers may have when designing and operating systems.
- Outages can be costly for businesses, and companies that practice recovery pay significantly less per hour of outage than those that do not.
- Chaos engineering helps teams continuously practice their recovery skills and discover new ones, preventing skill atrophy.

### Chaos Engineering at Amazon

- Amazon has been practicing chaos engineering since the early 2000s through a program called GameDays.
- GameDays involve intentionally injecting faults into systems to train operations teams to recover quickly.
- Today, chaos engineering is mandated for every feature launch and service through an Operational Readiness Review.

### Failure Mode Analysis

- Failure mode analysis is a critical part of chaos engineering, helping identify potential failure scenarios to test.
- Three categories of failure modes:
  1. Fault isolation boundaries: Defining the potential blast radius of a failure.
  2. Dependencies: Testing the impact of failures in third-party services, packages, and other dependencies.
  3. Bimodal behavior: Testing how a system operates under different conditions (e.g., cache hit vs. miss).

### Demo: Ad-hoc Experimentation

- Ad-hoc experimentation is a straightforward approach to uncover unknown issues in an application.
- The demo showcased injecting network latency to the cache layer of a sample application using the AWS Fault Injection Service (FIS).
- The experiment uncovered an assumption about the application's behavior when the cache is unavailable, leading to a code fix and improved resilience.

### Demo: GameDay

- GameDays are periodic processes to test runbooks, alarms, and the ability of on-call personnel to follow procedures during incidents.
- The demo simulated an Availability Zone (AZ) outage using the FIS AZ power interruption scenario.
- The experiment revealed a configuration issue where the application was hard-coded to connect to a specific AZ's DynamoDB endpoint, leading to a proposed fix.

### Continuous Experimentation

- Scheduled experiments: Running chaos experiments on a schedule using the FIS.
- Chaos pipeline: Integrating chaos experiments into a separate pipeline from the release pipeline.
- On-call rotation: Having a secondary on-call team periodically run GameDays to test runbooks and operations.

### BMW's Chaos Engineering Journey

- BMW shared their journey from pulling cables in on-premises data centers to running sophisticated chaos experiments in the AWS cloud.
- Key lessons learned:
  1. Cross-team collaboration and knowledge sharing boosted the chaos engineering initiative.
  2. Leadership buy-in is crucial for running chaos experiments in production.
  3. Psychological safety, where failure is seen as an opportunity to learn and improve, is essential.
- BMW plans to automate and scale chaos experiments, allowing service owners to choose and execute experiments through a portal.

## Conclusion

Chaos engineering is a powerful approach to proactively identify and address potential issues in systems, verify assumptions, and continuously improve resilience and recovery capabilities. By intentionally injecting faults and observing system behavior, teams can uncover unknown unknowns, practice recovery skills, and build confidence in their systems' ability to withstand turbulent conditions.

Human Resources