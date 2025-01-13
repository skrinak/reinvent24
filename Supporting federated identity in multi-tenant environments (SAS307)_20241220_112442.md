# Summary of AWS re_Invent 2024 - Supporting federated identity in multi-tenant environments (SAS307).txt

Here is a comprehensive summary of the transcript in Markdown format:

# AWS re:Invent 2024 - Supporting Federated Identity in Multi-Tenant Environments (SAS307)

## Introduction

- The session covers adding federated identity support to multi-tenant SaaS applications.
- Presented by Dhammika Sriyananda and Toby Buckley, senior architects at AWS SaaS Factory.
- Covers design principles, architectural patterns, and implementation details for adding federation to SaaS applications.
- Explores different federation protocols like OpenID Connect and SAML 2.0, using Amazon Cognito as an example.

## Standard SaaS Identity Patterns

### SaaS Application Architecture

- SaaS applications have two main components:
  - Application plane (business logic, microservices, databases)
  - SaaS control plane (shared services for efficient operation)

### SaaS Identity Provider

- The SaaS control plane provides a centralized SaaS Identity Provider (IdP) to manage user identities and identity operations (authentication, authorization).
- User profiles in the SaaS IdP contain:
  - User attributes (username, password, identity details)
  - Tenant ID and tenant context (creating a "SaaS identity")

### Token-Based Implementation

- SaaS IdPs often support token-based identity operations using JSON Web Tokens (JWTs).
- JWTs represent the SaaS identity and can be used for efficient downstream communication with the SaaS application.
- JWTs are managed by the SaaS IdP, encrypted, and have time-to-live (TTL) expiration.

## Motivation for Federated Identity

- Some tenants prefer not to have the SaaS provider manage their employee identities due to security concerns and company policies.
- These tenants want to integrate their corporate Identity Providers (IdPs) with the SaaS application for single sign-on (SSO).
- This motivates adding federated identity support to the SaaS application.

## Federated Identity Workflow

- With federation, tenants use their corporate IdPs for authentication instead of creating users in the SaaS IdP.
- The SaaS IdP (e.g., Amazon Cognito) is still needed to manage federation details and workflows.
- Example federated authentication flow:
  1. User tries to access the SaaS application without a valid session.
  2. Cognito redirects the user to the tenant's corporate IdP for authentication.
  3. User authenticates with the corporate IdP.
  4. Corporate IdP redirects the user back to Cognito with authentication details.
  5. Cognito validates the authentication and authorizes access to the SaaS application.

## Challenges and Considerations

- Coexistence of federation and standard identity workflows in the SaaS application.
- Supporting multiple identity protocols (OpenID Connect, SAML 2.0, etc.) based on tenant preferences.
- Injecting tenant ID and context into federated user identities for downstream automation.
- Compliance and regulations, especially for data residency and sovereignty.
- Cost and quotas for identity operations in federated vs. non-federated scenarios.
- Automating the tenant onboarding process with federation support.

## Implementation

### Tenant Onboarding with Federation

- Circular dependency: Tenant onboarding requires federation configuration, but federation configuration requires tenant onboarding.
- Potential solutions:
  - Two-step asynchronous onboarding process (e.g., OIDC flow)
  - Upfront integration app creation by the tenant (e.g., SAML flow)

### Multi-Tenant Aspects of Cognito

- Pooled model: Sharing resources (user pool, app client) across tenants.
- Siloed model: Dedicating resources (user pool, app client) per tenant.

### Federation Workflow Implementation

- OIDC and SAML federation flows in Cognito.
- Cognito as a federation hub, handling different protocols transparently for the application.
- Creating proxy users and groups in Cognito for federated users.

### Mapping User Attributes

- Mapping tenant IdP user attributes to Cognito user attributes for normalization.
- Injecting tenant ID using Cognito Lambda triggers (e.g., post-confirmation trigger).

### Resolving Federated IdP at Runtime

- Passing `idp_identifier` or `identity_provider` parameters in the `oauth2/authorize` call to dynamically resolve the federated IdP.

### Additional Considerations

- Handling entitlements and user limits using Cognito triggers (e.g., pre-authentication trigger).
- Understanding Cognito from an OAuth2 and OpenID Connect perspective.
- Quotas and resource limits for Cognito resources.
- Pricing differences for federated vs. non-federated users.
- User pools vs. identity pools in Cognito.

## Conclusion

- Federation adds more moving parts but is manageable with Cognito.
- Cognito acts as a federation hub, handling different protocols transparently.
- Cognito triggers provide customization capabilities for various scenarios.
- Mapping and Lambda triggers help reconcile differences between tenant and SaaS user identities.
- Frictionless tenant onboarding is crucial for a successful SaaS business.