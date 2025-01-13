# Summary of AWS re_Invent 2024 - Accelerating multi-tenant development with the SaaS Builder Toolkit (SAS406).txt

# AWS re:Invent 2024 - Accelerating multi-tenant development with the SaaS Builder Toolkit (SAS406)

## Overview

The SaaS Builder Toolkit (SBT) is a set of tools and libraries designed to accelerate the development of multi-tenant Software as a Service (SaaS) applications on AWS. It provides a composable experience for building and customizing SaaS solutions, allowing developers to pick and choose the components they need and extend or replace them as necessary.

## Key Points

### SaaS Builder Toolkit (SBT)

- SBT is a CDK-heavy experience, leveraging the power and expressiveness of the AWS Cloud Development Kit (CDK) to describe and provision infrastructure.
- It is a tool, not a product, designed to be used in an editor-based environment, where developers can compose and customize the SaaS environment through CDK constructs.
- SBT is composed of three main areas: Control Plane, Application Plane, and Libraries and Utilities.

### Control Plane

- The Control Plane provides a ready-to-use implementation of common SaaS components, such as tenant management, user management, billing, and metering.
- It supports extensibility through interfaces, allowing third-party integrations and customizations.
- The "Bring Your Own Control Plane" concept encourages developers to use the provided Control Plane as a starting point or create their own implementation.

### Application Plane

- The Application Plane is an open playground for developers to build their business functionality and address tenant isolation and data partitioning.
- SBT provides reference architectures (e.g., EKS, Serverless) as starting points for the Application Plane.
- Developers can customize or replace the provided Application Plane implementations or create their own from scratch.

### Libraries and Utilities

- SBT includes a collection of libraries and utilities to assist in common SaaS development tasks, such as tenant isolation and token vending.
- These libraries can be easily integrated into the Application Plane or extended with custom implementations.

## Important Conclusions

- SBT is designed to be a composable and extensible toolkit, allowing developers to pick and choose the components they need and customize them as required.
- It provides a consistent approach to building SaaS solutions by separating the Control Plane and Application Plane, while enabling integration between the two.
- SBT leverages the power of CDK and constructs, making it easier to understand, modify, and extend the codebase.
- Developers are encouraged to contribute feedback and extensions to help shape the future direction of SBT.

Overall, the SaaS Builder Toolkit aims to accelerate the development of multi-tenant SaaS applications by providing a composable and extensible set of tools, libraries, and reference architectures, while promoting best practices and separating concerns between the Control Plane and Application Plane.