# Summary of AWS re_Invent 2024 - Toyota drives innovation & enhances operational efficiency with gen AI (AUT201).txt

# Summary

## Toyota Drives Innovation & Enhances Operational Efficiency with Generative AI

### Introduction

- The presentation covers various generative AI use cases that Toyota has worked on to drive innovation and enhance operational efficiency.
- Speakers: Sandeep, Stephen Ellis, Kordel France, and Paul.

### Generative AI for Automotive (Sandeep)

- Generative AI can potentially reduce design and development time by several weeks to months in the automotive industry.
- Potential use cases:
  - Product design and quality: Generate innovative design recommendations, evaluate vehicle aerodynamics.
  - In-vehicle experience: Real-time conversational assistants for guidance, route recommendations, and troubleshooting.
  - Service and maintenance: Guided troubleshooting steps for service technicians.
  - Autonomous driving: Generate synthetic edge cases for model training.
- AWS offerings for generative AI:
  - Low tier: Chips (Inferentia, Trainium, GPUs), SageMaker for full control.
  - Middle tier: Amazon Bedrock with 30+ foundation models, security, and customization options.
  - High tier: Amazon Q for solving business problems without worrying about the underlying models.

### Toyota's Mobility and Generative AI Vision (Stephen Ellis)

- Toyota is transitioning from a car manufacturing company to a mobility company, presenting opportunities and challenges.
- Knowledge retention platform to disseminate information across teams and regions using generative AI.
- Process: Interview subject matter experts, analyze documents, validate information, create writeups, and socialize knowledge.
- Benefits of generative AI:
  - Asynchronous knowledge transfer across the organization.
  - Context-aware transcription and translation.
  - Tailored responses for different audience expertise levels.
  - Future-proofing data for multiple models and iterations.

### GearPal and Battery Brain (Kordel France)

- GearPal: Reduce mean time to repair for machines on the manufacturing line.
  - Allows team members to ask questions and get troubleshooting guidance.
  - Data-agnostic ingestion pipeline for various document types and languages.
  - Golden query feedback system for model fine-tuning.
- Battery Brain: Reduce battery scrappage on the manufacturing line.
  - Provides guidance on processes and material properties.
  - Incorporates internet search results for state-of-the-art battery knowledge.
  - Handles complex data types like OneNote documents.
- Common RAG framework and data-agnostic ingestion pipeline reused across applications.
- Incorporates Toyota production standards for quality control.

### Code Modernization and Mainframe Modernization (Paul)

- Mainframe modernization: Converting mainframe code (COBOL) to modern languages (Java).
- Challenges: Shared environment, downstream system impact, and production risks.
- Collaboration between AWS and Toyota teams, including human feedback loops.
- Amazon Q's text classification capabilities for understanding COBOL code and deriving business rules.
- Knowledge graphs and contextual understanding for handling abbreviations and institutional knowledge.
- Iterative process with human validation, achieving over 90% accuracy.
- Future: Reasoning engines and formal logic for longer tasks.

### Conclusion

- Toyota invests in AI for both consumer and enterprise applications.
- Generative AI assists in driving innovation and enhancing operational efficiency in the automotive industry.