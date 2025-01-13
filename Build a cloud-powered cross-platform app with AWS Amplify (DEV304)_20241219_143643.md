# Summary of AWS re_Invent 2024 - Build a cloud-powered cross-platform app with AWS Amplify (DEV304).txt

# AWS re:Invent 2024 - Build a Cloud-Powered Cross-Platform App with AWS Amplify

## Summary

Salih and Olivier, developer advocates at AWS, presented a comprehensive session on building cross-platform applications using AWS Amplify Gen 2. The session covered the following key points:

### Introduction to AWS Amplify

- **History of Amplify**: Amplify started in 2017 with the launch of Amplify JS, followed by the Amplify CLI in 2018, Amplify Hosting, and Amplify Studio in subsequent years.
- **Amplify Gen 2**: The latest version of Amplify, announced in 2023, introduces several improvements, including:
  - TypeScript-based backend infrastructure definition
  - Git-based full-stack CI/CD
  - File-based convention for backend services
  - Sandboxes for developer environments
  - Integration with Amazon CodeWheel for code completions and inline editing
  - Consolidated management console
  - Flexibility to extend with AWS CDK

### Live Coding Demo

The presenters conducted a live coding demo, showcasing the following features of Amplify Gen 2:

#### Authentication

- Implemented email-based authentication with custom email templates and user attributes
- Added pre-sign-up triggers to allow or deny sign-ups based on specific email domains

#### Data Modeling and Storage

- Defined data models for a travel planning application using the Amplify data modeling syntax
- Demonstrated one-to-many and many-to-many relationships between models
- Performed CRUD operations (Create, Read, Update, Delete) on data models

#### AI Integration

- Leveraged Amplify's AI capabilities to generate travel itineraries based on natural language prompts
- Streamed AI responses and parsed JSON data to store in the database

#### Storage

- Implemented user profile image upload and retrieval using Amplify Storage (backed by Amazon S3)

#### Extensibility with AWS CDK

- Showcased how to extend Amplify applications with additional AWS services using the AWS Cloud Development Kit (CDK)
- Demonstrated integrating Amazon Pinpoint for in-app messaging campaigns

## Key Insights and Conclusions

- **Simplicity**: Amplify Gen 2 simplifies the development of cross-platform applications by abstracting away complex infrastructure setup and management.
- **TypeScript-based Infrastructure**: Defining backend infrastructure using TypeScript allows for better tooling, code completion, and integration with the application codebase.
- **Git-based CI/CD**: Amplify Gen 2's Git-based CI/CD pipeline enables seamless deployment across multiple environments (dev, staging, production) directly from Git branches or pull requests.
- **Sandboxes**: Sandboxes provide isolated developer environments for testing and experimentation without impacting production resources.
- **Extensibility**: While Amplify Gen 2 offers a comprehensive set of built-in capabilities, developers can extend their applications with additional AWS services using the AWS CDK.
- **Open Source**: The demo application showcased during the session will be available as an open-source project in the AWS organization on GitHub, allowing developers to explore and learn from the codebase.

Overall, AWS Amplify Gen 2 aims to simplify and streamline the development of cross-platform applications by providing a comprehensive set of tools and services, while still allowing for extensibility and customization using AWS CDK.