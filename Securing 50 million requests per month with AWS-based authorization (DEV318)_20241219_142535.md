# Summary of AWS re_Invent 2024 - Securing 50 million requests per month with AWS-based authorization (DEV318).txt

# AWS re:Invent 2024 - Securing 50 million requests per month with AWS-based authorization (DEV318)

## Summary

The presentation covers how the team at Simply Business, a UK-based insurance broker, implemented authorization using Amazon Verified Permissions (AVP) and the Cedar open-source policy language. The main points and key insights are:

### External Role-Based Access Control (Gateway Access Control)

- Implemented role-based access control at the API Gateway level for external partners using Lambda authorizers and AVP.
- Created configuration JSON to simplify the process for developers, automatically mapping to Terraform configurations.
- Utilized caching at the API Gateway level to reduce the number of AVP requests.
- Leveraged release tests to validate policies against AVP before deployment.

### Internal Attribute-Based Access Control (Resource Access Control)

- Initially planned to use a single policy store for all resources but faced challenges due to unsupported Cedar operators in AVP.
- Ended up using separate policy stores for different resource types (RFQ, Policy, External Policy).
- Developed a Ruby gem (SB Authorization) to handle authorization across multiple resource servers, following the hexagonal architecture pattern.
- Utilized Cedar CLI for local testing and payload validation against the Schema, increasing confidence during development.
- Employed Backstage templates for easy rollout across multiple projects.

### Internal Role-Based Access Control (Service Access Control)

- Implemented role-based access control between internal applications for zero-trust security.
- Enhanced the existing token house library to handle authorization in addition to JWT token generation.
- Utilized configuration files to define authorized endpoints and policy stores for each application and environment.
- Employed caching extensively, reducing AVP costs by 93% through optimized cache key generation.

### Key Insights and Lessons Learned

- Differences between Cedar and AVP versions, syntax, and supported features posed challenges.
- Caching played a crucial role in reducing AVP costs, which can be expensive for high-volume requests.
- Hexagonal architecture and Backstage templates facilitated easier rollout and maintenance.
- AVP lacked features like search, sorting, and tagging for policy stores, making management difficult.
- Cedar CLI proved to be a game-changer for local testing and payload validation.

### Additional Resources

- The presenter created an AVP-CLI tool for learning and experimentation.
- A blog post series covering Cedar, AVP, and various use cases is available.
- The Cedar GitHub organization and Slack community provide additional resources and support.

Overall, the presentation showcased the team's journey in implementing authorization at scale using AWS services and open-source tools, highlighting the challenges faced, solutions implemented, and lessons learned along the way.