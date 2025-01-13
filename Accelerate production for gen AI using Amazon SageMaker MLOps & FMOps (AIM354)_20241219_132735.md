# Summary of AWS re_Invent 2024 - Accelerate production for gen AI using Amazon SageMaker MLOps & FMOps (AIM354).txt

Here is a comprehensive summary of the transcript, formatted in Markdown with appropriate headers and bullet points:

# AWS re:Invent 2024 - Accelerate Production for Generative AI using Amazon SageMaker MLOps & FMOps

## Key Trends in Generative AI

- Customer spend on generative AI grew 2.5x in less than a year, from $7 million to $18 million annually.
- Customers are increasingly relying on multiple model providers for building generative AI applications.
- With the advent of high-quality open-source foundation models, customers are now relying on pre-trained foundation models and customizing their behavior instead of building their own foundation models.

## Overview of MLOps, FMOps, and Gen AI Ops

- **MLOps** brings practices across people, process, and technology to build scalable, repeatable, and reliable AI/ML workloads.
- **FMOps** builds on top of MLOps and brings in unique aspects relevant for foundation models, such as selecting and evaluating foundation models, using prompts to modify behavior, and implementing safeguards.
- **Gen AI Ops** builds on top of FMOps and brings in unique aspects required for building end-to-end generative AI solutions, such as capabilities to build agents, augmenting foundation models with secondary sources of information, and specialized capabilities to trace and observe the behavior of generative AI applications in production.

## Key Challenges and Recommendations

### 1. High-Quality Training Data for Fine-Tuning

- Challenge: Fine-tuning foundation models requires high-quality training data, which often depends on human annotators.
- Recommendation: Use SageMaker Ground Truth, which provides an easy interface for human feedback and can be integrated into model development pipelines.

### 2. Experiment and Model Management

- Challenge: Tracking experiments, associated metadata, and model inputs/artifacts can be tedious and error-prone.
- Recommendation: Use SageMaker's managed MLflow for reliable experiment tracking and model management, which comes pre-configured with SageMaker capabilities and can be accessed from various environments.

### 3. Prompt Management

- Challenge: With prompt management, new personas emerge who want to interact with foundation models for modifying their behavior, and different tools are preferred.
- Recommendation: Follow best practices for prompt patterns, such as saving prompts as templates and data, and combining prompts with evaluation results for traceability and collaboration.

### 4. Building Repeatable Workloads

- Recommendation: Use SageMaker Pipelines to build end-to-end model development pipelines, incorporating human feedback, fine-tuning, and deployment steps. Pipelines are serverless, pre-integrated with SageMaker capabilities, and can be scheduled with EventBridge.

### 5. Evaluation and Monitoring

- Challenge: Generative AI and FMOps require broader evaluation metrics across model performance, data quality, user feedback, agent behavior, and system metrics.
- Recommendation: Use SageMaker MLflow and Clarify for model evaluation, incorporate user feedback, and leverage AWS services and open-source tools like OpenTelemetry for observability and monitoring.

### 6. Risk Compliance and Governance

- Recommendation: Use SageMaker Model Registry as a single source of truth for all models, capturing training job information, evaluation results, and enabling model sharing across environments for traceability and compliance.

### 7. Implementing Safeguards

- Challenge: When users interact with foundation models through prompts, there is a need to manage prompt injection attacks and filter out harmful or sensitive content in responses.
- Recommendation: Restrict access to models based on licensing and corporate policies, use Bedrock Guardrails or build custom safeguards with LlamaGuard for filtering content, and deploy models cost-effectively using techniques like multi-adapter inference endpoints.

## Rocket Mortgage's Journey with MLOps and FMOps

- Rocket Mortgage has a mission to make homeownership attainable for everyone and has invested heavily in AI and data to transform the industry.
- They started their MLOps journey 10 years ago and have scaled up their infrastructure to support over 200 proprietary AI models in production.
- By adopting a modernized data strategy with AWS services like S3, Redshift, and Lake Formation, and leveraging SageMaker and Bedrock, they have reduced development time by 40-60%, increased business velocity, and improved efficiency while maintaining high accuracy standards.
- Rocket Mortgage has successfully deployed generative AI solutions like chatbots and document processing, resulting in higher client satisfaction, increased team member productivity, and significant time savings.

## Key Takeaways and Resources

- Apply human feedback to create and evaluate high-quality models with SageMaker Ground Truth.
- Manage ML models and generative models, and track application experiments at scale with MLflow.
- Use model evaluation with MLflow and SageMaker Clarify for FMOps.
- Create automated build workflows with SageMaker Pipelines.
- Implement safeguards using Bedrock Guardrails or open-source models like LlamaGuard.
- Explore additional resources:
  - SageMaker MLOps page
  - Generative AI workshop
  - LinkedIn profiles of the presenters