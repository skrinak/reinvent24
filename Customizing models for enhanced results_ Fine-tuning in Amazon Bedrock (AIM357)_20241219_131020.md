# Summary of AWS re_Invent 2024 - Customizing models for enhanced results_ Fine-tuning in Amazon Bedrock (AIM357).txt

# Summary

## Introduction
- Fine-tuning is a hot topic for squeezing performance from foundation models and small language models.
- The session covers the basics of fine-tuning, two applications with Anthropic and Meta models, and relevant features in Amazon Bedrock related to fine-tuning and model customization.

## What is Fine-tuning?
- Fine-tuning is the process of taking a pre-trained model and customizing it with task-specific data.
- Large organizations pre-train models on massive unlabeled data to get a capable foundation model.
- Task-specific labeled data (prompt-completion pairs) is then used to fine-tune the base model for a particular use case.
- Fine-tuning allows models to perform well on specific tasks and domains, improving accuracy and domain-specific capabilities.

## Fine-tuning Lifecycle
1. **Use Case**: Define the specific task, e.g., document summarization, text-to-SQL.
2. **Data Preparation**: Clean, enrich, and de-duplicate high-quality task-specific data.
3. **Fine-tuning**: Use frameworks like Amazon SageMaker or Amazon Bedrock to fine-tune the model with the prepared data.
4. **Monitoring**: Monitor the fine-tuning process and adjust hyperparameters if needed.
5. **Evaluation**: Evaluate the fine-tuned model's performance on a blind test set.

## When to Fine-tune?
- Fine-tune when prompt engineering and retrieval-augmented generation (RAG) don't fully meet the requirements.
- Fine-tune for tasks outside the base model's expertise, like teaching a new skill (e.g., text-to-SQL).
- Fine-tune when few-shot examples work well, indicating potential for fine-tuning with more data.
- Fine-tune when prompts become excessively long and complex, to reduce input token costs.

## Key Considerations for Fine-tuning
- Fine-tune for new concepts the base model is familiar with, but needs to learn through small-scale fine-tuning.
- Fine-tune when few-shot results are promising, as fine-tuning with more data can improve performance further.
- Fine-tune when prompt engineering leads to overly complex prompts, to simplify prompts while maintaining performance.

## Amazon Bedrock Fine-tuning Features
- **Bedrock Fine-tuning**: Fine-tune models with a JSON Lines formatted dataset, using the console or APIs.
- **Hyperparameters**: Control fine-tuning outcomes with parameters like learning rate, epochs, and warmup steps.
- **Continued Pre-training**: Rare but supported, allowing pre-training models from scratch with unlabeled data.
- **Custom Model Import**: Import fine-tuned models from other sources (e.g., SageMaker, HuggingFace) into Bedrock for inference.
- **Model Distillation**: Generate labeled data using a larger model, then fine-tune a smaller model on this data.

## Customizing Anthropic Claude 3 Haiku
- Data preparation: Use JSON Lines format with the message API, alternating user and assistant roles.
- Fine-tuning parameters: Epoch count, batch size, learning rate, early stopping threshold, and early stopping patience.
- Best practices: Use higher batch sizes for larger datasets, lower for smaller datasets. Learning rate has more impact with larger datasets.
- Evaluation: Fine-tuned Haiku outperformed base Haiku, Claude 3 Sonnet, and Claude 3.5 Sonnet on the TAT-QA dataset.
- Benefits: Reduced output token usage (35% improvement) and more concise, factual outputs.

## Customizing Meta Llama Models
- Use cases benefiting from fine-tuning: Customer service chatbots, content generation, compliance and regulatory analysis, financial chart analysis.
- Crucial steps: Dataset analysis, processing, diversity, and curation for the specific domain or task.
- Fine-tuning approaches: Full parameter fine-tuning, LoRa, QLoRa (examples in Llama Recipes and Llama Stack repos).
- Demo: Fine-tuning an 8B model using synthetic data generated from the 405B model, improving performance on algebraic word problems.
- Benefits: Increased performance, accuracy, and adaptation to specific use cases. Potential cost savings through reduced token usage.

## Conclusion
- Fine-tuning allows models to excel at specific tasks and domains by customizing them with high-quality, relevant data.
- Amazon Bedrock offers managed fine-tuning features, including custom model import and model distillation.
- Anthropic and Meta models can be fine-tuned for improved performance, with benefits like reduced token usage and increased accuracy.
- Proper data preparation, hyperparameter tuning, and evaluation are crucial for successful fine-tuning.