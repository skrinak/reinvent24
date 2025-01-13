# Summary of AWS re_Invent 2024 - Pioneering gen AI in aviation_ MAG_s intelligent airport revolution (INO110).txt

# Summary: Pioneering Gen AI in Aviation: MAG's Intelligent Airport Revolution

## Introduction

- Mike Bainbridge, Innovation Programs at AWS, introduces the session on how Manchester Airports Group (MAG) used generative AI to transform the passenger experience at their airports.
- The session covers the customer problem, the digital experience delivered, the solution architecture, and the journey to production.

## MAG and the Customer Challenge

- Jon Fowler, Chief Operating Officer at London Stansted Airport, introduces MAG:
  - The UK's largest airport operator, with Manchester, East Midlands, and London Stansted airports.
  - Serving up to 65 million passengers annually to 261 destinations.
  - Employing 38,000 people and contributing £8 billion to the UK economy.
- The challenge: With a diverse passenger base (50% from outside the UK) speaking over 40 languages, how can MAG better serve and inform customers, answer their questions, and maximize value from their custom?

## The Digital Experience and Solution Architecture

- Ryan Cant, Chief Digital Officer at MAG, describes the hypothesis: Using generative AI (Amazon Bedrock) to interact with customers' questions in a human-like way, in multiple languages.
- The AWS Prototyping Team's Val Cohen explains the prototyping process, architecture, and key components:
  - API Gateway, Lambda, DynamoDB for chat history, Amazon Kendra for vector database, and Amazon Bedrock for LLM orchestration.
  - Retrieval Augmented Generation (RAG) for answering questions using website content.
  - LLM agents and custom tools for handling flight information and weather queries.
  - Support for multiple languages, low latency, and staying on topic using Bedrock Guardrails.

## Journey to Production and Impact

- Ryan Cant discusses the challenges faced in moving from prototype to production:
  - Addressing hallucination and overconfidence issues through rigorous testing and guardrails.
  - Building confidence among stakeholders by demonstrating the system's capabilities and limitations.
- After addressing these challenges, the Virtual Airport Liaison (VAL) was launched in November 2023 across MAG's three airports, starting with London Stansted.
- Early impact and benefits:
  - Positive feedback from customers and staff, especially for multi-language support.
  - Integration with digital wayfinding for gate information.
  - Unintended benefits: Insights into customer queries (e.g., toilet locations, travel to London) for improving operations and commercial opportunities.
- Future plans include a mobile release, personalization, and integration with MAG's digital travel marketplace (CAVU).

## Lessons Learned and Takeaways

- Focus on understanding the customer problem deeply before developing solutions.
- Consider the human element and how new technologies can enhance existing capabilities, not replace people.
- Adopt an iterative approach, with launch day being the start of a journey of discovery and continuous improvement.
- Successful innovation requires selecting the right stakeholders, focusing on problems (not projects), and defining the business value upfront.

## Additional Resources

- Innovation Ambassadors Podcast: Insights into addressing the customer challenge.
- "This Is My Architecture" video: Detailed look at the AWS architecture and development process.