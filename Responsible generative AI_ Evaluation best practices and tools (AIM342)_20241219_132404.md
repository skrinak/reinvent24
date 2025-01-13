# Summary of AWS re_Invent 2024 - Responsible generative AI_ Evaluation best practices and tools (AIM342).txt

# AWS re:Invent 2024 - Responsible Generative AI: Evaluation Best Practices and Tools

## Summary

### Introduction

- Generative AI has immense potential but also introduces new risks and considerations for responsible adoption.
- Classical machine learning models often involve point predictions with full control over data and architecture, while Generative AI deals with unstructured data and relies on large foundation models trained on vast datasets.
- As Generative AI applications increase in complexity, involving multiple models and components, comprehensive evaluation throughout the lifecycle becomes crucial to mitigate risks and ensure responsible deployment.

### Evaluation Plan and Dimensions

- Develop an evaluation plan by understanding the application's purpose, inherent risks, and creating a risk assessment.
- Evaluate across four dimensions: quality/accuracy, latency, cost, and confidence (responsible AI considerations).
- The Responsible AI framework organizes evaluation into eight pillars: accountability, fairness, privacy, robustness, safety, security, transparency, and value alignment.

### Evaluation Architecture and Tools

- Access models, data, and input engineering components for evaluation.
- Use a combination of human evaluation, heuristic metrics (standard NLP tools), and LLM-as-a-judge (Generative AI models for evaluation).
- Utilize tools like Amazon Bedrock Model Evaluation, SageMaker Evaluation, and open-source packages for automatic evaluation.
- Perform component analysis (unit testing) and end-to-end evaluation (integration testing) across the application lifecycle.

### Evaluating Large Language Models (LLMs)

- Leverage public benchmarks and datasets for initial model selection, but evaluate on representative customer data.
- Measure latency, throughput, and performance using AWS tools like Bedrock Model Evaluation and SageMaker Evaluation.
- Assess performance across dimensions like veracity, robustness, privacy, security, safety (toxicity), and fairness.

### Establishing Launch Confidence

- Define the specific use case and target domain to assess potential risks accurately.
- Choose relevant metrics to measure identified risks, considering responsible AI dimensions.
- Set release criteria based on the risk matrix (severity and likelihood) and maximum acceptable rates.
- Design a representative evaluation dataset reflecting the target use case and domain.
- Generate metrics using tools like Bedrock Model Evaluation and interpret results with confidence intervals and hypothesis testing.
- Measure disparity across demographic groups and establish joint confidence in meeting release criteria.
- Communicate evaluation results and considerations through transparency reports and AWS AI Service Cards.

### Mitigation and Continuous Evaluation

- If not confident in release, identify sources of low confidence and implement mitigation methods like input/output filtering (e.g., Amazon Bedrock Guardrails).
- Re-evaluate the system after mitigation, considering overall quality, latency, and cost impacts.
- Continuously evaluate and monitor the system throughout its lifecycle, as data and domains may drift over time.

## Key Insights and Conclusions

- Responsible adoption of Generative AI requires comprehensive evaluation across multiple dimensions, including responsible AI considerations like fairness, safety, and privacy.
- Evaluation should be an ongoing process throughout the application lifecycle, from development to production monitoring.
- Defining the specific use case and target domain is crucial for accurate risk assessment and representative evaluation datasets.
- Interpretation of evaluation results should capture uncertainty through confidence intervals, hypothesis testing, and joint confidence measures across demographic groups.
- Transparency reports and AI Service Cards can communicate evaluation results and considerations, building customer trust.
- Mitigation methods like input/output filtering may be necessary if release criteria are not met, followed by re-evaluation of the mitigated system.
- AWS provides tools and frameworks to support responsible Generative AI evaluation, such as Bedrock Model Evaluation, SageMaker Evaluation, and Responsible AI guidelines.