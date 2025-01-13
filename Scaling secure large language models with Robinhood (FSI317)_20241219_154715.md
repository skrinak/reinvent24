# Summary of AWS re_Invent 2024 - Scaling secure large language models with Robinhood (FSI317).txt

# Scaling Secure Large Language Models with Robinhood

## Introduction

- Presentation by Dolly, a mission learning engineer at Robinhood, and Trevor Spiers, a solutions architect at AWS.
- Discusses Robinhood's journey in scaling Large Language Models (LLMs) reliably and securely using AWS Bedrock.
- Covers design iterations, architecture, and tools built for secure LLM inference.

## Robinhood's AI Platform Mission

- Empower developers with powerful AI and ML abstractions.
- Support power users with advanced tools.
- Streamline the journey from experimentation to production.
- Enable rapid adoption of state-of-the-art Gen AI technologies.

## Use Case: Fraud Investigation

- Over 80 fraud investigation agents write 300+ case conclusions daily.
- Maintaining consistency and quality in narratives was a challenge.
- Implemented a solution using AWS Bedrock's Provisioned Throughput Mode and the Claude Sonnet model.
- Model generates a structured draft conclusion from raw notes and form details in seconds.
- Safeguards implemented to prevent misuse, including click limits and feedback loop.

## Challenges with Provisioned Throughput Mode

- Scalability issues: Predicting traffic patterns months in advance and handling bursts.
- Noisy neighbor problem: One team's high consumption affecting others.
- Delayed access to new models and limited model variety.
- Cost constraints and six-month commitment period.

## Transition to On-Demand API

- Moved to AWS Bedrock's On-Demand API for greater flexibility and scalability.
- Leveraged cross-region inference for doubled throughput and increased resilience.
- Seamless transition without affecting client traffic using LLM Gateway.

## LLM Gateway

- Compatible with various SDKs (OpenAI, Anthropic, open-source).
- Validates input parameters and logs requests/responses for auditing.
- Includes a PII reduction service for data privacy compliance.
- Supports fallback models for high availability and continuity.
- Facilitates continuous model evaluation and cost management.

## Goals for 2025

- Introduce built-in tools for model and prompt analysis.
- Centralize AI data governance for consistency and compliance.
- Enhance gateway for dynamic model routing and fine-tuning options.
- Roll out batch inference pipelines for large-scale tasks.
- Provide a prompt playground for experimentation and testing.

## Conclusion

- Presentation highlights Robinhood's journey in scaling LLMs securely and reliably.
- Covers design iterations, architecture, and tools like the LLM Gateway.
- Emphasizes the importance of flexibility, scalability, and security in LLM inference.