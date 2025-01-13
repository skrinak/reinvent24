# Summary of AWS re_Invent 2024 - SK Telecom_s TelClaude_ Redefining telco CX with generative AI on AWS (TLC203).txt

# AWS re:Invent 2024 - SK Telecom's TelClaude: Redefining Telco CX with Generative AI on AWS

## Summary

### Introduction

- This session covers the collaboration between AWS, SK Telecom, and Anthropic to fine-tune the Claude language model for contact center use cases in the telecommunications industry.
- The session highlights the process, challenges, and benefits of fine-tuning large language models for high-value workflows.

### Telco Industry and Contact Center Context

- Customers expect personalized service from telcos across various channels (phone, chat, retail stores, etc.).
- Phone calls account for 80% of interactions with telcos, with billions of voice minutes processed through contact centers annually.
- 60-70% of calls are billing or account-related, presenting an opportunity for automation and optimization.
- Expectations for personalization and frictionless experiences have been driven up by digital natives like Amazon.
- Telcos aim to transform contact centers from cost centers to profit centers, with up to 60% of future revenue expected to be driven through contact center interactions.

### Collaboration and Fine-tuning Process

- SK Telecom provided domain expertise, language expertise, and data for fine-tuning.
- Anthropic handled model fine-tuning, reinforcement learning from human feedback (RLHF), and prompt engineering.
- AWS provided the infrastructure, scalability, and collaboration through the Generative AI Innovation Center and Amazon Bedrock.
- The collaboration involved iterative cycles of data construction, fine-tuning, RLHF, and benchmarking over the course of a year.

### TelClaude: The Fine-tuned Model

- TelClaude is the fine-tuned model optimized for the telecommunications domain.
- It was trained on two datasets: TelTask (for enhancing capabilities like summarization, intent detection, and topic extraction) and TelInstruct (for teaching domain knowledge and retrieval).
- The model showed a 38% improvement in Telco Expertise Score and over 90% customer satisfaction compared to the base model.
- Trust and safety were prioritized, with systems in place to detect and filter out inappropriate or off-topic content.

### Use Cases and Results

- TelClaude was applied to two main use cases: real-time assist during calls and post-call automation.
- Real-time assist involved searching relevant documents, generating responses, and providing citations to agents.
- Post-call automation included call summarization, intent detection, and topic extraction, reducing manual effort for agents.
- The model improved customer experience by providing faster and more uniform responses, and increased agent satisfaction by reducing stress and ramp-up time for new hires.

### Lessons Learned and Future Directions

- Benchmarking and evaluation for large language models are complex and require a combination of automated metrics, human evaluation, and end-to-end workflow evaluation.
- SK Telecom plans to expand the use of TelClaude to other domains like marketing, network operations, legal, and public relations.
- The collaboration with AWS and Anthropic enabled scalability, reliability, and expertise in model serving and optimization.

### Conclusion

The session showcased the successful collaboration between AWS, SK Telecom, and Anthropic in fine-tuning a large language model for the telecommunications domain. The fine-tuned model, TelClaude, demonstrated significant improvements in performance and customer satisfaction, paving the way for further expansion into other domains and use cases.