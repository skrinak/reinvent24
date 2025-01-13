# Summary of AWS re_Invent 2024 - How Netflix handles sudden load spikes in the cloud (NFX301).txt

# Summary

## Introduction

- Netflix handles massive traffic spikes due to new content releases, live events, and other factors, making load management crucial for maintaining a seamless viewing experience.
- The session covers how Netflix architects solutions on AWS to manage load spikes, leveraging features like auto-scaling, CloudWatch high-resolution metrics, and on-demand compute.

## Predicting and Proactively Scaling (Rob)

- Netflix runs an active-active architecture across four AWS regions, allowing for region failover to redirect traffic during issues or planned tests.
- For anticipated load spikes (e.g., new content launches), Netflix proactively scales services ahead of time using failover tooling and mapping expected load to required capacity.
- Traffic shaping distributes load across regions for geographically-concentrated launches, reducing risk and allowing auto-scaling to work effectively.

## Reactive Auto-Scaling Enhancements (Ryan)

- Netflix optimized auto-scaling policies to react faster to sudden load spikes:
  - Scaling based on requests per second (RPS) instead of CPU utilization
  - Using RPS "hammer" step scaling policies to provision the right capacity in one step
  - Incorporating higher resolution (5-second) CloudWatch metrics for faster load detection
  - Optimizing application and system startup times

## Maintaining Availability During Spikes (Joey)

- Netflix uses prioritized load shedding to maintain availability during load spikes:
  - Services are tagged based on criticality, business domain, and lifecycle
  - Lower-priority requests are dropped first within the "success buffer" (up to ~60% CPU utilization)
  - Higher-priority requests are dropped in the "failure buffer" (60-90% CPU utilization)
  - Prioritization is based on request context (URL, headers) and client device priority
- Latency-based load shedding protects I/O-bound services by treating high latency as high utilization.
- Cross-region request shifting retries throttled requests in another region, downgrading priority to prevent cascading failures.

## Testing and Validation (Rob)

- Netflix employs a "resilience testing pyramid" to validate load spike handling at different levels:
  - Synthetic load testing against individual services
  - Production load testing using real traffic ("auto-scaling squeeze tests")
  - Region scale testing by redirecting global traffic to a single region
  - Region load testing using synthetic user flows against the front door

## Key Takeaways

- Combine proactive (pre-scaling) and reactive (auto-scaling, load shedding) mechanisms for load spike handling.
- Prioritize high-value traffic and shed lower-priority requests to maintain availability.
- Fail requests quickly when in the "failure buffer" to prevent congestive failure.
- Continuously test resilience mechanisms in production environments.