# Summary of AWS re_Invent 2024 - Building and releasing robust generative AI solutions on AWS (BWP302).txt

# AWS re:Invent 2024 - Building and releasing robust generative AI solutions on AWS

## Summary

This session covered the development and deployment of robust generative AI (GenAI) solutions on AWS, with a focus on the Buy with Prime service. The presenters shared their experiences, best practices, and key insights gained from building two GenAI solutions: a merchant support assistant and a shopper assistant.

### Buy with Prime and the Need for GenAI Solutions

- Buy with Prime is an Amazon service that enables brands to offer Prime delivery and fulfillment services on their own websites, streamlining operations and attracting shoppers.
- With the increasing number of services and integration patterns offered by Amazon, merchants found it overwhelming to navigate the information and resources available.
- To address this, Amazon developed two GenAI solutions:
  1. **Merchant Support Assistant**: A knowledge-based chatbot that helps merchants find relevant information and resources faster and more accurately.
  2. **Shopper Assistant**: A conversational AI assistant that helps shoppers with product-related queries, order tracking, and customer support.

### Key Requirements and Architecture

The key requirements for these solutions were:

1. **Leveraging existing knowledge content**: Utilize the existing product information and merchant knowledge bases instead of building new data sources.
2. **Contextual awareness**: Understand the context of the user's query and provide relevant responses.
3. **Seamless human handoff**: Transfer queries that the AI cannot handle to human agents, ensuring a seamless customer experience.

The architecture for these solutions involved:

- **Amazon Bedrock**: Used for knowledge ingestion, conversational AI, and guardrails.
- **AWS Services**: Amazon S3 for static data sources, web crawlers for dynamic data sources, Amazon Connect for customer interactions, and Amazon Lex for initial intent classification.

### Key Results and Impact

- The merchant support assistant saw a 30% increase in merchant engagement with the search capability.
- 95% of the queries handled by the shopper assistant were successfully resolved by the chatbot.
- The solutions significantly improved the merchant and shopper experience, driving innovation for direct-to-consumer (DTC) businesses.

### Best Practices and Key Learnings

The session covered several best practices and key learnings, including:

1. **Automated Evaluation**: Implementing automated evaluation algorithms (LLM-based, METEOR, and ROUGE) to assess the quality and accuracy of GenAI responses, and creating positive and negative test cases.
2. **Traceability**: Enabling traceability by using unique request IDs and pushing logs to a single CloudWatch group for easier troubleshooting.
3. **Customer Data Isolation**: Physically isolating customer data in separate knowledge bases and authorizing requests to access only the relevant knowledge base.
4. **Improvement Cycle**: Establishing an improvement cycle involving data updates, knowledge base synchronization, and expert evaluation to ensure the GenAI solutions remain aligned with business changes.
5. **Security Threats**: Addressing security threats specific to GenAI, such as prompt injection, insecure output handling, over-reliance, and sensitive information disclosure, using Bedrock's built-in guardrails and policies.
6. **Data Backups**: Enabling versioned backups of data sources (e.g., S3 buckets) and providing tools to roll back data to a specific point in time, ensuring data integrity and recoverability.

The session concluded by emphasizing the importance of considering evaluation, security, and best practices when building robust GenAI solutions on AWS.