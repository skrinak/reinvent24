# Summary of AWS re_Invent 2024 - Improve clinical trial coverage analysis with generative AI (HLS212).txt

# Summary: Improving Clinical Trial Coverage Analysis with Generative AI

## Introduction

- Huron Consulting is a global consulting company that helps clients solve problems across various industries, including healthcare.
- The presentation focuses on how Huron used an enterprise-wide innovation challenge to transform their managed services through digital transformation, specifically in the area of opening clinical trials faster.

## Background: Clinical Trials and Coverage Analysis

- Opening a clinical trial is a crucial step in developing new treatments and vaccines, such as the COVID-19 vaccine during the pandemic.
- Coverage analysis is a complex process that involves understanding scientific protocols, patient care, and billing guidelines.
- It requires expertise in multiple domains and is repetitive, difficult, and has an intense decision tree process.

## The Challenge

- The challenge was to develop a solution that could automate and streamline the coverage analysis process by querying complex documents, asking difficult questions, and presenting the results in a shareable format.
- The solution had to work within the constraints of a finite audience, limited budget, and without a dedicated AI team.

## The Solution

### Backend Ingestion Process

- Amazon Bedrock Knowledge was used for document ingestion and querying.
- Filters were introduced to ensure that answers came from relevant documents for a specific clinical trial.

### Frontend and User Interface

- Instead of a chat UI, Smartsheets (an online spreadsheet platform) was chosen as the frontend.
- Templates were created in Smartsheets, which could be instantiated for each clinical review.
- Users could attach relevant documents, and the answers would be populated in the spreadsheet columns next to the questions.

## Challenges and Enhancements

### Handling Complex Schedules of Activities

- 65% of the schedules of activities (complex tables detailing clinical trial steps) had different formats and structures.
- A custom, advanced parser was developed to comprehend and preserve the integrity of these tables for the language model.

### Navigating Complex Decisions

- Coverage analysis involves making thousands of interdependent decisions for each procedure and time point.
- An AI agent framework was implemented to break down the problem into smaller, manageable components handled by specialized agents.
- This approach aimed to improve accuracy and consistency in decision-making.

## Benefits and Future Outlook

- The solution has increased efficiency by streamlining documentation workflows and reducing time spent on repetitive tasks.
- Improved accuracy allows for proactive identification of alternate procedures, minimizing the need for rework.
- The team is encouraged by the results and plans to continue improving the solution to support clinical trials that patients depend on.
- They look forward to learning more about technologies and best practices in this field.