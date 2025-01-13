# Summary of AWS re_Invent 2024 - Netflix_s massive multi-account journey_ Year two (NFX402).txt

# Summary

## Title: Netflix's Massive Multi-Account Journey: Year Two

### Main Points:

1. **Background**:
   - Netflix adopted AWS in 2008 and initially grew in a handful of large AWS accounts.
   - To reduce operational and security risks, improve developer experience, and adopt best practices, Netflix decided to migrate to a multi-account architecture.
   - In the previous year (2022), Netflix introduced an innovative approach to decouple IAM roles from AWS accounts containing compute resources, leveraging the strong isolation boundaries of AWS accounts.

2. **Account-Agnostic Credential Delivery**:
   - A foundational capability required for the migration is account-agnostic credential delivery.
   - Netflix built a lightweight OIDC provider and an IMDS proxy to enable the delivery of arbitrary IAM role credentials to workloads, regardless of the account they reside in.

3. **Migration Complexity Assessment**:
   - Netflix assessed migration complexity based on AWS service usage, security risk, and operational risk for each application.
   - Applications with high security risk but low migration complexity were targeted first for maximum risk reduction leverage.

4. **Migration Orchestration Tooling (CAMP)**:
   - Netflix developed the Cloud Application Migration Platform (CAMP) to orchestrate and automate the migration process.
   - CAMP integrates with data sources, Spinnaker (continuous deployment platform), and account vending processes.
   - CAMP performs validation checks to ensure safe migrations and provides an operator interface for managing migrations.

5. **IAM Patterns and Policies**:
   - Netflix leverages a combination of service control policies, resource control policies, permissions boundaries, and attribute-based access control (ABAC) to simplify resource access control and support infrastructure as code.
   - ABAC policies allow for generic resource policies that can be applied ahead of migrations, reducing migration complexity.

6. **Risk Reduction and Progress Measurement**:
   - Netflix measures progress by tracking access exposure (the number of allowed access paths between application roles and resources) and access efficiency (the ratio of intended to actual access).
   - Early migrations provide higher risk reduction leverage, as the marginal risk reduction diminishes as migrations progress.

7. **Learnings and Takeaways**:
   - Designing for minimal application owner interaction has paid dividends.
   - Organizational buy-in and commitment from security and engineering teams have been crucial.
   - Getting into the migration feedback loop as soon as possible and minimizing external dependencies would have accelerated the process.
   - As of the presentation, Netflix has migrated 405 applications and over 1,100 IAM roles, with the largest parallel batch being 277 applications.

### Key Insights and Conclusions:

- Netflix's innovative approach to decouple IAM roles from compute resources has enabled a massive multi-account migration while reducing operational and security risks.
- The development of orchestration tooling (CAMP) and the integration of various data sources, deployment platforms, and account vending processes have been crucial for automating and scaling the migration process.
- Measuring progress through access exposure and access efficiency metrics has provided visibility into risk reduction and guided the prioritization of migrations.
- Leveraging ABAC policies and a combination of IAM patterns has simplified resource access control and supported infrastructure as code adoption.
- Organizational buy-in, dedicated resources, and minimizing external dependencies are critical success factors for such large-scale migration initiatives.

Overall, Netflix's multi-account journey showcases an innovative approach to cloud architecture, leveraging AWS account boundaries and automating complex migration processes to achieve improved security, operational resilience, and developer experience.