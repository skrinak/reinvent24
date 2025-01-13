# Summary of AWS re_Invent 2024 - Using multiple agents for scalable generative AI applications (AIM304).txt

Here is a comprehensive summary of the AWS re:Invent 2024 session "Using multiple agents for scalable generative AI applications (AIM304)" in Markdown format:

# AWS re:Invent 2024 - Using Multiple Agents for Scalable Generative AI Applications

## Introduction

- The session introduced Amazon Bedrock Agents, a fully managed service for creating and deploying generative AI agents.
- Bedrock Agents provides foundational building blocks for customers to create their own agentic applications, including access to various models, agentic primitives (memory, knowledge bases, Guardrails, tools), and debugging/observability capabilities.
- The session highlighted the recently launched multi-agent collaboration feature, which allows orchestrating complex tasks using groups of specialized agents.

## Why Multi-Agent Workflows?

- Single agents can become monolithic and decrease in task success, accuracy, and goal achievement as they scale to handle more complex problems.
- Customers have organically evolved to use multi-agent workflows, with groups of specialized agents chained together and orchestrated by a supervisor agent.
- Multi-agent collaboration enables more complex problem-solving, improves accuracy and scalability, and allows reusing and composing agents across teams.

## Key Capabilities of Multi-Agent Collaboration

- Easily assemble a set of smaller, focused agents and knowledge bases.
- Use a supervisor agent to plan and execute across sub-agents without writing complex code.
- Unified conversations across agents with built-in intent classification and low-latency routing.
- Observability across flows, including sub-agent invocations and multi-level hierarchies.
- Security, Guardrails, privacy, and data governance inherited from AWS and Bedrock Agents.

## Use Cases

### 1. Unifying Customer Experience

- Replace siloed, focused agents with a supervisor and collaborators, enabling seamless conversations across capabilities.
- Optimized routing routes user requests to the right sub-agent in sub-second time.
- Allows providing a one-stop shop for customers to interact with all aspects of a business.

### 2. Automating Complex Processes

- Define roles and experts as specialized sub-agents, and add a supervisor on top.
- The supervisor can plan and execute multi-step workflows across sub-agents, including parallelism and iterations.
- Enables tackling complex processes like investment portfolio analysis, insurance claims processing, and code generation.

## Customer Case Study: Northwestern Mutual

- Northwestern Mutual built a multi-agent solution on Bedrock Agents for internal developer support.
- The solution answers support requests within minutes without engineer engagement, freeing up time for complex issues.
- It uses multiple specialized agents (documentation, user management, repository management, pipeline analysis, response evaluation) orchestrated by a supervisor.
- Key lessons learned: curate data well, use cross-region inference, explain model decisions, limit actions per agent, filter noise for good user experience, and prioritize observability.

## Demos

1. **Unified Customer Experience**: A Mortgage Assistant with sub-agents for existing mortgages, new applications, and general questions, providing a seamless experience.

2. **Automating Complex Processes**: A Startup Advisor with sub-agents for market research, strategy, content writing, creative direction, and report formatting, generating a comprehensive marketing strategy report.

## Call to Action

- Get an open-source library of Bedrock Agent samples, including single agents and multi-agent collaboration examples (Mortgage Assistant, Startup Advisor, sports team poetry, and more).
- Kick off POCs and prototypes, and provide feedback to the Bedrock Agents team.