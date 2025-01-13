# Summary of AWS re_Invent 2024 - Build multimodal ASL avatars with bidirectional translation (DEV306).txt

# Summary

## Introduction

- The session discusses building multimodal American Sign Language (ASL) avatars with bidirectional translation capabilities using generative AI.
- It aims to address the challenges faced by Deaf and hard-of-hearing individuals in accessing multimedia content and engaging in conversations.

## Sign Language Avatars

### Narrative Avatar
- A digital human that can translate audio content into a sign language video in real-time.

### Conversational Avatar
- Enables Deaf and hard-of-hearing users to have natural conversations with an avatar, which responds in sign language.
- Facilitates conversations between Deaf/hard-of-hearing users and hearing users, acting as an interpreter.

## Solution Overview

### Sign Language Video Generation
1. Convert English audio to text using Amazon Transcribe.
2. Convert English text to ASL Gloss using Anthropic's Claude 3.5 Sonnet V2.
3. Generate raw ASL avatar video from ASL Gloss using Stable Diffusion models.
4. Smooth the raw video using a SmoothNet machine learning model.

### Video Detection (Reverse Direction)
1. Convert ASL video input to English text using Meta's Llama 3.2 Vision Instruct 11B (fine-tuned).
2. Convert English text to audio using Amazon Polly.

## Multimodal AI

- Multimodal AI can process and understand multiple types of information (images, text, speech, video) simultaneously.
- Benefits include better context understanding and performing a wider range of tasks.
- Challenges include data availability, compute-intensive, and expensive.

## Customizing Foundational Models

- Prompt engineering
- Retrieval-augmented generation
- Fine-tuning
- Continued pre-training

## Architecture and Best Practices

- Decoupled architecture with separate steps for each task.
- Use of AWS services like Amplify, API Gateway, Bedrock, and SageMaker.
- Best practices for live streaming, prompt management, cross-region inference, and security.

## Future Directions

- Adding multilingual support for other sign languages.
- Moving towards unified multimodal models for improved accuracy, quality, and context understanding.

## Conclusion

- The session demonstrated the potential of generative AI in building accessible and inclusive solutions for Deaf and hard-of-hearing individuals.
- It highlighted the architecture, best practices, and future directions for developing multimodal ASL avatars with bidirectional translation capabilities.