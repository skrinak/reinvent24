# Summary of AWS re_Invent 2024 - Getting better image analysis with generative AI (AES307).txt

# Summary: Getting Better Image Analysis with Generative AI

## Introduction

- Chris Wise (Solutions Architect Manager) and Joy Fasnacht (Principal Solutions Architect) from the AWS aerospace and satellite team presented on prompt engineering for better image analysis using generative AI.
- The focus was on understanding how to structure prompts for image analysis tasks using Bedrock and the Amazon Claude 3.5 model.

## Prompt Engineering

### What is Prompt Engineering?

Prompt engineering is the key to interacting with generative AI models effectively. It involves:

- **Context**: The business case, background information, and relevant constraints.
- **Role**: The perspective or role the model should take when analyzing the data.
- **Instructions**: Clear and concise directions for the specific task.
- **Constraints**: Limitations or guidelines for the model's output (e.g., size, format).
- **Input Data**: The specific data or metrics for the model to analyze.
- **Output Format**: How the output should be organized and presented.

### Example Prompt Structure

An example prompt structure for a technology copywriter was provided:

**Context**: Your role is a technology copywriter for CosmosNet Solutions, a pioneering company specializing in satellite-based internet.

**Instructions**: Write a promotional blog to introduce the GlobalConnect service to potential customers.

**Input Data**: Company information, service details, monthly cost.

**Output Format**: Attention-grabbing headlines, introduction paragraphs, 3-4 bullet points.

**Constraints**: 400-500 words, professional yet exciting tone, avoid technical jargon.

## Image Analysis Demo

Joy Fasnacht demonstrated how prompt refinement with Bedrock can improve image analysis results using satellite imagery.

### Base Case

With no prompt provided, the model gave a detailed but generic description of the satellite image (coastal area, vegetation, structures, roads).

### Refined Prompt 1

By providing context (role as a satellite imagery analyst), instructions (analyze the area, predict impact of a 10-foot storm surge), and output format (5 paragraphs for urban planning), the model's output became more focused and relevant.

### Refined Prompt 2

Additional constraints were added, such as warning if cloud cover exceeds 25% and considering digital elevation models for accurate predictions. The model estimated the cloud cover, warned about human validation, and suggested using elevation data.

## Conclusion

- Prompt engineering is crucial for effective image analysis with generative AI models.
- By refining prompts with context, roles, instructions, constraints, and output formats, the quality and relevance of the model's output can be significantly improved.
- AWS Bedrock and the Amazon Claude 3.5 model were used for the demonstrations, but the principles can be applied to other models and use cases.

## Resources

- AWS Bedrock documentation (QR code provided)
- GitHub repository with Bedrock sample code, including the image analysis demo (QR code provided)