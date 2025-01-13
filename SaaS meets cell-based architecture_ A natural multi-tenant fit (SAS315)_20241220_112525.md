# Summary of AWS re_Invent 2024 - SaaS meets cell-based architecture_ A natural multi-tenant fit (SAS315).txt

# AWS re:Invent 2024 - SaaS meets cell-based architecture: A natural multi-tenant fit (SAS315)

## Summary

### Introduction

- The speaker, Todd Golding, is a Solutions Architect at AWS, focused on the SaaS domain for the past 8-9 years.
- SaaS architectures have diverse deployment models, needs, and requirements, making it challenging to find a one-size-fits-all solution.
- The talk aims to explore the intersection between multi-tenancy principles and cell-based architecture, introducing a new deployment model for SaaS applications.

### The Challenges of Multi-Tenant SaaS Architectures

- Workload profiles of tenants can vary significantly, making it difficult to determine scaling strategies, resilience, and isolation.
- Technology considerations, such as compute stacks (EKS, serverless), storage (RDS, serverless), and business requirements (domain, compliance, regulations), add complexity.
- Addressing principles like noisy neighbor, isolation, and consumption optimization is challenging.
- Deployment models often involve a mix of siloed, pooled, and tiered environments, complicating the overall architecture.
- Multi-region deployments and distributed footprints introduce additional complexity.

### Cell-Based Architecture: A New Approach

- Cell-based architecture introduces a logical construct for grouping tenants, enabling better scaling, resilience, and deployment flexibility.
- Cells can be pre-provisioned or provisioned on-demand based on load, offering different strategies for tenant placement.
- Cells have a lifecycle, requiring rebalancing and tenant movement as workloads change.
- Onboarding tenants involves determining the appropriate cell placement and managing the tenant-to-cell mapping.
- Cells can encapsulate the lifecycle of resources required for tenant onboarding, or rely on the control plane for provisioning.
- Deployments within cells need to consider the mix of siloed and pooled resources, and the responsibility for deployment can be distributed between the control plane and the cell.
- Routing becomes more complex, requiring indirection to map tenants to cells and potentially additional routing within cells for siloed resources.
- Cell-based architectures naturally address noisy neighbor issues, tenant isolation, and resilience by containing blast radiuses within cells.
- Operational considerations include cell-specific telemetry, visibility, and monitoring.

### Choosing a Cell-Based Strategy

- The decision to adopt a cell-based architecture should be driven by business needs, such as scaling requirements, multi-region deployments, noisy neighbor issues, or tiering strategies.
- Architects must articulate the value proposition of cell-based architectures to the business.
- Trade-offs between complexity and value must be evaluated, considering factors like over-provisioning, deployment flexibility, and indirection overhead.

### Conclusion

- Cell-based architectures represent a new model for SaaS deployments, offering advantages but also introducing additional complexity.
- The talk aims to encourage architects to consider cell-based architectures as an option when designing multi-tenant SaaS solutions.
- Further exploration, discussion, and refinement of cell-based architecture patterns are expected in the future.

### Additional Resources

- The speaker mentioned several related sessions, workshops, and a book on multi-tenant SaaS architectures at the conference.
- Attendees are encouraged to provide feedback through surveys to help shape future content on this topic.