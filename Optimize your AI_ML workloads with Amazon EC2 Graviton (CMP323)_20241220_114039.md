# Summary of AWS re_Invent 2024 - Optimize your AI_ML workloads with Amazon EC2 Graviton (CMP323).txt

Here is a comprehensive summary of the transcript, formatted in Markdown with appropriate headers and bullet points:

# AWS re:Invent 2024 - Optimize your AI/ML workloads with Amazon EC2 Graviton

## Introduction

- AWS Graviton is a general-purpose CPU that delivers up to 40% better price performance for AI/ML workloads.
- The cloud provides a broad and deep portfolio of AI/ML services and infrastructure, allowing you to choose the right tool for the job.
- AI/ML workloads involve a continuum of compute, ranging from CPUs to purpose-built accelerators like AWS Trainium and Inferentia.

## AWS Graviton: Evolution and Performance

- Graviton has been around for six years, with four generations delivering 4X performance improvements.
- Graviton3 introduced hardware innovations like:
  - Doubled SIMD engine width with SVE
  - Native Bfloat16 data type
  - Larger branch predictor
  - DDR5 memory support
- Graviton4 builds on Graviton3 with:
  - 96 cores (up from 64 in Graviton3)
  - Two-socket capable (up to 192 CPUs)
  - Neoverse V2 cores
  - Doubled L2 cache size
  - DDR5-5600 memory support
  - PCIe Gen5 connectivity

### Customer Examples

- Sprinklr achieved 20% throughput improvement, 30% latency reduction, and up to 30% cost reduction with Graviton3.
- Databricks saw up to 3.5X better price performance with their Photon query engine on Graviton.

## ML Framework Optimizations

- AWS has optimized popular ML frameworks like PyTorch, TensorFlow, and JAX for Graviton.
- Optimizations include:
  - SVE and Bfloat16 support
  - Operator fusion and caching
  - Transparent Huge Pages
  - Optimized math libraries (oneDNN, OpenBLAS)
- These optimizations deliver up to 3.5X performance improvements on Graviton.

## Generative AI Inference

- Graviton instances can run large language models like Llama 7B on a single node, meeting latency requirements.
- Vector databases are crucial for retrieval-augmented generation and benefit from Graviton's improved memory bandwidth and L2 cache.

## Data Ingestion and Preparation

- Challenges include maintaining data quality, compliance, and unbiased representation while optimizing resource utilization and reducing carbon footprint.
- Graviton instances excel at data ingestion, preparation, and processing tasks, enabling faster iteration and experimentation.

### Anthropic's Experience

- Anthropic has moved a significant portion of their data processing pipeline to Graviton, achieving:
  - 20% per-core cost savings
  - 30% less power usage per core
  - Improved thermal performance
  - Faster data deduplication and filtering
  - Easier adoption of optimizations like SVE and THP

## When to Use Graviton for AI/ML

- Generative AI text generation with models up to 70B parameters
- Data ingestion and preparation
- Vector databases for retrieval-augmented generation
- Classical AI/ML workloads like NLP, classification, ranking, and clustering

## Call to Action

- Examine your AI/ML pipelines and identify workloads that can run on CPUs instead of accelerators.
- Evaluate the price performance of Graviton instances for your specific workloads.
- Leverage the optimized ML framework support on Graviton for seamless integration.
- Experiment and evaluate Graviton instances to potentially achieve significant cost savings.