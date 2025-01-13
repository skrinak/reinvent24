# Summary of AWS re_Invent 2024 - Power a cost-effective RAG solution using Amazon Titan Embeddings Text (AIM358).txt

# Summary

## Introduction to Embeddings

- Embeddings are numerical representations of text that encode semantic meaning, allowing retrieval of relevant documents based on meaning rather than just lexical matching.
- Embeddings help overcome limitations of lexical search by understanding the semantics of documents and queries.
- Key considerations for using embeddings at scale include the cost of creating embeddings for documents and queries, supporting multiple languages, embedding speed, and storage costs for embeddings.

## Amazon Titan Embeddings

- Amazon Titan Embeddings is a cost-effective solution for creating and storing embeddings at scale.
- It supports English, multilingual, and code embeddings with low embedding costs (e.g., $0.00002 per 1K tokens).
- Titan Embeddings offers options to reduce storage costs, including dimension reduction (chopping), rounding, and binary encoding, with different trade-offs between storage savings and performance.
- The recently launched binary encoding option provides a good balance, with up to 98.44% memory savings while retaining around 96.3% of the original performance.

## NetDocuments Success Story

- NetDocuments, a legal document management company, faced challenges with the high storage costs of float-point embeddings for their 10 billion documents.
- By adopting Amazon Titan Embeddings with binary encoding, they achieved significant cost savings of around 90% in storage requirements.
- The reduced storage needs translated to fewer instances required, lowering the overall cost from $5.4 million per year (with float-point embeddings) to around $430,000 per year.
- Binary embeddings also improved CPU and memory efficiency, enabling better performance with fewer resources.

## Architecture and Best Practices

- A basic architecture involves ingesting documents into Amazon S3, creating embeddings using Titan Embeddings, storing embeddings in OpenSearch Serverless, and retrieving relevant documents based on embedded queries.
- To improve precision while leveraging binary embeddings' storage savings, a re-ranking approach can be employed:
  1. Store both binary and float-point embeddings (e.g., in S3 for float-point embeddings).
  2. Use binary embeddings for initial retrieval from OpenSearch.
  3. Re-rank the results using float-point embeddings for increased precision.
- This hybrid approach combines the storage cost benefits of binary embeddings with the precision of float-point embeddings for re-ranking.

In summary, the session covered the benefits of embeddings for semantic search, the cost-effective solution offered by Amazon Titan Embeddings (especially with binary encoding), a real-world success story from NetDocuments, and architectural best practices for leveraging binary embeddings while maintaining high precision through re-ranking techniques.