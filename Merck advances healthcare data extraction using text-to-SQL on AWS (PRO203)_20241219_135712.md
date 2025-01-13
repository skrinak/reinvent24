# Summary of AWS re_Invent 2024 - Merck advances healthcare data extraction using text-to-SQL on AWS (PRO203).txt

# Summary

## Merck's Challenges in Healthcare Data Analytics

### Key Points:

- Merck deals with a large number of real-world data sources (electronic medical records, insurance claims data, etc.) from various vendors, each with unique data structures and variables.
- Developing SQL queries across these diverse datasets is challenging due to the complexity and lack of standardization.
- Common data models, which translate variables into a common format, can lead to loss of fidelity with the original raw data.
- Cohort builders used by citizen data scientists rely on common data models or require expensive tools with a learning curve.
- Ensuring accurate capture of clinical concepts using vetted code lists from clinical experts is essential.

## Text-to-SQL Solution with Generative AI

### Key Insights:

- Merck developed a Text-to-SQL solution using AWS Generative AI services to streamline data extraction across diverse datasets.
- The solution leverages a large language model (LLM) trained on Merck's data documentation, schemas, and sample queries to generate SQL statements from natural language queries.
- The pipeline includes components for providing database schemas, sample data, few-shot examples, and optional tools (e.g., mapping IDs to readable values).
- The LLM generates a summary of the intended query for user validation before generating the final SQL statement.
- The solution allows users to edit and refine the generated SQL statements and provides execution capabilities against the target database.
- A feedback system is incorporated to collect user input for further fine-tuning of the LLM.

### Performance and Impact:

- The solution achieved over 97% accuracy on a test dataset, with 100% accuracy for easy and medium queries after a single re-prompt.
- The solution empowers business users and analysts to focus on insights rather than writing complex SQL queries.
- Merck plans to expand the solution to other real-world data sources, optimize performance, collect real user queries, and explore automated accuracy evaluation methods.

### Future Directions:

- Roll out the solution to all real-world data users at Merck.
- Optimize performance by storing user queries, incorporating feedback, and exploring different LLMs and prompts.
- Develop a real dataset of user queries for evaluation.
- Explore automated methods for evaluating the accuracy of generated SQL statements.