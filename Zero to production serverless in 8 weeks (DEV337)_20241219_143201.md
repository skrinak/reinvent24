# Summary of AWS re_Invent 2024 - Zero to production serverless in 8 weeks (DEV337).txt

# AWS re:Invent 2024 - Zero to Production Serverless in 8 Weeks

## Summary

The speaker discusses a project they completed for an online pharmacy, Chemist4U, in the UK. The project involved building a system to integrate with a clinic that provides ADHD diagnosis and treatment services. The key requirements included securely receiving patient information and prescription data, handling payments, implementing a workflow for clinical checks, and integrating with the existing warehouse fulfillment system.

## Main Points

### Project Background
- Chemist4U is the third-largest online pharmacy in the UK, dispensing around 175,000-200,000 items per month.
- They formed a partnership with a clinic that needed a pharmacy to handle ADHD medication dispensing.
- The existing pharmacy couldn't scale to meet the demand, so Chemist4U took on the project.
- The project had a tight deadline of 8 weeks due to the existing pharmacy running out of medication.

### Serverless Approach
- The team chose a serverless approach to focus on business logic rather than infrastructure management.
- Serverless offered benefits like built-in high availability, low administration, rapid development, and auto-scaling.
- They used AWS CDK for infrastructure as code, TypeScript across the stack, and tools like Vitest and Zod for testing and validation.
- The project followed a hexagonal architecture pattern and used boilerplate code for quick setup.

### Development Process
- The team started with a prototype, focusing on the most complex area (the integration) first.
- They defined the interface early and deployed a stubbed API for the third-party clinic to develop against.
- For the customer-facing website, they used off-the-shelf components and templates to keep it simple.
- They implemented error handling using AWS Chatbot to send notifications to Slack or Teams.
- The team was small (4 engineers, 1 tester, and a product owner) to move quickly.
- They followed a lean, agile process with small, deployable tasks and heavy automation.

### Key Insights
- Defining interfaces early and using stubbed APIs allowed parallel development with third parties.
- Automation and static code analysis were crucial for maintaining momentum and code quality.
- The "good enough" approach prioritized functionality over perfection, with plans for future refactoring.
- The project was an MVP but successfully launched and enabled business growth.

## Important Conclusions
- The team successfully delivered a serverless system in 8 weeks, meeting the tight deadline.
- The project enabled Chemist4U to enter a new B2B market and drive business growth.
- Serverless, automation, and agile practices were key enablers for rapid development.
- Future steps include refactoring into microservices, improving observability, and event-based tracing.