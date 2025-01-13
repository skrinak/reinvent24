# Summary of AWS re_Invent 2024 - Innovate with analytics and governance_ Customer Panel (ANT203).txt

Here is a comprehensive summary of the transcript in Markdown format:

# AWS re:Invent 2024 - Innovate with Analytics and Governance: Customer Panel (ANT203)

## Introduction

- Panelists:
  - Mirko Buholzer, VP of Engineering at Natera (Healthcare/Life Sciences)
  - Zach Anderson, Chief Data and Analytics Officer at NatWest (Financial Services)
  - Siva (Amazon Transportation)
- Moderated by Shikha Verma, Head of Product for Data and AI Governance at AWS

## Generative AI in Healthcare/Life Sciences

- Natera leverages Generative AI and Large Language Models (LLMs) to extract unstructured clinical data from patient records, combine it with their genetic test data, and create comprehensive patient journeys.
- This allows physicians to:
  - Understand the full treatment history and outcomes for individual patients.
  - Compare patient journeys and identify similar cases to inform treatment strategies.
- Generative AI enables this at scale, whereas previously it was only possible for small cohorts.

## Generative AI in Financial Services

- Generative AI has shifted the paradigm, with business units now actively demanding AI solutions instead of data scientists having to inspire them.
- Use cases:
  - Call summarization and pre-meeting information gathering for relationship managers.
  - Fraud investigation: Identifying fraud networks across accounts using graph embeddings and LLMs to extract entities and traverse the graph.
- Generative AI has enabled NatWest to discover fraud networks 10x faster and provide unprecedented information to law enforcement, leading to successful prosecutions and victim rescues.

## Generative AI at Amazon Transportation

- Amazon Transportation deals with petabytes of data daily, across 100+ systems, to orchestrate package delivery on a massive scale.
- They used a Composite AI approach, starting with expert system-based knowledge graphs and machine learning for root cause analysis.
- Generative AI (LLMs) is then used to represent the insights to station-level users (91% acceptance rate).
- Future plans include using LLMs for reasoning and agent frameworks to action the insights automatically.

## Advice and Learnings

### Siva (Amazon Transportation)

- Start with the right problem that is a real issue for someone, and use Generative AI as a means to solve it.
- Follow an incubation mechanism (validate the idea) and an operationalization mechanism (data platform, feature engineering, model pipelines, model management, etc.).

### Mirko Buholzer (Natera)

- Culture change is crucial when shifting from a centralized to a distributed data mesh model.
- Teams need to prioritize data, understand business questions, and manage data products effectively.
- Implement a culture where data is top of mind when implementing new functionality.

### Zach Anderson (NatWest)

- Be bold and pick projects that seem "magical" or infeasible now, as they may become possible by the time the project is completed due to the rapid pace of innovation.
- If a project fails initially, revisit it in a few months with new model capabilities.
- Encourage businesses to provide their hardest problems, even if they seem implausible currently.

## Key Takeaways

- Generative AI is enabling innovative use cases across industries by extracting insights from unstructured data and combining it with structured data.
- Embedding governance into workflows and pipelines is crucial for efficient and compliant AI adoption.
- Adopting a distributed data mesh model requires cultural change and prioritizing data across teams.
- Be bold in pursuing ambitious AI projects, as the pace of innovation may make the "magical" possible by the time the project is completed.