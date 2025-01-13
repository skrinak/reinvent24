# Summary of AWS re_Invent 2024-Unlocking power of structured data with Amazon Bedrock Knowledge Bases-AIM396-NEW.txt

# Summary: Unlocking the Power of Structured Data with Amazon Bedrock Knowledge Bases

## Introduction

- The session covers Retrieval-Augmented Generation (RAG) and how Amazon Bedrock Knowledge Bases can help unlock the power of structured data.
- RAG involves retrieving relevant information based on a user query, augmenting it with the query, and passing it to a foundational language model to generate a response.
- Unstructured data can be handled using semantic search, while structured data requires a different approach, such as natural language to SQL conversion.

## Structured Data Retrieval with Bedrock Knowledge Bases

- Bedrock Knowledge Bases can translate natural language queries into SQL queries, execute them on the user's database, and retrieve the relevant tabular data.
- The key challenges in natural language to SQL conversion include:
  - Personalization to the user's database schema, table names, and column names.
  - Personalization to the data format and how the data is stored.
  - Understanding the SQL dialect and framing queries correctly.

- Bedrock Knowledge Bases addresses these challenges by:
  - Fetching the database metadata and past queries to build a knowledge bank.
  - Leveraging an understanding of SQL dialects and query engines.
  - Offering query configuration options like adding descriptions, inclusion/exclusion filters, and curated queries.

## Demo

The demo covered the following aspects:

1. **Creating a Structured Knowledge Base**
   - Configuring the query engine (currently supporting Amazon Redshift)
   - Specifying data storage (Redshift managed storage or AWS Glue Data Catalog)
   - Authentication mechanism (IAM role or Redshift database user)

2. **Query Generation and Execution**
   - End-to-end RAG flow: Generating SQL, executing it, and summarizing the response using a foundational model.
   - Retrieve API: Generating SQL and returning the tabular data without generating a response.
   - Generate Query API: Returning the SQL query corresponding to a natural language question.

3. **Advanced Query Configuration**
   - Adding descriptions for ambiguous table or column names.
   - Using curated queries for custom vocabulary or complex SQL queries.

4. **Data Protection**
   - Detecting and blocking data modification queries (e.g., DELETE, UPDATE) for safety.

## Conclusion

- Bedrock Knowledge Bases provides a fully managed service for orchestrating RAG workflows, capable of handling both unstructured and structured data.
- The session encourages trying out Amazon Bedrock Knowledge Bases, providing feedback, and discussing use cases with the team.