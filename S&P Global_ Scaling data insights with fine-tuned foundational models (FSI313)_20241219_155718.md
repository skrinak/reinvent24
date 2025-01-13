# Summary of AWS re_Invent 2024 - S&P Global_ Scaling data insights with fine-tuned foundational models (FSI313).txt

# AWS re:Invent 2024 - S&P Global: Scaling Data Insights with Fine-tuned Foundational Models

## Summary

### Introduction

- The session covered how S&P Global leveraged fine-tuned foundational models (LLMs) using Amazon SageMaker, deployed on Amazon EKS, to handle millions of inferences per week while optimizing cost efficiency.
- Customers build generative AI solutions on top of their data foundation, following different approaches like prompt engineering, retrieval augmented generation, fine-tuning, or continued pre-training.
- S&P Global chose fine-tuned foundational models as the design pattern to solve their complex business problem.

### Business Use Case

- S&P Global deals with a vast amount of data, and their ratings business relies on financial analysis for credit ratings.
- However, assessing credit risk for private companies (SMEs) is challenging due to the lack of publicly available financial information.
- To overcome this, S&P Global looks for alternative signals, such as management changes, payment history, legal filings, and textual footprints from company websites.
- The goal is to provide real-time credit assessments and risk gauges for millions of private companies, enabling customers to make informed decisions.

### Technical Approach

- S&P Global leverages natural language processing (NLP) to collect data from documents and web pages.
- They create a domain graph for each company, identifying relevant child pages and sections with credit risk signals.
- Fine-tuned LLMs are used for complex classification and extraction tasks, such as identifying business activities and risk signals.
- Parameter-efficient fine-tuning methods like LoRA (Low-Rank Adaptation) are employed, reducing computational requirements and model size.
- A self-grading pipeline with larger LLMs is used to create training data for fine-tuning the smaller models.
- Amazon SageMaker is utilized for fine-tuning the LLMs, with careful prompt engineering and output shaping.
- The models are converted to run on CPUs using the LLAMA C++ library for cost optimization.
- The architecture involves worker pods in Amazon EKS, orchestrated by Amazon Managed Workflows for Apache Airflow, and leverages Redis for queue management.

### Lessons Learned

- Start simple with smaller LLMs and gradually increase complexity if needed.
- Parameter-efficient fine-tuning methods mitigate overfitting and catastrophic forgetting risks.
- Compare the performance and cost trade-offs between CPU and GPU inference for specific use cases.
- Break down prompts into smaller pieces for better performance with LLMs.
- Leverage existing prompt templates and limit output token lengths for better control over LLM outputs.

### Conclusion

- The session showcased S&P Global's innovative approach to leveraging fine-tuned foundational models for real-time credit risk assessments of private companies.
- Their distributed architecture, leveraging AWS services like SageMaker, EKS, and Airflow, enabled scalability and cost optimization.
- The lessons learned provide valuable insights for organizations exploring generative AI solutions with LLMs.