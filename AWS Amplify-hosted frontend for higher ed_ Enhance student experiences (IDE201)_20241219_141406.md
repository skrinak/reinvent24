# Summary of AWS re_Invent 2024 - AWS Amplify-hosted frontend for higher ed_ Enhance student experiences (IDE201).txt

# Summary of AWS re:Invent 2024 - AWS Amplify-hosted frontend for higher ed: Enhance student experiences (IDE201)

## Introduction
- The session highlights the cloud journey of UNCF (United Negro College Fund) in building HBCUv, a unique edtech platform for Historically Black Colleges and Universities (HBCUs).
- HBCUs represent 3% of the nation's colleges and universities but produce 20% of all African American graduates, 50% of Black doctors and lawyers, and 80% of Black judges.
- During COVID-19, only 20% of HBCUs had a plan for online education, compared to 56% of all colleges across America.
- HBCUv aims to engage the remaining 65% of HBCU students who could not attend or finish college during their careers.

## HBCUv Platform Overview
- HBCUv is an online platform designed to enhance the student experience and institutional vitality of HBCUs.
- Key features include:
  - The Yard: A virtual space mimicking the campus yard, where students can connect, join groups, and find opportunities.
  - Course Catalog: A shared catalog enabling cross-registration and course articulation across HBCUs.
  - My Path: A personalized student success center with resources, advising, and career opportunities.
  - Future roadmap includes Open Academy (for families of students), Faculty Lounge, and Innovation Lab.

## Design Principles
- The platform was designed based on 3,300 hours of research with nine partnering institutions.
- Key design principles include:
  - Safe space for Black joy and expression
  - Opportunity to find one's tribe and connect with like-minded individuals
  - Honor rituals and traditions
  - Build upon and create new legacies
  - Mobility and guidance for students
  - Celebrate and redefine what it means to be Black in higher education and online

## Technology Stack and AWS Amplify
- The frontend was developed using AWS Amplify and the React framework.
- Amplify provided a streamlined and fully managed hosting platform, enabling accelerated frontend development.
- Key benefits of Amplify include easy setup, built-in authentication, visual development simplified, hosting and CI/CD, backend services integration, and a developer-friendly ecosystem.
- Amplify enabled feature branch deployments, pull request previews, redirects, and custom headers.
- The platform leveraged AWS Step Functions for orchestrating complex user registration and onboarding workflows.
- AWS CloudWatch RUM (Real User Monitoring) was used for performance monitoring and enhancing the frontend application experience.

## Challenges and Approaches
- Data consistency and synchronization across multiple HBCUs
- Maintaining consistent UI/UX design across integrated components
- Data privacy and security, including FERPA compliance
- Communication and coordination with partner institutions
- Performance and scalability during peak usage periods
- User authentication and authorization, including passwordless authentication
- Integration complexity with partner institutions and third-party services
- Strategic integration planning and unified data management
- Shifting security to the left (DevSecOps practices)
- Data governance and security, including consent management
- User journey mapping for different personas
- Serverless-first approach for scalability and cost efficiency

## Conclusion
- HBCUv represents a potential solution to engage and support underserved communities, particularly first-generation Black students.
- The platform leverages technology and a shared service approach to enhance student success and institutional vitality for HBCUs.
- AWS Amplify and other AWS services played a crucial role in enabling the seamless and engaging user experience of the HBCUv platform.