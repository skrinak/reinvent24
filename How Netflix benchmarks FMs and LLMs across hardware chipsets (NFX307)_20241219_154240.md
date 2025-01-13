# Summary of AWS re_Invent 2024 - How Netflix benchmarks FMs and LLMs across hardware chipsets (NFX307).txt

# Netflix's Approach to Benchmarking Foundation Models and Large Language Models

## Overview

- Netflix extensively utilizes machine learning algorithms and models for personalization and recommendation services, catering to its growing global subscriber base of around 300 million paid subscribers.
- With the increasing demand for accelerated computing and the transformative potential of generative AI (gen AI), Netflix is building custom, pre-trained, and fine-tuned models for AI-enabled services.
- Notable gen AI projects at Netflix include text-to-image generation, conversational-based search, real-time adaptive recommendations, and react-based search use cases.

## Benchmarking and Right-sizing Gen AI Workloads

- Netflix evaluates AWS instances using industry-standard benchmarks and production loads, integrated into their CI/CD platform and automated test harnesses.
- The process begins by determining the service accuracy, latency, and throughput requirements for a gen AI workload.
- Netflix then evaluates various foundation models, AWS instance sizes, types, and service stacks (e.g., NVIDIA Triton, TensorRT, TGI, vLLM) to identify the combination that delivers the best performance and scalability while meeting cost and budget constraints.
- This automated approach empowers service owners to make data-driven decisions on deployment costs, capacity requirements, and optimizing pre-scaling and auto-scaling targets.

## Key Factors in Benchmarking Foundation Models

- Model parameters, quantization, and the service stack play crucial roles in benchmarking foundation models.
- Model parameters (weights and activations) represent the learned knowledge and are important for ensuring accuracy in large language models (LLMs).
- Tokenizers and embeddings enable contextual understanding and efficient text generation when working with LLMs.
- Optimization techniques like mixed-precision or low-precision quantization (FP8, INT8, INT4, INT1) can optimize compute and memory requirements, depending on the accuracy requirements.
- Inference engines (e.g., TensorRT, vLLM) optimize model execution and hardware utilization.
- Inference servers (e.g., Triton, TGI) manage GPU resources, tensor parallelism, content batching, and LLM-based optimizations like Flash and page attention.

## AWS Foundation Model Benchmarking Tool (FMBench)

- FMBench is an open-source package for benchmarking any foundation model on any AWS generative AI service.
- It is model-agnostic and AWS service-agnostic, supporting models from various sources (Hugging Face, Meta, Anthropic, proprietary models).
- FMBench provides a unified configuration file for testing different combinations of models, instance types, inference servers, and engines.
- It generates detailed reports with metrics like inference latency, time to first/last token, transaction throughput, token throughput, and accuracy numbers.
- Key features include support for LongBench prompt dataset, extensive customization options, comprehensive inference engine and server support, and granular GPU server metrics.
- FMBench helps identify the right instance types and serving stack for a given workload, considering latency, cost, and throughput requirements.
- Netflix uses FMBench to benchmark LLM inference performance across AWS instances, ensuring scalability, latency, and throughput requirements are met for gen AI workloads.

## Getting Started with FMBench

- The FMBench orchestrator repository provides a companion tool for easy setup and configuration.
- Video guides, documentation, and the FMBench website are available for installation, configuration, and interpretation of reports.
- FMBench is an open-source project, and requests or issues can be submitted on GitHub or through LinkedIn.
- Future updates will include support for evaluating agentic workflows.