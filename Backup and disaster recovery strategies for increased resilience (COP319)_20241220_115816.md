# Summary of AWS re_Invent 2024 - Backup and disaster recovery strategies for increased resilience (COP319).txt

# AWS re:Invent 2024 - Backup and Disaster Recovery Strategies for Increased Resilience

## Summary

### Introduction

- Backup and disaster recovery strategies have evolved from having a single approach (tape backups) to multiple choices (backup, disaster recovery, resilience, availability, compliance).
- Organizations now have more choices and need to decide the appropriate strategy based on their requirements.

### Key Factors in Choosing a Strategy

- **Shared Responsibility Model**: AWS is responsible for the cloud infrastructure, while customers are responsible for the data and applications in the cloud, including data protection, compliance, and testing.
- **Recovery Point Objective (RPO)** and **Recovery Time Objective (RTO)**: These metrics define the acceptable data loss and downtime for an application or workload.
- **Tiering Applications**: Categorize applications based on their criticality and RTO/RPO requirements, typically into 4 tiers (e.g., Tier 1: mission-critical, Tier 4: non-critical).

### AWS Services for Backup and Disaster Recovery

- **AWS Elastic Disaster Recovery Service (DRS)**: Suitable for Tier 1 and Tier 2 applications, providing continuous data protection, fast recovery, and easy testing. Ideal for mission-critical workloads.
- **AWS Backup**: Suitable for Tier 3 and Tier 4 applications, providing centralized backup management and compliance capabilities. Often used in conjunction with DRS for long-term retention and compliance.

### Best Practices

1. **Tier Applications**: Categorize applications based on business requirements and RTO/RPO.
2. **Test Recovery Capabilities**: Regularly test recovery processes to ensure they work as expected and account for changes in the production environment.
3. **Leave Time for Troubleshooting**: During recovery tests, allocate time for troubleshooting and resolving issues that may arise.
4. **Utilize Multiple Tools**: Leverage both backup and disaster recovery tools based on the threat or issue, as well as compliance requirements.
5. **Implement a Layered Approach**:
   - Local Copy: For tactical recovery within the same Availability Zone.
   - Remote Disaster Recovery Copy: For cross-region or cross-AZ recovery, using DRS for low RTO/RPO.
   - Ransomware Recovery Copy: For cyber resilience and ransomware recovery, using backup vaults and isolated accounts.

### Conclusion

Backup and disaster recovery strategies require careful planning and a combination of tools and approaches based on application requirements, compliance needs, and potential threats. Regular testing and a layered approach are essential for ensuring resilience and minimizing data loss and downtime.