# Summary of AWS re_Invent 2024 - Build scalable RAG applications using Amazon Bedrock Knowledge Bases (AIM305).txt

Here is a comprehensive summary of the transcript in Markdown format:

# AWS re:Invent 2024 - Build Scalable RAG Applications using Amazon Bedrock Knowledge Bases

## Overview
- The session covers building scalable Retrieve Augmented Generation (RAG) applications using Amazon Bedrock Knowledge Bases.
- RAG allows customizing models by contextualizing the output with proprietary data (structured or unstructured).
- Amazon Bedrock Knowledge Bases is a managed service for creating end-to-end RAG workflows.

## Year in Review
- Over 50 new features were introduced in the past year, including:
  - Hybrid search, manual metadata filters, connectors to Salesforce and Confluence
  - Chunking strategies (hierarchical, semantic, custom)
  - Support for CloudFormation, Terraform, SDK, and CDK
  - LLM parser, custom prompts, query reformulation, and decomposition

## New Announcements
- Structured data retrieval: Native support for retrieving data from databases
- Auto-generated query filters: Filters generated automatically from the query
- Re-rank API: Post-processing to prioritize the most relevant content
- GraphRAG: Support for creating knowledge graphs from data sources
- Streaming responses: Generating responses token-by-token for improved performance
- RAG evaluation and LLM judge: Evaluating the validity of responses and iterating on the application

## Building Scalable RAG Applications: Methodology
1. **Data Strategy**: Have a proper strategy for different data types, chunking, and data preparation.
2. **RAG Infrastructure**: Select appropriate models and vector databases for latency and capabilities.
3. **Start Small and Simple**: Begin with a proof of concept, evaluate responses, and iterate.
4. **User Feedback**: Allow users to interact with the application and provide feedback for continuous improvement.
5. **Scalable Infrastructure**: Ensure the infrastructure can scale as the application becomes more complex.

## Enverus Journey
- Enverus built the "Instant Analyst" platform using Amazon Bedrock Knowledge Bases.
- The platform supports 25 years of energy industry data, structured and unstructured.
- Key phases: Planning, validation, development, testing, optimization, and platform building.
- Challenges addressed: Chunking, data synchronization, throttling, and retrieval accuracy.
- Benefits: Security, high performance, reduced research time, and AWS partnership.

## Advanced Techniques
- **Multimodal Data Processing**: Handling documents with images, tables, and other modalities.
- **Structured Data Retrieval**: Generating SQL queries from natural language queries and retrieving data from databases.
- **GraphRAG**: Understanding relationships between entities across multiple documents using knowledge graphs.

## Conclusion
- The session challenged attendees to start their RAG application journey, partner with AWS, and provide feedback to shape the product.