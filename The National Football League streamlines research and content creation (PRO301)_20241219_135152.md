# Summary of AWS re_Invent 2024 - The National Football League streamlines research and content creation (PRO301).txt

# Summary

## Main Points and Key Insights

### Background and Motivation

- The National Football League (NFL) partnered with AWS to develop a generative AI solution called "Playbook Pro" to streamline research and content creation for their production team.
- The existing process of finding relevant video footage and plays was time-consuming, involving multiple tools and filtering steps, hindering the efficiency of content creators.
- The goal was to enable natural language queries to retrieve relevant plays and video assets quickly and intuitively.

### Proof of Concept (POC) Development

- The AWS Gen AI Innovation Center collaborated with the NFL team to identify the problem and build a POC.
- Key challenges included:
  - Accurately translating natural language queries into database-understandable filters and API calls.
  - Handling entity recognition, duplicate names, and complex queries with multiple constraints.
  - Providing efficient and reliable responses within seconds.
- Techniques employed:
  - Pre-processing data and documentation for better language model understanding.
  - Using step-by-step reasoning and providing explanations to users for transparency.
  - Including correct and incorrect examples to guide the language model's behavior.
- The POC achieved 90% accuracy on unseen test data with an average response time of 20 seconds, validating the approach.

### Production Implementation

- AWS Professional Services team developed an agentic workflow architecture to take the POC to production.
- The architecture mimics human decision-making processes:
  - Assessing intent and confirming entities (players/teams) upfront.
  - Retrieving and leveraging past memories (similar tasks) from a vector database.
  - Breaking down the problem into sub-tasks (API documentation review, API call generation, etc.).
  - Introducing error handling and self-correction loops.
  - Enabling the system to learn from successful executions and commit them to memory.
- Key components: language models, workflow orchestration (serverless compute), and memory (MemoryDB for Redis).
- The architecture allows for enhancements, improvements, and new use cases.

### Impact and Future Work

- Playbook Pro went into production in August 2022, onboarding 250 users within the first month.
- Content creators can now find relevant footage in 30 seconds, compared to 10 minutes previously, freeing up time for creative work.
- Future plans include:
  - Expanding to more Next Gen Stats API endpoints and the NFL API for broader coverage.
  - Supporting queries about players from pre-2017 (before Next Gen Stats era).
  - Exploring fan-facing applications of the solution.

## Important Conclusions

- Generative AI can significantly streamline research and content creation processes by enabling natural language queries and leveraging large language models.
- A systematic approach, involving stakeholder alignment, POC development, and iterative refinement, is crucial for successful implementation.
- An agentic workflow architecture, mimicking human decision-making processes, can effectively translate natural language queries into database queries and retrieve relevant information.
- Continuous learning and memory capabilities allow the system to improve over time, reducing the space of unknown tasks and enhancing efficiency.
- Collaboration between domain experts (NFL) and technology partners (AWS) is key to developing tailored and impactful solutions.