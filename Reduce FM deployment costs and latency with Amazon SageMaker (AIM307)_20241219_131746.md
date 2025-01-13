# Summary of AWS re_Invent 2024 - Reduce FM deployment costs and latency with Amazon SageMaker (AIM307).txt

Here is a comprehensive summary of the transcript in Markdown format:

# AWS re:Invent 2024 - Reduce FM Deployment Costs and Latency with Amazon SageMaker (AIM307)

## Introduction

- This session explores how to maximize return on investment by achieving optimal performance at the lowest possible cost for hosting machine learning models.
- It covers two fully managed inference capabilities in AWS: Amazon Bedrock and Amazon SageMaker.
- The focus is on SageMaker inference capabilities that help achieve low inference latencies, high throughput, and optimal cost alignment.

## Amazon Bedrock vs. Amazon SageMaker

- **Amazon Bedrock** is best suited for serverless deployment, with no need to provision instances or configure infrastructure. It offers pre-trained models that can be fine-tuned, with token-based pricing.
- **Amazon SageMaker** is the go-to choice for more control over deployment infrastructure. It is server-based, allowing users to fully configure the managed infrastructure for their models. Users can bring their own models, and pricing is instance-based.

## SageMaker Inference

- SageMaker Inference offers a configurable software and hardware stack, giving customers granular control over their machine learning infrastructure.
- Deploying models on SageMaker involves three steps: creating a SageMaker model object, configuring an endpoint, and deploying the model to the endpoint.
- With access to over 100 instance types, including CPUs, GPUs, and specialized AI accelerators, users can precisely match compute resources to their model's needs.
- SageMaker allows adding custom pre- and post-processing steps, as well as deploying multiple models onto a single endpoint.

### Balancing Complexity, Performance, and Cost

- Three factors to consider when deploying models at scale: complexity, performance, and cost.
- Complexity manifests in model size, ensembles, or systems of models.
- Cost involves minimizing hosting and operational overhead.
- Performance relates to minimizing inference latencies and achieving high throughput.
- These three factors often pose a tradeoff, where users can choose two to meet business requirements, and the third becomes difficult to optimize.

## Cost-Saving Features

- **Multi-Model Endpoints**: Host multiple foundational models on a single endpoint, using accelerators effectively.
- **Faster Autoscaling**: Over 58% lower autoscaling latencies for popular foundational models.
- **Scale Down to Zero**: Configure endpoints to scale down to zero instances when there is no traffic, saving costs.
- **Fine-Tuned Model Flavors**: Host thousands of fine-tuned flavors of a model on the same endpoint and instance, saving costs.

## Performance Optimization Features

- **Load-Aware Routing**: SageMaker tracks which model copies are serving traffic and routes requests to available copies, reducing latency by over 20%.
- **Session-Aware Routing**: All requests for the same session are routed to the same model copies, allowing reuse of processed information.
- **Inference Optimization Toolkit**: Provides speculative decoding, quantization, and compilation for improved performance and lower costs.

## Demos

1. **Sticky Session Routing**: Demonstrated using the LAVA model, showing a reduction in inference latency from 5.39 seconds to around 1 second for subsequent inferences on the same data asset.

2. **Speculative Decoding**: Demonstrated using the LAMA 370B model, achieving a 40-50% improvement in inference latency by using a smaller draft model to generate tokens in parallel.

3. **Quantization**: Demonstrated using Activation-Aware Weight Quantization (AWQ) on the LAMA 370B model, enabling deployment on a smaller G5 12X large instance while maintaining similar inference performance.

## Capital One Success Story

- Grant Gillary, VP and Distinguished Engineer at Capital One, shared their success story of deploying models on SageMaker for inference.
- Capital One has embarked on an AI and ML journey, with use cases in production across nearly all lines of business.
- They integrated SageMaker inference into the backend of their ML platforms, enabling the FM inferencing stack while aligning with existing production systems and pipelines.
- The integration reduced development time, worked out-of-the-box with deep learning containers, reduced vulnerability exposure, and provided high availability.
- Capital One is evaluating optimizations like safety inference components, speculative decoding, and quantization for further improvements.

## Key Takeaways

- SageMaker Inference offers configurable software and hardware stacks for granular control over machine learning infrastructure.
- Various features help optimize deployment costs, inference latencies, and throughput.
- Demos showcased the benefits of session-aware routing, speculative decoding, and quantization.
- Capital One's success story demonstrated the integration of SageMaker inference into their ML platforms, enabling FM inferencing while aligning with existing processes.

## Q&A Session

- The session concluded with a Q&A session, where attendees could ask questions and provide feedback through the session survey.