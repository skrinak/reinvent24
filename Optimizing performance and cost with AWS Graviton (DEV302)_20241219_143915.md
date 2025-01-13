# Summary of AWS re_Invent 2024 - Optimizing performance and cost with AWS Graviton (DEV302).txt

Here is a comprehensive summary of the transcript in Markdown format:

# AWS re:Invent 2024 - Optimizing Performance and Cost with AWS Graviton (DEV302)

## Introduction

- The speaker, Liz Fong-Jones, shares Honeycomb's experience in migrating to AWS Graviton while maintaining performance and reducing costs.
- Honeycomb is a software company that enables developers to gain insights into their systems using big data.
- Their goal is to provide fast query responses (99.5% of queries within 10 seconds) and easy data ingestion.

## Background on ARM and Graviton

- In the past, software was developed for specific hardware architectures (mainframes, x86, 68k).
- The mobile revolution brought ARM32 chips for power efficiency.
- ARM64 and RISC-V processors now compete with x86 for cloud deployments.
- Open source software and containers enabled easier architecture portability.
- ARM is more efficient because it has a simpler instruction set and can use smaller transistors.

## Honeycomb's Graviton Journey

- In 2020, Honeycomb evaluated Graviton2 and found 20% better performance and 10% lower costs.
- They conducted A/B testing, measuring latency, throughput, and cost.
- The Go programming language made porting the code easier.
- Graviton2 instances could run at higher utilization without latency degradation, providing additional cost savings.

## Rolling Out Graviton

- Honeycomb started with a small deployment in their "Dogfood" staging environment.
- They chose a stateless data ingest service for the initial rollout, as it was easier to roll back if needed.
- Graviton3 and Graviton4 migrations were relatively straightforward, just changing instance types.
- They abandoned using Spot instances due to capacity constraints for newer Graviton generations.

## Stateful Workloads

- For stateful workloads like Kafka and indexing, Honeycomb had to overcome some challenges.
- They optimized Kafka's S3 interactions by using Graviton-optimized libraries.
- For indexing, they migrated from I3 to M6gd instances, gaining more cores and performance.
- They used AWS Lambda with Graviton for parallel processing of older data on S3.

## Results and Conclusions

- Honeycomb is now 100% on Graviton for both serverful and serverless (Lambda) workloads.
- They achieved 2.2x better price/performance compared to five years ago.
- Their AWS bill only increased by 13x while scaling ingestion by 20x, resulting in 1.6x cost efficiency per trace.
- Reliability remained solid, with stable P99 latencies.
- Liz recommends setting goals, experimenting, and using data to make the business case for completing the migration.

Overall, Honeycomb's migration to AWS Graviton allowed them to optimize performance and costs while maintaining reliability and scalability.