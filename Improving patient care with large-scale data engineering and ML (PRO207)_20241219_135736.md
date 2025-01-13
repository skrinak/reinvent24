# Summary of AWS re_Invent 2024 - Improving patient care with large-scale data engineering and ML (PRO207).txt

# Improving Patient Care with Large-Scale Data Engineering and ML

## Key Points

- AI/ML in healthcare is challenging due to the vast amount of unstructured data trapped in freeform medical texts (progress notes, medical notes, visit summaries, etc.), which is growing at a petabyte scale daily.

- Three common healthcare use cases addressed:
  1. Patient care coordination (organ transplant, cancer treatment planning)
  2. Patient transfer between healthcare organizations
  3. Population healthcare analysis with government departments

- Traditional AI/ML methods face limitations:
  - Incomplete extraction of document images (OCR misses complex data like tables, forms, images)
  - Bag-of-words technique lacks contextual understanding and relationships
  - Simpler ML algorithms are not contextually aware

## Solution Approach

### 1. Data Extraction with Amazon Textract
- Improves text extraction from document images, including handwriting, distorted text, and low-quality images
- Recognizes document layout, table structures, and form key-value pairs

### 2. Summary Generation with GenAI (Amazon Bedrock)
- Mimics human reading process by asking and answering relevant questions
- Collects questions from clinical experts and converts them into prompts
- GenAI agent answers the prompts on the documents
- Compiled answers form a concise summary, increasing signal-to-noise ratio

### 3. Predictive Modeling with Transformer Models (Amazon SageMaker)
- Transformer models can directly consume the summary text, preserving context
- Skips feature engineering, making the approach scalable
- Utilizes transfer learning with pre-trained clinical transformer models
- Configures the final layer for specific use cases (e.g., patient transfer prediction)

### Architecture and Parallelization
- Utilizes AWS services like Lambda, Step Functions, and SageMaker
- Step Functions' Map state enables concurrent processing of hundreds of thousands of tasks

## Potential Improvements
- Explore visual language models for multimodal processing of document images
- Implement guardrails to mitigate LLM hallucinations, using human evaluation or automated contextual ground checking
- Optimize cost by using AWS Trainium for training transformer models

## Conclusion
The presented solution leverages GenAI-driven data engineering, mimicking human reading processes, and massively parallel processing on AWS Cloud to address common healthcare use cases involving unstructured medical data. It highlights the potential of combining GenAI, transformer models, and cloud technologies to improve patient care through large-scale data analysis.