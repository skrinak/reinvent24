# Summary of AWS re_Invent 2024 - Introduction to prompt engineering (TNC101).txt

# AWS re:Invent 2024 - Introduction to Prompt Engineering

## Summary

### Introduction to Generative AI and Foundational Models

- Generative AI technology can be used to create new content, such as generating images, stories, or summarizing content from news articles or emails.
- Foundational models use deep neural networks to emulate human brain functionality and handle complex tasks like text generation, image creation, and chatbot applications.
- Foundational models are trained on large, unlabeled datasets and can be used for general tasks like text summarization or question answering.
- The training process for foundational models involves three stages:
  1. Pre-training: Self-supervised learning to capture context from trillions of words.
  2. Fine-tuning: Using your own data to train the model for specific use cases.
  3. Prompt engineering: Optimizing the input prompts to influence the model's output.

### Large Language Models (LLMs)

- LLMs are a subset of text-to-text foundational models used for tasks like chatbots, text summarization, and code generation.
- LLMs use transformer architectures to convert text inputs into numbers, identify similar words/numbers, and convert the output back to text.
- Key components of LLM architectures:
  - Embedding layer: Converts text into numbers.
  - Feedforward layer: Assigns weights to find similar words/numbers.
  - Attention mechanism: Focuses on the relevant context of the input text.
- Use cases for LLMs include chatbots, code generation, enhancing creativity, and process optimization.

### Prompt Engineering Concepts

- Prompt engineering optimizes the input prompts given to LLMs or foundational models, without retraining the model.
- Key elements of a prompt:
  - Instructions: The task or question to be answered.
  - Context: Background information or data relevant to the task.
  - Input data: Additional information to influence the output.
  - Output indicator: The desired format or type of output.
- Best practices for effective prompts:
  - Be clear and concise.
  - Include context when needed.
  - Use directiveness for desired response types.
  - Consider the output format in the prompt.
  - Start with questions (what, who, why, when, how).
  - Provide example responses.
  - Break down complex questions into smaller steps.
  - Experiment with different models and prompts.

### Prompt Techniques

- Zero-shot prompting: Providing a question without any context or examples.
- Few-shot prompting: Providing context, examples, and desired outputs in the prompt.
- Chain of thought prompting: Breaking down complex questions into smaller steps, referring to previous steps as needed.
- Combinations:
  - Chain of thought with zero-shot: Breaking down questions without context or examples.
  - Chain of thought with few-shot: Breaking down questions with context and examples.

## Key Takeaways

- Generative AI and foundational models can create new content by emulating human cognition on large datasets.
- Large language models are a powerful subset of foundational models for text-based tasks.
- Prompt engineering optimizes the input prompts to control the model's output without retraining.
- Following best practices and using techniques like few-shot and chain of thought prompting can improve the quality and relevance of the model's responses.
- Experimentation and iterative refinement of prompts are encouraged to achieve the desired results.