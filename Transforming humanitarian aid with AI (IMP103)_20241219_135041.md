# Summary of AWS re_Invent 2024 - Transforming humanitarian aid with AI (IMP103).txt

Here is a comprehensive summary of the transcript, formatted in Markdown with appropriate headers and bullet points:

# AWS re:Invent 2024 - Transforming Humanitarian Aid with AI

## Introduction

- Sandra, the lead for AI for Good at AWS Social Responsibility and Impact (SRI) team, introduced the session and the importance of ensuring that the benefits of AI are distributed equitably.
- She emphasized the need for collaboration across companies, industries, and countries to solve complex global challenges.

## Tech To The Rescue (TTTR)

### Overview

- Jacek Siadkowski, CEO of TTTR, shared the origin story of the organization, which started during the COVID-19 pandemic.
- TTTR connects tech companies with non-profits, enabling the companies to provide pro bono services to build solutions for social impact.
- The organization has grown to 1,800 tech companies working in 60 countries.

### AI for Changemakers Program

- TTTR, in partnership with AWS and Google.org, launched the AI for Changemakers program to support 100 outstanding organizations.
- The program provides access to:
  - World-class designers to identify AI use cases and build AI strategies
  - Hundreds of companies ready to build AI solutions pro bono
  - AWS credits, mentors, and potential funding opportunities

### Barriers to AI Adoption in the Social Sector

- Talent shortage and limited funding for AI in the non-profit space are significant barriers.
- Non-profits often lack the capacity to innovate, build datasets, and test prototypes.
- Securing funding requires working prototypes, creating a catch-22 situation.

## Mercy Corps

### Overview

- Alicia Morrison, Interim Senior Director for Technology for Development at Mercy Corps, introduced the organization's mission and global reach.
- Mercy Corps aims to help people build secure, just, and productive communities by alleviating poverty, suffering, and oppression.

### AI Methods Matcher

- The AI Methods Matcher is a chatbot that serves curated reports and resources to help humanitarian personnel explore how their peers have successfully used analytical tools to benefit their programs.
- The solution aims to foster cross-pollination of ideas and methods across teams and programs.

### Solution Architecture

- The solution uses a retrieval-augmented generation strategy with a vector database (Milvus) and a curated S3 bucket of resources.
- It leverages the Cloudera Data Platform, Cloudera AI Inference Service, and the Mistral 7B Instruct model.
- The architecture includes a Flask application and an Angular front-end, hosted on Amazon Elastic Kubernetes Service.

### Challenges and Advice

- Capacity constraints, legacy systems, and underinvestment in data systems are significant barriers for non-profits.
- Alicia advised looking at pain points and addressing them with proven technologies, rather than chasing the latest trends.
- She encouraged tech companies to support non-profits by providing capacity and cushion for innovation.

## ACAPS and SOPHIA

### Overview

- Yevhen Barshchevskyi, Data Solutions Team Lead at ACAPS, introduced the organization's mission as an independent information service provider in the humanitarian sector.
- ACAPS provides data sets and ad hoc analytics to inform aid distribution and decision-making.

### SOPHIA (Solutions Platform for Humanitarian Information Analysis)

- SOPHIA is a SaaS product that allows analytical staff to monitor crises in real-time.
- It uses AWS technologies like Lambda, Sagemaker, and S3 to scrape, translate, and classify information from various sources.
- SOPHIA supports over 70 languages and aims to prioritize signals from noise.

### Solution Architecture

- SOPHIA is built on a serverless architecture, leveraging AWS Lambda, Sagemaker, S3, and Amplify.
- It incorporates a GenAI module using a retrieval-augmented generation (RAG) approach.

### Challenges and Advice

- Yevhen emphasized the importance of user-centric design and understanding the problem before chasing technology solutions.
- He advised demystifying AI, understanding its advantages and limitations, and identifying the right technology for specific use cases.
- ACAPS found value in traditional machine learning for document recommendation and risk forecasting, in addition to exploring GenAI for critical analysis.

## Closing Thoughts and Call to Action

- The panelists discussed the potential of AI as a multiplier, both amplifying existing inequalities and bridging gaps through collaborative efforts.
- Alicia called for tech companies to seek out organizations like TTTR and lend their resources and capacity to non-profits for AI innovation.
- Jacek expressed excitement about the cultural shift towards building solutions for good, with more companies embracing pro bono projects.
- The panelists encouraged the audience to "go build" and engage with the solutions presented.