# Summary of AWS re_Invent 2024 - Rapid detection and noise reduction using automation (SUP311).txt

# Summary

## Introduction

- The session discusses the challenges faced by security teams in handling a large volume of security alerts and findings, and how AWS Managed Services (AMS) team addressed these challenges using automation and a novel approach of focusing on known good behavior.

## Challenges

- Small security teams with limited resources struggle to triage thousands of security alerts and findings manually.
- Manual triage is time-consuming, taking 3-5 hours per alert, leading to delays in responding to actual threats.
- Cloud environments are dynamic, with resources constantly being created and destroyed, making it difficult to prioritize alerts.
- Manually triaging security alerts is error-prone and lacks precision, leading to missed threats or false positives.

## Proposed Solution

- Aggressively automate the undifferentiated heavy lifting tasks, such as log analysis and threat intelligence lookups.
- Focus on identifying known good behavior patterns instead of solely looking for malicious activity.
- Leverage the scale of AWS and customer data to build knowledge bases of expected behavior patterns.
- Enable security analysts to contribute their domain knowledge by learning coding (e.g., Python) and embedding their investigation techniques into automation.
- Implement a closed-loop system where responders feed their learnings back into the automation to continuously improve detection capabilities.

## Benefits

- Reduced noise-to-signal ratio by hundreds to one, significantly reducing the number of alerts to investigate.
- Freed up security engineers' time to focus on proactive security work and innovation.
- Improved coverage and reduced the likelihood of missing actual threats.
- Enabled continuous learning from security incidents across the customer base.
- Empowered security teams to use their skills more effectively on high-judgment tasks.

## AWS Security Incident and Response Service

- A new service launched by AWS, based on the AMS team's approach and automation capabilities.
- Provides automated monitoring and investigation of security alerts from GuardDuty and third-party tools via Security Hub.
- Offers a console for centralized security incident management and collaboration.
- Provides access to 24/7 specialized security experts for proactive monitoring and incident response.

## Conclusion

The session highlights the power of automation and a novel approach to security monitoring, enabling security teams to focus on high-value tasks and continuously improve their detection capabilities. The newly launched AWS Security Incident and Response Service aims to bring these benefits to AWS customers.