# Summary of AWS re_Invent 2024 - How to choose between AWS CloudFormation, Terraform, and AWS CDK (DEV309).txt

# Summary

## Introduction

- The speaker, Martijn van Dongen, discusses the evolution of Infrastructure as Code (IaC) tools and how to choose between AWS CloudFormation, Terraform, and AWS Cloud Development Kit (CDK).
- He covers the differences between these tools, their respective levels (L1, L2, L3), and provides rapid learning exercises and demos for each tool.
- The talk also addresses common anti-patterns and key takeaways for selecting and using IaC tools effectively.

## Evolution of Infrastructure as Code

- CloudFormation was launched around 2011-2012, marking a shift from scripting to using IaC tools.
- Terraform was introduced in 2014, providing an alternative IaC tool.
- AWS CDK version 1 was launched in 2018, allowing developers to define AWS resources using programming languages.

## Rapid Learning Exercises

### Terraform

- L1 (Basic): Defining individual resources like VPCs, DynamoDB tables, and Lambda functions.
- L2 (Modules): Using pre-built modules from the community (e.g., Anton Compalinco's modules) for reusable infrastructure components.
- L3 (Stack Modules): Combining multiple modules into comprehensive architectures and sharing them across teams.

### CloudFormation

- L1 (Basic): Defining resources in a single CloudFormation template.
- L2 (Sceptre/Terraform): Using tools like Sceptre or Terraform to structure CloudFormation templates and share them across teams.
- L3 (AWS Service Catalog): Leveraging AWS Service Catalog for pre-approved, shareable architectures.

### AWS CDK

- L1 (Basic): Defining CloudFormation resources using a programming language.
- L2 (Curated Constructs): Using higher-level constructs provided by CDK for common infrastructure patterns.
- L3 (Patterns): Creating reusable patterns and sharing them across teams.

## Anti-Patterns

- Building monolithic, complex IaC configurations that are difficult to maintain and share.
- Letting experts or fans choose the tool, leading to knowledge gaps and dependencies.
- Asking customers to write IaC code without providing a sandbox or playground.
- Overengineering solutions or concentrating risk on a single tool.
- Disregarding the human effort required to learn and maintain IaC tools.
- Underestimating the knowledge gap between experts and new users.

## Key Takeaways

1. Think about how to use IaC tools effectively (L1, L2, or L3) and simplify where possible.
2. Create abstractions or share knowledge to make IaC tools more accessible and scalable.
3. Understand the different needs of partners and customers when choosing IaC tools, and strive for "stickiness" rather than "lock-in."

## Additional Resources

- The speaker's bio link and GitHub repository containing the demo code and resources are provided.