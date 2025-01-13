# Summary of AWS re_Invent 2024 - Building an AWS solutions architect agentic app with Amazon Bedrock (DEV331).txt

# AWS re:Invent 2024 - Building an AWS Solutions Architect Agentic App with Amazon Bedrock

## Introduction

- Banjo Obayomi: Senior Developer Advocate at AWS, creates technical content to educate and inspire builders.
- Namrata Shah: AWS Hero, Software Engineer, Managing Director & Head of Engineering at Nuveen, YouTuber (posts AWS tutorials and hands-on labs).

## The AWS Gen AI Stack

- Infrastructure layer: Amazon SageMaker, AWS Trainium (for training models), AWS Inferentia (for model inference), GPU-based EC2 instances.
- Amazon Bedrock: Fully managed serverless service to build and scale Gen AI applications using a foundation model.
- Amazon Q Business and Developer: Applications built on Bedrock, e.g., Amazon Q Developer (coding assistant).
- Third-party foundation models: Bedrock supports various third-party providers and models for different tasks like text summarization.

## Agentic Workflows

- An AI agent is an autonomous system that perceives, decides, and acts to achieve goals, adapting its behavior based on experiences and interactions.
- Key design patterns of agentic workflows:
  - Reflection: Self-examination and improvement.
  - Tool use: Ability to access external tools, data, and services.
  - Planning: Step-by-step planning and execution.
  - Multi-agent collaboration: Leveraging multiple agents for different tasks.

- Benefits of agentic systems:
  - Break down complex tasks and adapt strategies.
  - Increase autonomy for open-ended requests.
  - Efficiency for multi-step processes.
  - Scalability for multiple complex tasks.

## Building the AWS Solutions Architect Agentic App

### Knowledge Base Integration

- Integrated the AWS Well-Architected Framework as a knowledge base.
- Demonstrated querying the knowledge base for best practices on cloud security, providing context-aware responses.

### Diagram Review and Creation

- Reviewed a media streaming architecture diagram by describing its components and design considerations.
- Created an e-commerce architecture diagram from a simple prompt, describing the diagram's components.

### Infrastructure Deployment

- Generated a Python CDK script to deploy the e-commerce architecture on AWS.
- Created and deployed a Lambda function for sentiment analysis, demonstrated calling the function from a Python script.
- Provided instructions for setting up a CDK deployment app.

### Live Coding with Amazon Q

- Leveraged Amazon Q for live coding, explaining existing code, and making changes.
- Demonstrated updating code regions and accepting suggestions from Amazon Q.

## Key Takeaways

- Integrating AI into personal and team workflows can significantly enhance productivity and efficiency.
- Agentic workflows and tools like Amazon Bedrock and Amazon Q empower builders to create custom AI-powered applications tailored to their needs.
- No one has a definitive playbook on how to best use AI in an organization; builders must explore and find what works for their specific use cases.
- Building and experimenting with AI tools is crucial to unlocking their potential and staying ahead in the rapidly evolving AI landscape.

The session provided a practical demonstration of building an AWS Solutions Architect Agentic App using Amazon Bedrock, showcasing its capabilities in knowledge base integration, diagram creation, infrastructure deployment, and live coding with Amazon Q. The presenters emphasized the importance of embracing AI tools and finding ways to integrate them into personal and team workflows for increased productivity and efficiency.