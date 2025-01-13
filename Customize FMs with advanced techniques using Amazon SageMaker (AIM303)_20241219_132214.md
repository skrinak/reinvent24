# Summary of AWS re_Invent 2024 - Customize FMs with advanced techniques using Amazon SageMaker (AIM303).txt

Here is a comprehensive summary of the transcript in Markdown format:

# AWS re:Invent 2024 - Customize FMs with advanced techniques using Amazon SageMaker (AIM303)

## Introduction

- The session covers when and how to fine-tune foundation models (FMs) using Amazon SageMaker.
- Fine-tuning FMs can improve accuracy, reduce costs, and enhance performance for specific use cases.

## When to Fine-tune FMs

- To improve accuracy for a specific domain, function, or business
- To reduce costs for inference at scale while maintaining accuracy
- For latency-sensitive use cases where smaller models are required

## Prerequisites for Fine-tuning

- Having a unique and differentiated dataset not part of the original training corpus (e.g., customer data, internal documentation)
- Common starting points: customer service, support use cases

## Fine-tuning Process

1. **Data Preparation**
   - Domain adaptation: Providing documents for the model to learn the domain
   - Instruction tuning: Providing question-answer pairs to train the model
   - Visual Q&A: Adding images along with question-answer pairs
   - Often, hundreds or fewer examples can lead to meaningful improvements

2. **Model Selection and Configuration**
   - SageMaker provides hundreds of pre-trained FMs that can be fine-tuned
   - Customize hyperparameters like quantization, FSDP, and LoRA adapters

3. **Training and Deployment**
   - Use SageMaker Jumpstart (UI) or SageMaker Training (programmatic) for fine-tuning
   - SageMaker packages the fine-tuned model for deployment
   - Deploy on SageMaker or import into Amazon Bedrock for Bedrock workflows

## Demo: Fine-tuning on SageMaker

- Demonstrated fine-tuning a Llama 3.2 Vision model for document understanding and question answering
- Showed the process using SageMaker Studio UI and Python SDK
- Highlighted the improved accuracy of the fine-tuned model compared to the pre-trained model

## Intuit's Use Case: Transaction Categorization

- QuickBooks categorizes transactions for small businesses to generate financial reports
- Traditional ML models had accuracy limitations and operational complexity (maintaining millions of personalized models)
- Fine-tuned LLMs showed 5-10% accuracy improvement with fewer samples
- Potential to replace millions of personalized models, reducing operational complexity
- SageMaker enabled rapid experimentation and evaluation of multiple models
- Hybrid approach: Existing solution first, then fine-tuned model for low-confidence cases

## Key Learnings

- Large datasets (thousands of samples) were required for this use case due to variability in accounting practices
- Synthetic data didn't help; real customer data was needed for broad coverage
- Fine-tuning enabled managing accuracy, latency, and scale for the customer experience
- Rapid experimentation approach allowed quick learning, pivoting, and refining ideas
- Paves the way for task-specific fine-tuning at Intuit in the future