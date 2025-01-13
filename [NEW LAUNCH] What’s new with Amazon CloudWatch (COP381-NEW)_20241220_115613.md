# Summary of AWS re_Invent 2024 - [NEW LAUNCH] What’s new with Amazon CloudWatch (COP381-NEW).txt

# Summary

## Key Points and Insights

### What is Observability?
- Observability involves three key phases: detection (identifying what went wrong and where), investigation (understanding why it went wrong), and remediation (recovering from the issue).
- It is based on three pillars: metrics (measuring performance), logs (event streams), and traces (understanding component relationships).

### Observability Challenges
- Monitoring coverage is crucial to measure the behavior of all components in a system.
- Correlating data across different resources, metrics, and logs is difficult.
- Data silos and fragmentation make it hard to get a unified view.
- Identifying the root cause of issues in distributed systems is challenging.
- On-call incidents can be stressful, especially without proper context and guidance.

### New Amazon CloudWatch Features
1. **CloudWatch Database Insights**: Provides curated insights and a unified view for Amazon Aurora databases, tying SQL metrics to applications.
2. **CloudWatch Unified Navigation**: Enables seamless navigation across related telemetry and resources, revealing dependencies and providing inline views.
3. **OpenSearch Integration with CloudWatch Logs**: Allows enhanced querying and analytics on CloudWatch Logs data using OpenSearch capabilities.
4. **CloudWatch Span Analytics**: Provides complete visibility into application transactions at any scale, without sampling, through visual span analysis.
5. **Amazon Q Developer Ops Assistant**: An AI-powered assistant that investigates operational issues, provides hypotheses and observations, and guides towards root causes.

## Important Conclusions
- Monitoring coverage, data correlation, and unified analytics are crucial for effective observability.
- New CloudWatch features aim to address common observability challenges and accelerate issue detection, investigation, and remediation.
- CloudWatch Unified Navigation and Amazon Q Developer Ops Assistant can significantly reduce the time and effort required for investigations, especially during on-call incidents.
- By leveraging these new capabilities, teams can gain better visibility, context, and guidance, leading to faster resolution of operational issues and improved customer experience.