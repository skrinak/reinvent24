# Summary of AWS re_Invent 2024 - How developers can self-remediate AWS Security Hub findings (DEV216).txt

# AWS re:Invent 2024 - How Developers Can Self-Remediate AWS Security Hub Findings

## Summary

### Background and Objectives

- The company, Kaminashi, provides multiple products, each with its own services and environments (development, staging, production).
- Security Hub is enabled, and findings are consolidated in an audit account.
- The responsibility for securing each service lies with the respective engineering team.
- The security engineering team's mission is to enable and empower the developers, not directly secure the products.
- The goal is to build a security culture where developers maintain constant security awareness during development, design, and operations.
- Speed and agility are prioritized, but with a minimal level of security.
- Developers should recognize and take action on security issues, rather than relying solely on the security team.

### The "Liver" System

- The "Liver" system was developed to achieve the above objectives.
- It aggregates Security Hub findings from various accounts and sends notifications to on-call developers.
- Developers can set minimum severity levels for notifications (e.g., critical, high).
- Three main concepts:
  1. **Explanation Tickets**: Provide information on why an action is necessary and how to address the issue.
  2. **Individual Responsibility**: Notifications are sent to individual developers, ensuring accountability.
  3. **Risk Management**: Severity levels from Security Hub findings are used as risk values.

### Key Features and Operations

- Security Hub configurations and automations are essential for proper operations.
- Prototype accounts are used for development, with disabled Security Hub controls.
- Liver pages the on-call developer, who creates a ticket and seeks approval from the CTO if no action is required.
- If approved, the finding is marked as "Suppressed" in Security Hub.
- A ramp-up period allows engineering teams to tag resources to be ignored by Liver.
- Resource tagging is monitored to understand the context and reasons for ignoring findings.
- Autoscaling resources are tagged to avoid repeated notifications.

### Outcomes and Learnings

- Operational design took significant time and discussion within the security engineering team.
- Initial deployment in a production environment reduced 17 critical findings to zero in the first week.
- Shift-left approach is recommended to introduce Liver early and take action before production release.
- Tagging resources during the ramp-up period helps manage findings in long-standing services.
- Continuous improvement is needed to create a more secure and robust environment.

## Key Insights and Conclusions

- Empowering developers with security ownership and accountability is crucial for building a security culture.
- Providing context, explanations, and actionable steps enables developers to self-remediate security findings.
- Automations and configurations in Security Hub are essential for efficient and effective operations.
- Risk management should consider the severity of findings and the context of the environment.
- A gradual approach, with ramp-up periods and resource tagging, can help manage findings in existing environments.
- Continuous improvement and collaboration between security and engineering teams are necessary for maintaining a secure and agile environment.