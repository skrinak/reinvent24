# Summary of AWS re_Invent 2024 - Avoid turbulence_ Driving an airline notification service switch (DEV210).txt

# Summary: Avoiding Turbulence in an Airline Notification Service Migration to AWS

## Introduction
- The talk focuses on the leadership principles applied to migrate an airline's notification service from a mainframe to AWS Cloud.
- The speaker discusses the challenges faced during the project and how the AWS community helped overcome them.

## Background
- Airlines use a Passenger Name Record (PNR) code containing flight details, passenger information, and contact details.
- The airline (referred to as "Unicorn Airlines") was using a passenger service system from the 1960s and a 20-year-old notification service, considered legacy technology.
- The existing setup involved a corporate data center connected to AWS Cloud via Direct Connect, with PNR numbers processed through SQS, Lambda, and stored in a database for analytics and notifications.

## Challenges
- Renaming a folder caused issues with Terraform deployment.
- Unmerged branches from previous engineers led to confusion.
- Lack of communication between teams slowed progress.
- Too many meetings hindered development work.
- Business pressure to meet deadlines.

## Leadership Principles Applied
- **Customer Obsession**: Treat the project as the customer, prioritizing its success.
- **Ownership**: Bought a share in the company to understand business pressure.
- **Invent and Simplify**: Reused existing code and simplified over-engineering to improve collaboration.
- **Have Backbone, Disagree and Commit**: Questioned decisions with facts and information, considering security implications.
- **Frugality**: Simplified architecture, removed redundant components, and leveraged spot instances to reduce costs.
- **Deliver Results**: Focused on delivering results rather than perfection, following the "done is better than perfect" principle.

## AWS Community Support
- Leveraged the AWS Community Builders and User Groups for assistance.
- Consulted community members for specific services and architecture improvements.
- Community members helped test SMS delivery in different countries.
- The community provided personal support and motivation during challenging times.

## Conclusion
- The speaker encourages joining local AWS User Groups and engaging with the community.
- Connecting with the speaker on LinkedIn and joining AWS User Groups Moldova and AWS Community Builders is recommended.