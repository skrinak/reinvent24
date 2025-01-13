# Summary of AWS re_Invent 2024 - Transforming AV_ADAS development at Continental with generative AI (AUT307).txt

# AWS re:Invent 2024 - Transforming AV/ADAS Development at Continental with Generative AI

## Summary

### Introduction

- Jeff, a product leader at AWS Industry Products, runs the automotive products group, which builds automotive-specific services and solutions using a co-development model with customers.
- Continental, a major tier-one automotive supplier, challenged AWS to help them get more out of their limited engineering resources and manage the massive amounts of data involved in developing ADAS (Advanced Driver Assistance Systems) and autonomous driving features.

### Challenges in Autonomous Mobility Development

- Transitioning from Level 2 (partial automation) to Level 3 (conditional automation) autonomy requires significant testing and rigor to ensure the system is safer than human drivers.
- ADAS features, even at lower levels of autonomy, provide unprecedented value by reducing traffic deaths, injuries, and crashes.
- Developing autonomous mobility systems involves processing massive amounts of data from various perception sensors (cameras, radars, lidars), amounting to 50-80 terabytes per day or hundreds of petabytes per year.
- Developers often spend 60-70% of their time finding the right data for their specific tasks (annotation, training, simulation, verification, and validation).
- Supporting different data formats, tool chains, and applications for various data-driven tasks is complex and costly.
- Scalability is a challenge, as systems need to ingest and process petabytes of data daily for simulation and validation.

### Continental's Collaboration with AWS

- Continental has 15 years of experience in data-driven development and decided to move to the cloud with AWS.
- They developed the CAEdge (Continental Automotive Edge Computers) platform on AWS, which provides services for developing ADAS and autonomous driving features.
- The platform can ingest up to 1 petabyte of data per day, process it, extract relevant metadata, and provide it to developers for various use cases.
- Continental aimed to reduce operational costs by 60%, reduce the time spent finding data sets, and leverage generative AI technologies to improve algorithms and bring more value to customers.

### Scene Search Solution

- AWS and Continental collaborated to develop a generative AI-based scene search solution to address the challenge of finding relevant data for developers.
- The solution combines state-of-the-art approaches, including generative AI, machine learning, and non-ML retrieval techniques, to support semantic search, custom annotations, and visualization.
- Developers can use natural language queries (e.g., "pedestrians in the rain with glare") and structured searches to find specific driving scenes across multimodal data.
- The solution includes components for data extraction, indexing and querying, and user interface for curation.
- A demo showcased the ability to search for specific scenarios (e.g., construction cones, chickens on the road) and quickly identify true positives and false positives for downstream tasks like annotation and simulation.

### Key Takeaways

- Autonomous mobility development involves managing massive amounts of multimodal data and supporting complex tool chains and data formats for various data-driven tasks.
- Generative AI and scene search solutions can help developers find relevant data more efficiently, reducing the time spent on data discovery and curation.
- Standardized APIs and middleware layers can facilitate integration of new technologies and applications, enabling faster innovation and adaptation to changing requirements.
- Collaborations between cloud providers and automotive companies can drive transformative solutions to address the challenges of developing safer and more advanced autonomous driving systems.

### Call to Action

- Reach out to AWS representatives to learn more about the collaboration approach and solutions for autonomous mobility development.