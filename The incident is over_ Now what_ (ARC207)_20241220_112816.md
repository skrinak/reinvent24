# Summary of AWS re_Invent 2024 - The incident is over_ Now what_ (ARC207).txt

# Summary

## Main Points and Key Insights

### Incident Handling and Response

- AWS has a comprehensive system for detecting, engaging, and mitigating incidents across multiple services.
- Detection is done through monitoring metrics, alarms, synthetic monitoring (canaries), and aggregate alarms for issues impacting multiple services.
- Engagement involves bringing together relevant teams, AWS support, and incident commanders on a tech call to coordinate the response.
- Mitigation focuses on shifting away from failures, rolling back changes, restarting services, scaling up proactively, and making code changes if needed.
- Communication with customers is a priority, balancing accuracy, detail, and speed through personalized dashboards and notifications.

### Post-Incident Analysis

- AWS conducts comprehensive post-incident analyses (COEs) written by the teams closest to the failed components.
- COEs cover impact summaries, root causes, observations, learnings, and action items to prevent recurrence.
- Empathy is crucial in understanding the decisions made during the incident and the context at the time.
- AWS has a weekly ops meeting to review COEs, share learnings across the organization, and drive centralized changes or programs.

### Scaling Learnings and Improvements

- Learnings from incidents are scaled across AWS through the weekly ops meeting, centralized changes, and codifying tenets (principles) for the entire organization.
- AWS builds new services or features (e.g., Route 53, Load Balancers, Certificate Manager, Zonal Shift) based on learnings from operating at scale.
- AWS continuously improves practices, such as adaptive retries in SDKs, based on insights from analyzing incidents.

## Important Conclusions

- Effective incident response requires a balance between quick mitigation and thorough root cause analysis.
- Sharing learnings across the organization and scaling improvements is crucial to prevent recurring issues.
- Empathy and creating a safe space for teams involved in incidents foster transparency and continuous improvement.
- Codifying tenets and principles helps align teams and guide decision-making during incidents.
- AWS leverages its own operational experiences to build services and features that benefit customers.