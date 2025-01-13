# Summary of AWS re_Invent 2024 - Building an AI-powered shopping assistant  (RCG204).txt

# Summary: Building an AI-powered Shopping Assistant with AWS

## Introduction

- Pat Riley and Yuri Chamarelli, Generative AI Specialists at AWS, discuss how to build an AI-powered shopping assistant to enhance the online shopping experience.
- They highlight common challenges faced by online shoppers, such as product discovery, information overload, decision paralysis, and accessibility issues.

## Evolution of Retail Search

- A brief history of retail search:
  - 1990s: Regex search (string matching)
  - 2000s: Search Engine Optimization, auto-complete, better UI
  - 2020s: Machine learning optimization, natural language processing
  - 2024: Chatbots, agentic workflows, and the future of online shopping

## Benefits of an AI Shopping Assistant

- Provide online shopping assistance and expertise, similar to in-store specialists
- Improve conversion rates and reduce shopping cart abandonment
- Remove decision paralysis by distilling options and recommendations
- Reduce information overload by presenting curated options
- Enhance accessibility for customers with visual or auditory impairments

## Demo: Retail Assistant for Home Improvement

- Yuri demonstrated a fictional home improvement website with an AI shopping assistant powered by AWS services.
- The assistant guides the user through building an outdoor deck, providing product recommendations, considerations, and contextual knowledge.
- Key AWS services used:
  - React frontend hosted on CloudFront and S3
  - AppSync (GraphQL API) for connecting the chatbot to DynamoDB
  - Amazon Bedrock for the chatbot and reasoning
  - OpenSearch as a vector database for semantic product search
  - DynamoDB for maintaining conversational context

## Benefits of Using Amazon Bedrock

- Agile and fast development of AI assistants
- Ability to train and customize models
- Support for single or multi-agent flows
- Built-in security and privacy features

## Conclusion

- Feedback from attendees is welcomed to improve the AI shopping experience.
- AWS provides a comprehensive set of services to build AI-powered shopping assistants, enhancing online retail experiences.