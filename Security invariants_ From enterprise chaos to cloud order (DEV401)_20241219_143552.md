# Summary of AWS re_Invent 2024 - Security invariants_ From enterprise chaos to cloud order (DEV401).txt

# AWS re:Invent 2024 - Security Invariants: From Enterprise Chaos to Cloud Order

## Summary

Chris Farris and Rich Mogull presented a comprehensive session on security invariants, which are preventative controls that always hold true for your business. The key points and insights are as follows:

### Introduction to Security Invariants

- Security invariants are preventative controls that are always true for your business, reducing the security burden and providing consistency.
- They are enforceable, specific, realistic, and avoid exceptions.
- Invariants can be implemented using various AWS services like Service Control Policies (SCPs), Resource Control Policies (RCPs), and Declarative Policies.

### Enforcing Invariants

- SCPs apply to identities (users and roles) within your AWS Organization.
- RCPs apply to all identities and resources in your accounts, regardless of the organization.
- Declarative Policies enforce configurations outside of IAM, like blocking public access.
- Permission Boundaries define the maximum permissions for IAM roles or users within an account.

### Writing and Deploying Invariants

- Define the invariant in plain language, specifying personas, actions, resources, and conditions.
- Leverage AWS Identity Center for role-based access and SIEM for monitoring invariant violations.
- Test invariants thoroughly before deployment to avoid breaking production workloads.
- Store invariants as Infrastructure as Code (IaC) for reproducibility and transparency.
- Organize accounts into Organizational Units (OUs) like Workloads, Exceptions, Onboarding, Nursery, and Suspended.

### Key Conclusions

- Security invariants provide a consistent and enforceable way to reduce the security burden and prevent common mistakes.
- Proper planning, testing, and communication are crucial for successful invariant implementation.
- AWS offers various services and features to implement and manage security invariants effectively.

Overall, the session provided valuable insights and practical examples for implementing security invariants in AWS environments, emphasizing the importance of preventative controls and reducing the security overhead for development and operations teams.