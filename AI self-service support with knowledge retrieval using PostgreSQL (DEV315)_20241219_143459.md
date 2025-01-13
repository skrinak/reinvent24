# Summary of AWS re_Invent 2024 - AI self-service support with knowledge retrieval using PostgreSQL (DEV315).txt

# AWS re:Invent 2024 - AI Self-Service Support with Knowledge Retrieval Using PostgreSQL

## Summary

Guillermo Ruiz and Elizabeth Fuentes, AWS Developer Advocates, presented a session on building an AI-powered travel assistant using Amazon Bedrock, PostgreSQL with vector support, and various AWS services. The main points and key insights from the session are as follows:

### Introduction

- The presenters shared a humorous story about booking flights to the wrong "Vegas" (Las Vegas, New Mexico instead of Las Vegas, Nevada) due to a single letter typo, highlighting the importance of accurate information retrieval and customer support.
- Traditional customer support channels often suffer from inconsistency, lack of personalization, limited agent knowledge, and potential data security issues, leading to poor customer experiences.

### Building the AI Travel Assistant

The AI travel assistant aimed to eliminate travel stress, fix problems proactively, and provide fast, personalized support. It was built using three main components:

1. **Knowledge Base**
   - A vector database (Amazon Aurora PostgreSQL with vector support) was used to store and retrieve information semantically.
   - PDF files containing airline policies and travel information were converted into vector embeddings and stored in the database for fast semantic search.
   - The knowledge base acts as the "brain" of the AI assistant, enabling accurate and context-aware responses.

2. **AI Agents**
   - Amazon Bedrock was used to build AI agents without training new machine learning models.
   - Agents were configured with foundation models, instructions, relevant data sources (knowledge base, passenger database, support ticket database), and available actions.
   - Agents can understand natural language queries, retrieve information from multiple sources, and generate comprehensive responses using large language models.

3. **Messaging Integration**
   - The AI agents were integrated with messaging applications like WhatsApp using API Gateway and Lambda functions.
   - Voice notes were transcribed using Amazon Transcribe, enabling voice interactions.
   - The integration allowed seamless customer interactions across various channels and supported multilingual queries.

### Key Highlights

- The solution was built using serverless architecture, enabling cost efficiency and auto-scaling.
- AI-powered retrieval was achieved through the use of pgvector in PostgreSQL.
- Seamless integration with messaging platforms like WhatsApp and multilingual support were enabled through Amazon Transcribe and foundation models.
- Amazon Bedrock facilitated the processing of multiple tasks and the integration of various data sources.
- The presenters emphasized the importance of responsible AI practices and provided resources for further exploration.

## Conclusion

The session demonstrated how AWS services like Amazon Bedrock, PostgreSQL with vector support, and serverless architecture can be combined to build AI-powered self-service support systems. The travel assistant example showcased the potential for personalized, context-aware, and multilingual customer interactions across various channels, ultimately improving the overall customer experience.