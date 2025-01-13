# Summary of AWS re_Invent 2024 - Scaling Prime Video for peak NFL streaming on AWS (ARC311).txt

# AWS re:Invent 2024 - Scaling Prime Video for peak NFL streaming on AWS (ARC311)

## Summary

This session covered the strategies and techniques employed by Prime Video to scale their infrastructure on AWS to handle the massive demand during peak NFL streaming events, particularly Thursday Night Football. The key points and insights are:

### Multi-Region Architecture

- **Challenges:** Handling appointment viewing with sharp traffic spikes, forecasting demand accurately, and ensuring high availability.
- **Solution:** Migrating key components to a multi-region active-active architecture for global reliability and low latency.
- **Key Components:**
  - Live signal ingestion and delivery stack (multi-region from the start)
  - Playback stack (multi-region, edge routing layer)
  - Application storefront (multi-region, globalized services)
- **Benefits:** Enhanced resilience, seamless failover, lower latency, and high availability.

### Elastic Scaling

- **Challenges:** Highly variable peak-to-mean traffic ratio, spiky traffic patterns, and coordination effort across hundreds of distributed teams.
- **Solution:** Building a centralized autoscaling product to automate capacity provisioning and scaling.
- **Key Components:**
  - Central forecasting system
  - Main central hub/gateway
  - Transformation library embedded in service teams
- **Benefits:** Reduced days at peak scale, improved resource utilization, 30% infrastructure cost savings (pilot), and automated scaling.

### Well-Architected Framework

- Prime Video adopted the AWS Well-Architected Framework, focusing on the Reliability and Cost Optimization pillars.
- **Reliability Principles:** Automatic recovery, testing recovery procedures, horizontal scaling, stopping guessing capacity, and automation.
- **Multi-Region Best Practices:** Understanding consistency/replication options, asynchronous replication, handling active-active conflicts, and differential observability.
- **Key Fundamentals:** Understanding requirements (RTO/RPO), data consistency (CAP theorem), dependencies, and operational readiness.

## Key Takeaways

- Operational resilience: Supporting growth for millions of users during peak events.
- Dynamic scaling: Handling highly variable peak-to-mean traffic ratios.
- Cost optimization: 20% reduction in operational costs, 30% savings in the pilot.
- Carbon footprint reduction: 43% reduction by optimizing EC2 instances and adopting Graviton.
- Focus on one pillar at a time (e.g., Reliability first, then Cost Optimization).
- Embrace failure as a natural occurrence and build resilient systems.

The session provided a comprehensive overview of Prime Video's journey to scale their infrastructure on AWS, leveraging multi-region architectures and elastic scaling strategies to deliver a seamless streaming experience for millions of viewers during peak NFL events.