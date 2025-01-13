# Summary of AWS re_Invent 2024 - Generative AI–powered graph for network digital twin (TLC202).txt

# Summary

## Main Points

1. **Autonomous Networks**: The goal is to enable autonomous networks with capabilities like detecting, reading, automating observability, root cause analysis, failure detection, and remediation. This is a vision being pursued by industry bodies and operators like Orange.

2. **Network Complexity**: Telecom networks are highly complex, with millions of equipment pieces across different domains (transport, core, radio access), generating massive volumes of data (alarms, KPIs, call records) and exhibiting diverse traffic patterns across geographies.

3. **Limitations of Current Approaches**: Traditional approaches based on expert rules, correlation, and siloed analysis of individual equipment data have limitations in handling network complexity, maintaining rules, and capturing dependencies between network elements.

4. **Graph-based Approach**: The proposed solution represents the network as a heterogeneous, temporal graph, capturing the topology and dependencies between network nodes across domains. This graph-based approach leverages graph neural networks, graph analytics, and generative AI to enable efficient root cause analysis, anomaly detection, and network change management.

5. **Key Components**:
   - Graph Modeling: Automated discovery and representation of network topology, including inferring missing links.
   - Graph Machine Learning: Applying graph neural networks for tasks like forecasting, anomaly detection, and link prediction.
   - Graph Analytics: Probabilistic models and algorithms for identifying critical nodes, communities, and root causes within the network graph.

6. **Benefits and Results**: The graph-based approach demonstrated significant reduction in time for root cause analysis (from hours to seconds), provided end-to-end multi-layer network topology visibility, and enabled effective alarm management through generative AI-powered reports and interactions.

## Key Insights

- Capturing network dependencies and temporal changes is crucial for effective root cause analysis and anomaly detection.
- Graph representations and techniques like graph neural networks and graph analytics can effectively model and analyze complex network topologies and dependencies.
- Combining graph-based approaches with generative AI enhances interpretability and usability for network operations teams.
- The solution breaks down silos between different network domains (transport, core, radio access) and provides a unified view of the end-to-end network topology.

## Important Conclusions

- The collaboration between Orange and AWS has demonstrated the potential of graph-based techniques and generative AI in enabling autonomous networks and efficient network operations.
- The proposed approach addresses limitations of traditional rule-based and correlation-based methods, providing a scalable and adaptable solution for complex, heterogeneous networks.
- Further work is planned to make the solution live, scale it to full country-level networks, and continue enhancing the spatio-temporal graph neural network models.
- The combination of cloud architecture, graph technologies, machine learning, and generative AI presents a promising path towards realizing the vision of autonomous networks.