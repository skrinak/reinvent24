# Summary of AWS re_Invent 2024 - Build Amazon Q apps to scale and drive community engagement (DEV201).txt

# Summary

## Introduction

- Viktoria and Linda met at re:Invent 2023 and started collaborating on organizing technical events and building communities.
- They share their insights and learnings from organizing events, building communities, and leveraging Amazon Q to scale their impact.

## Amazon Q and Generative AI on AWS

- Amazon Q is a generative AI service that allows users to connect to their data sources and ask questions based on their proprietary data.
- It provides a suite of products, including Amazon Q Business, which enables non-technical users to create generative AI applications without coding.
- AWS provides a comprehensive stack for building generative AI applications, including cost-efficient infrastructure, accelerated compute, SageMaker for training models, and Bedrock for accessing foundation models.

## Identifying Locations for Events

- To identify suitable locations for events, they scraped data from AWS User Groups and AWS Partners' websites.
- They used web crawlers, Lambda functions, and Step Functions to scrape dynamic and unstructured data from these sources.
- The scraped data was stored in S3 buckets and indexed using Amazon Q's S3 connector.
- By querying the indexed data, Amazon Q could provide accurate information about User Groups, Partners, and their locations.

## Identifying Speakers and Trending Topics

- They scraped data from AWS Community Builders, AWS Heroes, and the Sessionize speakers directory to identify potential speakers.
- They used Lambda functions and custom layers to scrape and structure the data.
- To better leverage the data with Amazon Q's language model, they concatenated the speaker information into natural language descriptions.
- They also scraped data from AWS Events YouTube channel and community blogs to identify trending topics and gain insights into how the community discusses events.

## Promoting Events and Creating Apps

- To promote events, they used Amazon Q to generate promotional content tailored to their tone and style, based on the event details and their sample captions.
- They also explored generating images using prompts based on the event city and topic.
- They created Amazon Q Apps by describing their desired inputs and outputs, allowing them to quickly retrieve relevant information for event planning.
- The apps could be published and shared within their organization.

## Architecture and Key Takeaways

- The complete architecture involved various data sources, web crawlers, S3 buckets, Lambda functions, EventBridge triggers, and the Amazon Q Business index.
- Key takeaways included having a specific use case, a comprehensive data strategy, ensuring compliant AI implementation, and optimizing for cost efficiency.
- They shared resources, including a GitHub repository and a workshop on building generative AI applications with Amazon Q Business.

The presentation covered the end-to-end process of leveraging Amazon Q and generative AI capabilities to streamline event planning and promotion, while emphasizing the importance of data strategy, compliance, and cost optimization.