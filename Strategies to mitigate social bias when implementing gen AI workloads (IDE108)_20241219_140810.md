# Summary of AWS re_Invent 2024 - Strategies to mitigate social bias when implementing gen AI workloads (IDE108).txt

# Summary

## Introduction

- The session discusses strategies to mitigate social bias when implementing generative AI (gen AI) workloads.
- Bias can manifest in various forms, from training data to algorithms, and can have consequences on individuals and communities.
- The presenters, Liza Ogwel and Monika, explore AWS services like Amazon Bedrock Guardrails, SageMaker Clarify, and SageMaker Data Wrangler designed to help identify and mitigate biases in machine learning models and data.

## Types of Bias

### Sample Bias
- Occurs when the training data is not representative of the diverse population the AI system interacts with.
- Mitigation: Curate training data from diverse sources and ensure adequate representation of different groups, cultures, and perspectives.

### Historical Bias
- Manifests when the training data reflects societal biases and discriminatory practices from the past.
- Mitigation: Critically examine training data, identify potential biases, and incorporate de-biasing techniques during training and deployment.

### Measurement Bias
- Arises when the evaluation metrics used to assess the performance of gen AI systems fail to capture important aspects of fairness.
- Mitigation: Develop comprehensive evaluation frameworks that incorporate measures of fairness, accountability, and ethical considerations.

## Impact of Bias on Society
- Reinforcing harmful stereotypes and discrimination
- Perpetuating discrimination in employment, housing, education, and healthcare
- Contributing to the spread of misinformation and false narratives
- Leading to polarization and suppressing alternative perspectives

## Strategies for Bias Detection and Mitigation

### Sourcing Training Data Broadly and Responsibly
- Ensure training data is representative of different demographic groups, age groups, genders, ethnicities, and nationalities.
- Involve subject matter experts to assess data quality and balance.
- Include data from diverse sources, including non-English language contexts.
- Use automated services like SageMaker Data Wrangler to identify and mitigate data imbalances.

### Interdisciplinary Collaboration
- Involve people with different specializations, such as machine learning, cybersecurity, social sciences, ethics, and law.
- Conduct threat modeling during the design phase to detect and mitigate security risks.
- Develop AI governance strategies to dictate the appropriate use of gen AI tooling.

### Model Evaluation
- Use SageMaker Clarify to evaluate the trained model in a test environment before moving to production.
- Conduct automated and human evaluations to assess model performance, bias, and stereotyping.
- Leverage SageMaker Model Monitor to monitor the production model for any divergence in bias.

### Filtering Output to Mitigate Discriminatory and Biased Content
- Use Amazon Bedrock Guardrails to set up preventative controls based on the organization's AI governance strategy.
- Configure Guardrails to deny specific topics, filter out offensive language, and reduce the risk of sensitive data exposure.
- Evaluate user input and foundational model output against the configured Guardrails.

## Conclusion
- The presenters provide QR codes for resources on SageMaker Data Wrangler, SageMaker Clarify, and Amazon Bedrock Guardrails to help attendees get started with mitigating bias in gen AI workloads.