# Summary of AWS re_Invent 2024 - Scaling generative AI workloads with efficient model choice (AIM397-NEW).txt

# AWS re:Invent 2024 - Scaling Generative AI Workloads with Efficient Model Choice

## Overview

This session focused on three new features announced by AWS to help customers optimize and scale their generative AI workloads: intelligent prompt routing, model distillation, and Amazon Bedrock Marketplace. The speakers discussed the challenges customers face in balancing quality, cost, and speed when building generative AI applications, and how these features can help address those challenges.

## Key Points

### Intelligent Prompt Routing

- Allows customers to use a combination of foundational models for their application, routing each prompt to the most suitable model.
- Helps achieve better accuracy and lower cost than using a single foundational model.
- Announced in preview with two routers: Anthropic router (Claude Sonnet 3.5 and Claude Haiku) and Meta prompt router (Llama 8B and 70B models).
- Customers can define their own routing criteria based on acceptable response quality difference between models.

### Model Distillation

- Process of transferring knowledge from a larger "teacher" model to a smaller, more cost-efficient "student" model.
- Customers can use their own production data (invocation logs) or Bedrock's proprietary data synthesis techniques to generate diverse datasets for fine-tuning the student model.
- Demonstrated significant improvements in speed and cost savings with minimal accuracy loss compared to the teacher model.
- Available for Amazon, Anthropic, and Meta model families.

### Amazon Bedrock Marketplace

- Provides access to over 100 publicly available and proprietary models from over 30 providers.
- Includes models for various domains (finance, legal), languages (Asian, European), and specialized tasks (protein sequence generation, image generation, audio dubbing).
- Models can be accessed through Bedrock's simple APIs and tools (agents, knowledge bases, guardrails).
- Serverful offering with configurable instance types and autoscaling policies.
- Customers can fine-tune compatible models and import them into Bedrock.

## Customer Use Cases

- Robin AI: Used model distillation to achieve 98% accuracy of the teacher model with 66% cost savings and faster inference for their legal AI application.
- Zendesk: Integrating Widn's high-performance model for multilingual translation and redaction of sensitive information.
- South Korean newspaper: Improved proofreading accuracy by 57.9% using Upstage's Solar models, aiming for 95% error detection and correction.
- Sony Group: Deploying an enterprise LLM platform with over 70 models from Bedrock, including domain-specific, small language, and lightweight models for various use cases across their business units.

## Conclusion

The new features announced by AWS aim to provide customers with more efficient and cost-effective ways to scale their generative AI workloads. Intelligent prompt routing and model distillation enable optimizing for quality, cost, and speed, while the Bedrock Marketplace offers a wide range of models for diverse use cases and domains.