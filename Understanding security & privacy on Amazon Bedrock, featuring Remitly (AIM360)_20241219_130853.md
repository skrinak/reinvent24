# Summary of AWS re_Invent 2024 - Understanding security & privacy on Amazon Bedrock, featuring Remitly (AIM360).txt

# Summary: Understanding Security & Privacy on Amazon Bedrock

## Introduction

- Security is a major concern for organizations when adopting generative AI (gen AI) technologies.
- This session covers the security features of Amazon Bedrock and best practices for building secure gen AI applications.

## Amazon Bedrock Security

### Data Privacy and Protection

- Amazon Bedrock does not store customer inference or training data, ensuring data privacy.
- Data is isolated per customer and remains in the same region as the API request.
- Customers decide which foundation models to enable for their users.
- All communication to/from/within Bedrock services is encrypted.
- Fine-tuned models can be encrypted with customer-managed KMS keys.
- Bedrock has achieved various compliance certifications.

### Connectivity

- Customers can access Bedrock through public or private connectivity options.
- Private connectivity is achieved through VPC endpoints, ensuring traffic stays within the AWS network.

### Access Control

- IAM administrators control who is authorized to access Bedrock resources.
- Policies can be used to grant or deny permissions to specific models.
- Application inference profiles allow granular control over model access through tags and IAM conditions.

### Observability and Auditability

- Amazon CloudWatch is used to monitor Bedrock metrics.
- Model invocation logging can be enabled to store request/response data in the customer's account.
- AWS CloudTrail provides a record of actions taken within the Bedrock account.
- Amazon Bedrock Guardrails ensure responsible AI policies are enforced.

## Remitly's Experience with Amazon Bedrock

- Remitly implemented Bedrock to enhance customer support experiences.
- Key considerations: fast resolution time, adaptability to multiple use cases, real-time chat experiences, and compliance.
- Generative AI provided superior intent classification, ease of customization, and scalability.
- Challenges included data discovery, response accuracy, data privacy, access control, and network security.
- Solution design: hybrid search, content retrieval, response generation, and response validation.
- Results: 25% of chats handled by the chatbot, high customer satisfaction, and only 3% escalations to human agents.
- Future plans: expand coverage, improve intent classification, generate marketing content, and integrate with Bedrock Guardrails.

## Patterns for Secure Gen AI Applications

### Building Correct Prompts

- System prompts define the model's behavior and capabilities.
- User prompts are the questions users ask.
- Optimized prompts significantly improve accuracy and prevent prompt attacks.

### Amazon Bedrock Guardrails

- Guardrails is a model-agnostic safeguard that blocks harmful input and output.
- It includes filters for content, sensitive information, denied topics, word filters, contextual grounding, and automated reasoning.
- Automated reasoning introduces deterministic checks for procedural documentation and explainable decision-making.

### Retrieval-Augmented Generation (RAG)

- RAG involves creating vector embeddings of data sources and retrieving relevant information based on user queries.
- Metadata filtering and authentication/authorization controls ensure data access is restricted.

### Agentic Behavior

- Agents can take autonomous actions based on user intent.
- Session attributes and deterministic controls ensure secure API calls and actions.
- Human-in-the-loop confirmation can be incorporated for added security.

### End-to-End Architecture

- Combine deterministic controls (IAM, CloudTrail, CloudWatch) with probabilistic controls (prompt engineering, Guardrails).
- Authenticate and authorize users, apply Guardrails, prompt-engineer agent instructions, and control access to knowledge bases and APIs.
- Implement defense in layers, leveraging both control types for different security aspects.

## Key Takeaways

- Understand the three stages of gen AI security: model security, model access, and application security.
- Leverage deterministic controls (IAM, KMS, network controls) for access management and data filtering.
- Utilize probabilistic controls (prompt engineering, Guardrails) to prevent harmful outputs and maintain relevance.
- Implement defense in layers by combining deterministic and probabilistic controls.
- Authenticate and authorize requests through traditional mechanisms, not the language model itself.

## Resources

- AWS Samples: https://github.com/aws-samples/amazon-bedrock-examples
- AWS Workshops: https://www.aws.amazon.com/bedrock/resources/
- AWS Documentation: https://docs.aws.amazon.com/bedrock/index.html