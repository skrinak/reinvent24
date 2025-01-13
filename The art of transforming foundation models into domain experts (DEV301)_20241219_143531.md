# Summary of AWS re_Invent 2024 - The art of transforming foundation models into domain experts (DEV301).txt

# AWS re:Invent 2024 - The art of transforming foundation models into domain experts (DEV301)

## Summary

This session provided a comprehensive overview of techniques for transforming large language models (LLMs) into domain experts tailored to specific business needs. The speakers, Sebastien and Greg, introduced five key methods and used analogies to explain them in an engaging manner.

### 1. Continued Pre-training

- Analogous to sending a model (Paul) back to university to learn more about a specific domain.
- Involves retraining the base LLM with a large quantity of domain-specific data (e.g., technical documentation, knowledge bases).
- Adapts the model to the desired domain but requires significant data and computational resources.
- Demonstrated using Amazon Bedrock.

### 2. Fine-tuning

- Analogous to providing internal training to the model (Paul) on specific conversation styles, tones, and frequently asked questions.
- Involves tuning the model's parameters to bias its outputs toward a particular style, vocabulary, or set of responses.
- Requires less data than continued pre-training but still generates a new model that needs to be deployed and maintained.
- Demonstrated using a labeled dataset from Kaggle and Amazon Bedrock.

### 3. Prompt Engineering

- Analogous to teaching the user (instead of the model) how to interact with the model effectively.
- Involves providing additional context and framing questions in a way that guides the model to generate more relevant and accurate responses.
- Demonstrated through examples of asking questions with varying levels of context.

### 4. Retrieval Augmented Generation (RAG)

- Analogous to introducing a librarian (Victor) who can quickly retrieve relevant documents from a database to assist the model (Paul) in answering questions.
- Involves creating embeddings (vector representations) of documents and storing them in a vector database for efficient semantic search.
- Allows the model to generate responses based on relevant information retrieved from the database.
- Demonstrated using Amazon Bedrock and the EU regulations dataset.

### 5. Agents

- Analogous to writing code (an agent) that can interact with the model and other tools or APIs to accomplish tasks.
- Involves using the model to classify which tools or APIs are needed to answer a question, then calling those tools and having the model generate a response based on the results.
- Demonstrated through a Python example using the Amazon Bedrock converse API and a stock price API.

The session also discussed factors to consider when selecting a base LLM, such as use case, deployment method, modality, accuracy, performance, budget, available data, licensing, and the ethics and responsible AI practices of the model provider.

Overall, the session provided a comprehensive toolbox of strategies for elevating LLMs from good to great, tailored to specific business domains and requirements.