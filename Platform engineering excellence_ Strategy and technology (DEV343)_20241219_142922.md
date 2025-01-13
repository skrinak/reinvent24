# Summary of AWS re_Invent 2024 - Platform engineering excellence_ Strategy and technology (DEV343).txt

# Summary: Platform Engineering Excellence: Strategy and Technology

## Introduction

- Harrison is an elite engineer at Fujitsu, presenting on platform engineering strategy and implementation for their customers.
- Platform engineering aims to solve the complexity of managing cloud infrastructure and tooling by introducing automation and self-service capabilities for development teams.

## The Problem Platform Engineering Solves

- As cloud infrastructure and tooling grow more complex, it becomes unmanageable and reduces team efficiency.
- Managing multiple AWS services, identity and access management, data storage, and other tools across different projects leads to cognitive overload and chaos.

## What is Platform Engineering?

- Platform engineering introduces automation to improve cognitive load and efficiency for downstream development teams.
- It focuses on providing self-service infrastructure catalogs, reusable patterns, cost optimization, and accelerated development.

## Components of a Good Platform

- Self-service developer portal for requesting AWS accounts and infrastructure
- Infrastructure as Code for managing resources
- Reusable, modular components
- Integrated monitoring tools
- Identity and access management integration

## Principles of Platform Engineering

- Scalable and secure
- Modular and standardized
- Automated processes
- Continuously improved through collaboration

## Importance of Platform Engineering

- Gartner predicts 80% of large organizations will use platform engineering by 2026.
- Platform teams build the platform, and engineering teams use it to automate complex infrastructure.
- The DORA report shows DevOps can increase acceleration by up to 40%.

## Implementing Platform Engineering

- Open-source tools like AWS Control Tower and HashiCorp Terraform can be used to provision and secure AWS accounts.
- Fujitsu's implementation includes HashiCorp Vault for secret management, GitLab for source control and CI/CD, and Okta for identity management.
- They have built a self-service developer portal for vending AWS accounts, infrastructure, SageMaker models, and bundled applications.
- Their DevSecOps pipeline integrates local development, code scanning, Docker builds, Kubernetes deployments, and monitoring with Datadog.

## Challenges and Solutions

- Maintaining the infrastructure catalog and deploying across AWS accounts securely and repeatably.
- Enforcing cross-account governance using AWS Control Tower and automating non-compliance remediation.

## Benefits for Customers

- Saving 30 days when provisioning a new AWS account
- Up to $50,000 in resourcing and infrastructure cost savings
- 40% accelerated developer performance

## Future Roadmap

- Expanding the catalog with more Golden Paths and organization-approved templates
- Supporting multi-cloud and hybrid environments
- Focusing on developer experience and feedback
- Accelerating AI development using tools like CodeWhisperer and Amazon CodeWhisperer
- Continuously improving based on feedback from engineers and customers