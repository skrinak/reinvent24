# Summary of AWS re_Invent 2024 - How Gousto reduces food waste and increases workforce productivity (MFG202).txt

Here is a comprehensive summary of the transcript, formatted in Markdown with appropriate headers and bullet points:

# AWS re:Invent 2024 - How Gousto Reduces Food Waste and Increases Workforce Productivity

## Introduction

- The session covers Gousto's journey in building data-driven operations using AWS services and partners to reduce food waste and increase workforce productivity.
- Gousto is a meal kit company that delivers boxes of fresh ingredients to customers in the UK.
- Their mission is to be the most loved way to eat dinner while enriching lives and protecting the planet.

## Challenges

- Gousto was experiencing significant downtime, costing them $30,000 per hour.
- They lacked visibility into the state of their operations and equipment, making it difficult to identify and resolve issues proactively.
- Gathering and preparing data for analysis was a time-consuming process, taking up to 80% of the effort.

## AWS Approach: Industrial Data Fabric

- AWS introduced the Industrial Data Fabric, an architecture that facilitates data flow from various systems through a common API.
- It enables manufacturers to ingest, store, contextualize, and act on data, regardless of the use case.
- The architecture involves AWS services like AWS IoT SiteWise, AWS IoT Core, and partners like HighByte.

## Gousto's Solution: FactoryOS

### Unified Namespace (UNS)

- Gousto used HighByte to connect to their automation data and AWS IoT Core to route the data to the cloud.
- This created a Unified Namespace (UNS), enabling access to raw data from various sources.

### Fault Detection and Repair

- They built a fault detector using AWS IoT Events, which triggered work orders in their maintenance system when equipment went down.
- This reduced the mean time to repair (MTTR) and enabled tracking of repair cycles.

### Data Lake and Analytics

- Gousto sent the data from the UNS to a data lake, enabling analytics, reporting, and model training.

### Predictive Maintenance

- They added sensors to monitor equipment conditions and used an anomaly detection service to predict potential breakdowns.
- Work orders were automatically generated, allowing proactive maintenance and avoiding downtime.

### SCADA System and Visualization

- Gousto built a SCADA system using Ignition, providing real-time visibility and situational awareness of their factory operations.
- They also used AWS IoT SiteWise for analytics and visualization.

### Overall Equipment Effectiveness (OEE)

- Gousto integrated OEE data into their system, enabling real-time monitoring and identification of areas for improvement.

### Digital Twin and Simulation

- They developed a digital twin of their factory, allowing them to replay past events, test scenarios, and optimize configurations.
- This simulation capability led to significant improvements in throughput (over 10% uplift).

## Future Plans

- Introduce containerization and GitOps for resilient infrastructure and continuous deployment.
- Upgrade the factory twin to enable short-term scenario testing and decision-making.
- Develop a "Factory API" to abstract vendor implementations and enable better integrations.
- Transition from rule-based logic to AI/ML models for predictive maintenance and decision support.

## Key Insights and Recommendations

- Start small with a proof of concept (POC) and deliver value incrementally.
- Leverage existing standards and tools (e.g., HighByte, AWS IoT Core) instead of building from scratch.
- Mesh teams from different disciplines (mechanical engineering, software engineering) for better collaboration and learning.
- Expose technology teams to the factory environment to gain a deeper understanding of operations.
- The goal is to move faster, go further, and enable data-driven decision-making across the organization.