# Summary of AWS re_Invent 2024 - Build Amazon Q apps to scale and drive community engagement (DEV201).txt

Here is a comprehensive summary of the transcript, formatted in Markdown with appropriate headers and bullet points:

# AWS re:Invent 2024 - Build Amazon Q apps to scale and drive community engagement (DEV201)

## Introduction

- The speakers, Viktoria and Linda, met at a previous re:Invent event and discovered their shared passion for organizing technical community events.
- They decided to collaborate and share their insights on using Amazon Q to streamline the process of organizing events, engaging with the community, and amplifying their impact.

## Amazon Q and Generative AI Capabilities

- Amazon Q is a generative AI service that allows users to connect to their proprietary data sources and ask questions based on that data.
- It supports over 40 built-in connectors for various data sources, including Salesforce, Google Drive, and web crawlers.
- Amazon Q ensures data security by respecting permissions and querying identity providers for access control.
- Users can create plugins and custom actions within Amazon Q to perform tasks like sending emails or creating tickets based on the retrieved data.

## Identifying Event Locations

- To identify suitable locations for events, the speakers used two data sources: AWS User Groups and AWS Partners.
- For AWS User Groups, they initially planned to use the web crawler connector to scrape data from the Meetup page. However, they encountered challenges with dynamically generated content and had to create a custom Lambda function to scrape the data.
- For AWS Partners, they used the web crawler connector to scrape unstructured data from individual partner pages, as the information varied across partners.

## Identifying Speakers

- The speakers leveraged multiple data sources to find potential speakers for their events:
  - AWS Community Builders and Heroes data scraped from AWS websites
  - Sessionize speakers directory, scraped using a custom Lambda function and Beautiful Soup library
  - They created natural language descriptions by concatenating various data points to help Amazon Q better understand the speaker information.

## Identifying Event Dates

- To avoid scheduling conflicts with major events like re:Invent, the speakers scraped data from the AWS Events YouTube channel and Meetup.com using APIs and web crawlers.
- They leveraged AWS Secrets Manager to store authentication credentials required for scraping certain websites.
- Amazon Q's capabilities allowed them to identify suitable dates for their events while considering other regional events and holidays.

## Promoting Events

- To promote their events effectively, the speakers used Amazon Q to generate promotional content tailored to their tone and style.
- They scraped data from the AWS Events YouTube channel (using APIs) and the community.aws blog (using web crawlers) to provide Amazon Q with additional context and knowledge.
- By providing sample captions and prompts, Amazon Q could generate promotional posts and image descriptions that matched the speakers' preferred communication styles.

## Building Amazon Q Apps

- Instead of repeatedly asking individual questions, the speakers created Amazon Q Apps to streamline the event planning process.
- These apps allowed them to input parameters like the event topic and city, and Amazon Q would generate suggestions for venues, speakers, promotional content, and even image prompts based on the ingested data sources.
- The apps could be customized by adjusting prompts, selecting relevant data sources, and adding additional output widgets.
- The apps could be published and shared within the organization, enabling collaboration and scaling the impact of their event planning efforts.

## Key Takeaways

- Generative AI requires a specific use case and a comprehensive data strategy.
- Ensure compliant AI implementation by checking data usage permissions and adhering to guidelines.
- Optimize for cost efficiency by considering data update frequencies and indexing requirements.
- The speakers provided resources, including a GitHub repository and a workshop, to help others get started with building generative AI applications using Amazon Q Business.

Overall, the presentation demonstrated how Amazon Q and generative AI can be leveraged to streamline event planning, engage with the community more effectively, and amplify the impact of technical events by leveraging proprietary data sources and tailoring content to specific communication styles.