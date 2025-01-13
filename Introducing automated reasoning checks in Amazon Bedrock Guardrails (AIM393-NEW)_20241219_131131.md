# Summary of AWS re_Invent 2024- Introducing automated reasoning checks in Amazon Bedrock Guardrails (AIM393-NEW).txt

# Summary of AWS re:Invent 2024 - Introducing Automated Reasoning Checks in Amazon Bedrock Guardrails

## Introduction

- Stefano, a product manager at AWS, and Byron, a distinguished scientist in the automated reasoning group, presented this session.
- The session aimed to introduce automated reasoning checks, a new feature in Amazon Bedrock Guardrails, and explain how it can help build accurate and responsible AI applications.

## Background and Motivation

- Generative AI and large language models (LLMs) have shown immense potential in various use cases, such as onboarding new employees, customer support, and automating complex decisions.
- However, a major concern with LLMs is the presence of hallucinations, where the model generates factually inaccurate or inconsistent information.
- While hallucinations can be desirable for creativity, they pose a problem when accuracy matters, such as in customer-facing applications.
- The industry is increasingly recognizing the need to address hallucinations and combine different AI techniques, such as machine learning and automated reasoning (symbolic AI), leading to the rise of neuro-symbolic AI.

## What is Automated Reasoning?

- Automated reasoning, also known as symbolic AI or formal verification, is rooted in mathematical logic and aims to reason accurately about infinite or intractably large sets of data.
- It allows proving properties about programs or models in a finite series of steps, even when the domain is infinite, which is impossible to test exhaustively.
- Automated reasoning has been used at AWS for over 10 years in various services, such as AWS Config Rules, Inspector, VPC Reachability Analyzer, S3 Block Public Access, IAM Access Analyzer, and more.
- It is also used to prove the correctness of AWS's internal programs, cryptographic foundations, and other critical components.

## Automated Reasoning Checks in Bedrock Guardrails

- Automated reasoning checks is a new feature in Amazon Bedrock Guardrails that helps identify, correct, and explain the factual accuracy of LLM responses.
- It works by creating an automated reasoning policy, a structured mathematical representation of your knowledge, such as corporate policies, laws, regulations, or operational workflows.
- Bedrock Guardrails can then use this policy to validate incoming questions and answers against the formalized knowledge.
- The process involves three steps:
  1. Create an automated reasoning policy by uploading relevant documents and refining the extracted rules and variable schemas.
  2. Configure Bedrock Guardrails to use the automated reasoning policy for validation.
  3. Use the validated Q&A in production applications.

## Key Benefits and Objectives

- Accuracy: Automated reasoning checks help ensure that factual claims made by LLMs are accurate and consistent with the formalized knowledge.
- Soundness: If a validity claim cannot be made, the system will indicate that it does not understand, rather than making an incorrect claim.
- Transparency: The system provides an auditable log of the reasoning and explanations behind the validation decisions, promoting transparency and explainability.

## Next Steps

- Learn more about automated reasoning by reading the "Gentle Introduction to Automated Reasoning" blog post.
- Explore Bedrock Guardrails and automated reasoning checks documentation.
- Join the gated preview by reaching out to AWS account teams.

Overall, the session introduced automated reasoning checks as a powerful tool to build accurate, sound, and transparent AI applications by combining the strengths of large language models and formal reasoning techniques.