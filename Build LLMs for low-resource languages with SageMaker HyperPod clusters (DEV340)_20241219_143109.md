# Summary of AWS re_Invent 2024 - Build LLMs for low-resource languages with SageMaker HyperPod clusters (DEV340).txt

# Summary: Building Large Language Models for Low-Resource Languages with SageMaker HyperPod Clusters

## Introduction

- The talk focuses on building large language models (LLMs) for low-resource languages using AWS SageMaker HyperPod clusters.
- Low-resource languages have limited linguistic resources available for computational processing and analysis.
- Preserving and safeguarding low-resource languages is crucial for maintaining intangible cultural heritage.

## Challenges and Importance

- Over 1,500 languages could be lost in the next 100 years, highlighting the need for language preservation efforts.
- Cantonese, despite being widely spoken, is considered a low-resource language with limited available data compared to English and Chinese.
- Building LLMs for low-resource languages faces challenges in data preparation, quality issues, and limited resources.

## Data Preparation

- Various data sources were utilized, including dictionaries, surveys, reviews, news, textbooks, and conversations from subtitles.
- Data processing steps included cleaning, deduplication, language identification, and quality control.
- Extracting data properly from sources like Wikipedia was crucial to avoid missing information or hallucination.
- A data pipeline generation using advanced LLMs was employed for synthetic data operations, such as translation and persona-based generation.

## Training Environment and Setup

- AWS CloudFormation was used to set up the training environment, including the cluster admin, lifecycle scripts, S3 buckets, and VPC subnets.
- The FSx for Lustre high-performance file system was utilized for handling LLM training tasks.
- The training was performed on SageMaker HyperPod clusters with AWS Trainium1 accelerators, leveraging the NeuronX Distributed framework from the Amazon Neuron SDK.
- Techniques like Tensor Parallelism and ZeRO redundancy optimizer were employed for efficient training.

## Evaluation and Applications

- The trained Cantonese LLM achieved promising results, with lower perplexity scores indicating better performance.
- Academic benchmarking using MMLU is underway to demonstrate state-of-the-art performance.
- The LLM can handle mixed Cantonese and English inputs, understanding local contexts and providing appropriate responses.
- Applications include chatbots, social media analysis, sentiment analysis, and industry-specific use cases requiring local language understanding.

## Open-Source and Collaboration

- The team is open-sourcing their data, models, and workflows on Hugging Face.
- They encourage collaboration and are willing to assist others in building LLMs for their local languages.

## Conclusion

The talk showcased the successful development of a Cantonese LLM using AWS SageMaker HyperPod clusters, highlighting the importance of preserving low-resource languages and the potential applications of such models in various industries. The team's open-source approach and willingness to collaborate aim to facilitate the development of LLMs for other low-resource languages.