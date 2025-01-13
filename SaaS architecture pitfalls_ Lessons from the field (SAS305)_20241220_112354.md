# Summary of AWS re_Invent 2024 - SaaS architecture pitfalls_ Lessons from the field (SAS305).txt

# AWS re:Invent 2024 - SaaS architecture pitfalls: Lessons from the field (SAS305)

## Summary

### The Promise of SaaS

The key promises of SaaS include:

- Maintaining agility and flexibility
- Focusing on delivering innovation and delighting customers
- Maintaining operational efficiency
- Achieving sustainable and profitable growth

### Pitfalls and Lessons Learned

#### 1. Lack of a Control Plane

- SaaS requires a different set of tools, including a control plane, to operate the solution as a single unit.
- The SaaS Builder Toolkit (SBT) is an open-source solution that provides a control plane with services for onboarding, metrics, billing, tenant management, and more.
- SBT allows pluggable integration with third-party tools and supports different application architectures (serverless, EKS, ECS).

#### 2. Identity Crisis

- Identity is a complex and multi-faceted story in SaaS, involving tenant users, SaaS admins, and potentially federated identities.
- Best practices include separating the identity domains for the control plane and application plane, using tenant-specific user pools, and implementing row-level security with AWS IAM.
- Federated identity and frictionless onboarding are important considerations for enterprise customers.

#### 3. Insufficient Telemetry

- SaaS providers often have an SRE-centric observability story but lack comprehensive telemetry for different roles (FinOps, product development, security, etc.).
- OpenTelemetry provides a flexible and vendor-agnostic approach to emit telemetry data to various destinations (AWS services, third-party tools).
- Observability should surface activity with tenant context to enable tenant-specific troubleshooting and analysis.

#### 4. Revenue Leakage

- SaaS providers may not accurately measure and bill for usage, leading to revenue leakage.
- A flexible billing pipeline with EventBridge, DynamoDB, and integrations with billing providers (Stripe, AWS Marketplace, Amberflo) can address this.
- Tracking entitlements, usage-based pricing, and free trial experiences are important considerations.

#### 5. Underinvesting in Testing

- SaaS providers often lack a comprehensive testing culture, focusing on unit tests and basic integration tests.
- Chaos engineering tools like Gremlin can introduce controlled failures to test application resilience and SLAs under various scenarios.
- Testing should cover tenant isolation, policy enforcement, SLAs, and different workload patterns.

#### 6. Complex Deployments to Customer Accounts

- AI/ML workloads may require deploying infrastructure to customer accounts due to data privacy and compliance requirements.
- Approaches include customer-managed keys, Nitro Enclaves, remote agents, and deploying the entire application to customer accounts.
- Maintaining observability and operational control is crucial when deploying to customer accounts.

### Key Takeaways

- Adopt a comprehensive control plane solution like SBT to manage SaaS operations at scale.
- Implement robust identity and access management practices, including tenant isolation and federated identity support.
- Leverage OpenTelemetry for flexible and vendor-agnostic observability with tenant context.
- Build a resilient billing pipeline to accurately measure and monetize usage.
- Invest in a testing culture, including chaos engineering, to ensure application resilience and SLA compliance.
- Prepare for complex deployment scenarios to customer accounts while maintaining operational control and observability.