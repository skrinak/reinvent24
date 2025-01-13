# Summary of AWS re_Invent 2024 - Implementing Amazon Q Developer_ Lessons from the field (DEV310).txt

# Amazon Q Developer: Lessons from the Field (DEV310)

## Overview

This presentation covers the implementation of Amazon Q Developer, an AI-powered pair programming tool, and the lessons learned from using it in the field. The key points and insights are as follows:

## Opportunities with Amazon Q Developer

- Amazon Q can help with various developer tasks such as:
  - Writing new code
  - Refactoring and code maintenance
  - Understanding new codebases
  - Production support and bug fixing
  - Writing unit tests
  - Automating infrastructure

- The top three use cases for Amazon Q are:
  1. Manual refactoring and code maintenance
  2. Scaling code quality across teams
  3. Handling large codebases

## Deployment Steps

- Choose between the free tier or the pro tier
  - Free tier has limits on interactions, developer agents, lines of code, and queries
  - Pro tier allows user management, security policies, customization, and higher limits
- Authenticate using an AWS Builder ID or AWS IAM Identity Center
- Install the Amazon Q extension or plugin in the IDE (e.g., VS Code, JetBrains)
- Use interactive (chat-based) or asynchronous (long-running tasks) developer experiences

## Demos

1. **New Feature Development**: Amazon Q can create a Flask API with CRUD operations from scratch, based on a prompt.
2. **Code Explanation**: Amazon Q can provide detailed explanations of code snippets, including examples and outputs.
3. **Code Transformation**: Amazon Q can migrate Java code from version 8 to 17, updating dependencies and project configurations.

## Lessons Learned

- Implement an AI acceptable use policy and onboarding plan for developers
- Use AWS partner credits to run a proof-of-concept (POC)
- Developers become expert prompt engineers over time
- Amazon Q can help reduce the number of open browser tabs and reliance on Google and Stack Overflow
- Challenges include handling large files, usability issues with the VS Code extension, and customization requirements

## Challenges and Solutions

- Large files may need to be split into smaller chunks or handled function-by-function
- Inline Code Suggestion feature in VS Code improves usability
- Customization requires at least 20 MB of data for training

## Personal Experience

- Amazon Q did not implement expected coding style improvements during Java code transformation
- The product team has added this feature to the backlog based on feedback

## Conclusion

Amazon Q can boost developer productivity by accelerating workflows, reducing repetitive tasks, and allowing focus on higher-value activities. While AI may not replace developers anytime soon, it can make them more creative, efficient, capable, and productive.