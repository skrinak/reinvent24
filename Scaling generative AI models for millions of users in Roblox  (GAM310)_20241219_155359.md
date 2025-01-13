# Summary of AWS re_Invent 2024 - Scaling generative AI models for millions of users in Roblox  (GAM310).txt

# Summary of AWS re:Invent 2024 - Scaling generative AI models for millions of users in Roblox (GAM310)

## Introduction

- Roblox is a platform that allows users to create and play games, with around 2.5 million developers, 5.3 million experiences, and 79 million daily active users.
- Roblox uses generative AI for various purposes, including safety, creator assistance, and player recommendations.
- They have built an AI API suite to integrate AI into their platform, catering to millions of users and creators.

## Roblox AI API Suite Architecture

- Roblox has an architecture that combines on-premises servers and AWS EC2 for GPU compute clusters.
- They use various tools and services, including a feature store, ground truth system, storage solutions (S3, Vector DB), data lake, Kubeflow, KServe, BLM (Batched Lambda Model Server), Ray, and custom gateways.
- The gateway architecture pattern is used to multiplex different AI providers, models, and versions, abstracting the complexity from developers.

## Challenges and Solutions

### 1. Blending and Managing Different AI Inference Use Cases

- Roblox uses a mix of cloud providers, open-source models (e.g., Llama), and their own models.
- Open-source models can be 10-26% of the cost compared to cloud providers, but with potential trade-offs in quality.
- The gateway architecture allows them to seamlessly switch between different providers, models, and versions.

### 2. Scaling with Capacity Constraints

- Roblox faces capacity constraints when using cloud GPUs, leading to sudden load spikes.
- They implemented a load spillover solution, where they provision heterogeneous clusters and dynamically route load across them.

### 3. Densifying GPU Clusters

- Roblox aims to maximize GPU utilization by densifying clusters.
- They encourage teams to use online and offline batching techniques to improve throughput and reduce costs.
- Shared GPU pools and mixing batch use cases with existing clusters helped improve utilization by 10x.

### 4. Evaluating Models for Production Use Cases

- Performance metrics like time to first token, time per output token, latency, and throughput are important, with throughput being the highest priority for cost-effectiveness.
- Quality evaluation is challenging, as academic datasets like MMLU and Chatbot Arena may not fully represent production use cases.
- Roblox is building its own evaluation datasets, using human labelers, LLM judges, and frameworks like Helm to assess model performance on their specific use cases.

### AWS Deep Learning Containers

- AWS Deep Learning Containers helped Roblox reduce operational burden by providing pre-packaged, validated, and optimized container images for various ML frameworks and hardware configurations.
- This enabled them to adopt new models, hardware, and versions more quickly, without the overhead of managing dependencies and compatibility issues.

## Lessons Learned

- Open-source model quality is improving and can be a cost-effective alternative to hosted solutions, with proper usage transparency and acknowledgment of potential trade-offs.
- Version toiling (managing different versions of models, clusters, inference engines, etc.) can be a significant burden, and tools like AWS Deep Learning Containers can help reduce this complexity.
- Densifying clusters through techniques like batching and load spillover can significantly improve cost-effectiveness.
- Evaluating model performance and quality for production use cases remains a challenge, but building custom evaluation datasets and leveraging human labelers and LLM judges can provide better insights.