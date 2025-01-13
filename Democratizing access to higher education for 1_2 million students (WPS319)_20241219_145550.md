# Summary of AWS re_Invent 2024 - Democratizing access to higher education for 1_2 million students (WPS319).txt

# AWS re:Invent 2024 - Democratizing Access to Higher Education for 1.2 Million Students

## Summary

This presentation showcased how AWS helped the Brazilian Ministry of Education (MEC) migrate the Unified Selection System (SISU) to the AWS Cloud. SISU is a platform that allows students across Brazil to apply for admission to public universities nationwide, promoting accessibility and reducing social disparities.

### Key Points

- **SISU Background**
  - Implemented in 2010 by MEC
  - Allows students to apply to different universities without traveling for entrance exams
  - Incorporates affirmative action policies, reserving spots for students from public schools, low-income families, and racial minorities
  - Impacts millions of students every year

- **Migration Objectives**
  - Cost reduction
  - Return process management to MEC
  - Improve performance and scalability
  - Ensure supplier and component compatibility
  - Availability of dedicated support resources

- **Architecture**
  - Highly scalable, secure, and reliable architecture deployed across multiple Availability Zones
  - Leveraged various AWS services, including Amazon Route 53, Amazon CloudFront, Amazon EC2, Red Hat OpenShift, AWS WAF, Amazon GuardDuty, AWS Security Hub, and AWS Shield Advanced
  - Multi-account structure within AWS Organizations for proper governance and control
  - Implemented infrastructure as code using GitLab for automation and consistency

- **Security and Resilience**
  - Implemented a comprehensive security strategy with AWS IAM, AWS Shield Advanced, Amazon CloudWatch, AWS GuardDuty, AWS Trusted Advisor, and AWS Config
  - Conducted Shield Response Team fire drills to test DDoS attack detection and response measures

- **Performance and Load Testing**
  - Conducted comprehensive performance and load tests simulating diverse user patterns
  - Exceeded expectations, handling up to 20,000 requests per second with 150,000 concurrent users
  - API latency remained below one second, with zero failures

- **AWS Countdown Framework**
  - Followed the AWS Countdown framework for large-scale events, including planning, reviewing, risk mitigation, and post-event recap
  - Utilized the AWS Well-Architected Framework to ensure a solid foundation

- **Results and Next Steps**
  - Successful go-live with over 104,000 candidate accesses and 11,000 registrations per minute
  - Zero downtime during the four-day execution window
  - 1.4 million students made over 2.4 million registrations for 260,000 vacancies across 107 universities
  - Future plans include regular Well-Architected reviews, operational efficiency improvements, autoscaling, automation, and application modernization

## Conclusion

The migration of SISU to AWS demonstrated the power of the AWS Cloud in delivering a highly scalable, secure, and reliable platform for critical educational applications. By leveraging various AWS services and following best practices, MEC successfully democratized access to higher education for over 1.2 million students in Brazil.