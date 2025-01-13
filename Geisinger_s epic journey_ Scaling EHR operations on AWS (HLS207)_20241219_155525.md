# Summary of AWS re_Invent 2024 - Geisinger_s epic journey_ Scaling EHR operations on AWS (HLS207).txt

# Summary

## Introduction
- This session covers Geisinger Health's journey of migrating their Epic electronic health record (EHR) system to AWS cloud.
- Mike Hegyi from AWS provides an overview of the benefits of running Epic on AWS, including reliability, speed, security, and cost optimization.
- Marlin Moyer from Geisinger Health shares their experiences and lessons learned from the migration process.

## Benefits of Running Epic on AWS
- **Reliability**: AWS has the highest service resiliency among cloud providers, ensuring continuous access to patient records.
- **Speed**: Health systems running Epic on AWS have seen at least 20% improvement in average response time and 50% reduction in workflows missing the response time target.
- **Security**: AWS provides HIPAA-eligible and high-trust certified services, while customers maintain control over data access and auditing.
- **Cost Optimization**: AWS allows refreshing infrastructure with newer, faster hardware regularly, leading to cost savings while maintaining performance.

## Geisinger's Epic Migration Journey
- Geisinger partnered with Deloitte and AWS for the migration.
- They started with migrating other clinical applications before moving Epic.
- A training instance was set up and tested thoroughly, including printing and peripherals.
- The production migration was initially planned for a week, but they decided to stay in the cloud after seeing significant performance improvements.
- They performed an Epic upgrade in the cloud, which was not initially planned.
- Geisinger embraced a "watch one, do one, teach one" approach with their partners to ensure knowledge transfer.

## Lessons Learned
- **Preparation**: Understand all data exchange touchpoints and segregate environments with appropriate firewalls and security measures.
- **FinOps**: Establish a FinOps program early in the process to identify and execute cost optimization opportunities continuously.
- **User Experience**: Listen to end-users to ensure their needs are met while optimizing costs.
- **Agility**: Being in the cloud has enabled Geisinger to scale resources quickly for research, integrations, and virtual care initiatives.

## Advice for Others
- Assess capacity and review instance types regularly for optimization opportunities.
- Establish a dedicated FinOps team or program.
- Push for cloud migration if not already done, and work with vendors to leverage new cloud technologies.
- For those running Epic on-premises, consider setting up an isolated recovery environment on AWS to improve resiliency and reduce business risk.
- Leverage AWS training and resources to educate teams on operating Epic in the cloud.

Overall, the session highlights the benefits of running Epic on AWS and shares valuable insights from Geisinger's migration experience, emphasizing preparation, FinOps practices, user experience, and agility as key factors for success.