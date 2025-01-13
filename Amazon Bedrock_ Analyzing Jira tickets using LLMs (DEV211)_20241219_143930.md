# Summary of AWS re_Invent 2024 - Amazon Bedrock_ Analyzing Jira tickets using LLMs (DEV211).txt

# Summary: Analyzing Jira Tickets using Amazon Bedrock and Large Language Models

## Introduction

- The talk focuses on a use case of supporting a national lab's cloud operations team by analyzing their Jira tickets using Amazon Bedrock and large language models (LLMs).
- The goal is to extract insights from over 4,000 Jira tickets without manually reading through them, enabling the creation of better FAQs and identifying emerging trends.

## Understanding the Jira Ticket Use Case

- Jira provides JQL (Jira Query Language) to search and filter tickets, but it doesn't reveal unknown trends or help connect researchers working on similar issues.
- Extracting Jira ticket data using the Jira API and cleaning the data was a crucial first step.

## Diving into Amazon Bedrock

- Initially, Amazon Comprehend was used for entity recognition but struggled with the unclean data.
- Amazon Bedrock, which provides access to LLMs from various providers, offered a promising solution.
- Setting up Bedrock involved creating a knowledge base, syncing it with the data, and testing it.
- The chunking strategy for dividing data into vectors was an important consideration, depending on the data format.
- Different LLMs were required for creating the knowledge base and for querying it.

## Key Insights and Future Work

- Prompt engineering and testing different LLMs are crucial for obtaining accurate and relevant results.
- Inserting all 4,000 tickets and addressing hallucinations encountered during testing are future goals.
- Creating a pipeline and taking a DevOps approach to coding will be necessary for scalability.
- Lessons learned include the importance of understanding the data, requesting the right LLMs upfront, and selecting the appropriate chunking strategy.

## Conclusion

- The talk provided insights into the process of leveraging Amazon Bedrock and LLMs to analyze Jira tickets, highlighting challenges, lessons learned, and future plans.
- The goal is to create better FAQs and identify trends that might otherwise go unnoticed, ultimately improving support for researchers at the national lab.