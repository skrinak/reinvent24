# Summary of AWS re_Invent 2024 - Demystifying containers on AWS_ What’s right for you_ (DEV307).txt

Here is a comprehensive summary of the transcript in Markdown format:

# AWS re:Invent 2024 - Demystifying Containers on AWS: What's Right for You?

## Introduction

- The session aimed to help attendees decide which AWS container service to use based on their needs, team expertise, and challenges.
- The speakers emphasized that there are trade-offs with every decision, and organizations can't do everything, so they need to prioritize their requirements.

## Container Management on AWS

### Layers of Container Management

1. **Capacity Layer**: Provides the raw computing power (CPU, memory, infrastructure resources) for containers.
   - Services: Amazon EC2, AWS Fargate
2. **Orchestration Layer**: Manages container deployment, scaling, and lifecycle across the environment.
   - Services: Amazon ECS, Amazon EKS, Red Hat OpenShift Service on AWS (ROSA), Amazon EKS Anywhere, Amazon ECS Anywhere
3. **Provisioning Layer**: Simplifies interaction with the orchestrator, reducing friction for developers.
   - Services: AWS App Runner, AWS Elastic Beanstalk, AWS Amplify, Amazon Lightsail

### Service Groupings

- **Group 1**: Services where you bring your container image, and AWS runs it (ECS, EKS, App Runner, AWS Lambda).
- **Group 2**: Services where you can run containers, but the primary purpose is added value (App Runner, AWS Amplify, AWS Elastic Beanstalk).
- **Group 3**: Services where containers run under the hood, managed by AWS.

### Approaches to Choosing Container Services

1. **Tactical Approach**: Focuses on practical solutions to get the application running quickly, typically used by startups or smaller teams with specific use cases.
2. **Strategic Approach**: Focuses on organizational-level discussions, balancing long-term needs like scalability, control, and developer experience, typically used by larger teams building a platform for deploying containerized applications.

## Cost Optimization

- Consider the total cost of ownership, including developer time, business impact, and single points of failure.
- Explore cost-saving options like AWS Fargate Spot, Amazon EC2 Spot Instances, and AWS Lambda.
- Evaluate trade-offs between services like Lightsail, ECS with EC2, ECS with Fargate, App Runner, and Lambda based on cost, complexity, and operational efforts.

## Flexibility and Scalability

- Amazon EKS with Amazon EC2 provides flexibility and control over the underlying compute infrastructure, networking, storage, and access policies.
- Amazon EKS with AWS Fargate simplifies scaling and offers secure isolation, but at a higher cost compared to EC2 instances.
- Amazon EKS Auto Mode automates node provisioning, scaling, and patching for EKS with EC2.
- EKS can be extended with add-ons, AWS Controllers for Kubernetes (ACK), Amazon EKS Blueprints, Amazon Managed Prometheus and Grafana, and Karpenter for optimized resource utilization.

## Demo and Resources

- The speakers provided a QR code and a short link to a community.AWS post, where they will share the video recording, code repositories, Terraform examples, and AWS Cloud Development Kit (CDK) versions for various container services.