# Summary of AWS re_Invent 2024 - Strengthening the safety net_ Transforming 211 with Amazon Connect (IMP207).txt

# AWS re:Invent 2024 - Strengthening the Safety Net: Transforming 211 with Amazon Connect

## Introduction

- Presented by Veena (Senior Solutions Architect, AWS Nonprofit Team) and Chris Ticknor (Chief Transformation Officer, United Way of Orange County)
- United Way is one of the largest nonprofits in the world, coordinating efforts to solve societal challenges in local communities.
- Over 50% of United Ways operate their local 211 service, which is a social services directory and information helpline.

## The State of Things

- Orange County faces significant challenges, with United Way touching nearly a third of the population through various programs and services.
- Key issues include a large Medicare population, homelessness, and a complex web of disconnected social services that individuals in crisis are expected to navigate.

## What is 211?

- 211 is a social services directory and information helpline, similar to 911 for emergencies or 411 for information services.
- It helps individuals navigate the complex web of federally available social services, programs, and service providers.
- In Orange County, 211 handles over 1,100 service providers running over 3,000 programs.

## The Solution: Amazon Connect

- United Way of Orange County implemented Amazon Connect to improve the 211 call center operations and provide better care coordination.
- Amazon Connect offers features like omnichannel experiences, productivity enhancements, deep insights, and scalability.

### Key Improvements with Amazon Connect

1. **Reporting and Insights with Contact Lens**
   - Contact Lens provides sentiment analysis, trend detection, call summaries, and automated redaction of sensitive information.
   - Enables real-time flagging of critical client needs for supervisor assistance.

2. **Forecasting and Scheduling**
   - AI/ML-powered tool optimizes agent schedules, forecasts call volumes, and enables capacity planning.
   - Outcomes: Shorter wait times, reduced labor loads, improved hiring practices, and better customer and agent experience.

3. **Agent Performance Evaluation**
   - Automated scoring and evaluation of agent performance using conversational analytics.
   - Customizable evaluation forms and adherence monitoring.
   - Improved agent productivity and customer experience, reduced supervisor time for coaching and evaluating.

## The Architecture

- The solution leverages various AWS services, including Amazon Connect, Polly, Lex, Kinesis Video Streams, Transcribe, DynamoDB, S3, Glacier, QuickSight, and Lambda.
- It integrates with Salesforce CRM and a Postgres data warehouse for referral data management and analytics.
- The architecture is serverless, allowing for scalability and cost-efficiency based on usage.

## Results and Future

- The solution enables a more efficient and coordinated care journey for individuals, from crisis to a happy, healthy, and housed state.
- Visualization and analytics capabilities provide insights into the health of the ecosystem of care, referral outcomes, and program enrollments.
- Integration with the California Data Exchange Framework and potential replication across other United Ways.

## Key Takeaways

- Amazon Connect and related AWS services have transformed the 211 call center operations for United Way of Orange County.
- The solution provides improved care coordination, insights, forecasting, and agent performance evaluation.
- It enables a more efficient and data-driven approach to navigating the complex web of social services for individuals in need.