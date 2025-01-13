# Summary of AWS re_Invent 2024 - Running a complex design environment on AWS (MFG205).txt

# AWS re:Invent 2024 - Running a Complex Design Environment on AWS (MFG205)

## Introduction

This session covered the journey of Samsung Electronics in building a design platform for their semiconductor fabrication (FAB) construction projects on AWS. The speakers, Changhee Park and Yeongyu Hwang, shared insights from an end-user perspective, highlighting the challenges, solutions, and outcomes achieved.

## Key Points

### Design Platform Overview

- Design work in industries like semiconductor manufacturing involves complex data sharing, collaboration among multiple teams, and stringent security requirements.
- A design platform addresses challenges related to productivity, security, and management by providing a centralized space for designers to work efficiently while ensuring data consistency and access control.
- AWS offers a comprehensive suite of services to build such a platform, including networking, storage, computing, virtualization, orchestration, and collaboration tools.

### Samsung's Journey

#### Challenges

- Traditional on-premise IT systems led to data silos among stakeholders, causing costly issues during construction.
- FAB design and construction projects are highly complex, with strict security requirements and frequent changes due to evolving chip technologies.
- Providing a seamless user experience and high performance for resource-intensive design applications was crucial.

#### Solutions

- Adopted a cloud-based approach using AWS to overcome limitations of on-premise systems.
- Implemented a data lake concept to integrate data management and enable collaboration.
- Utilized AWS services like Amazon EC2, Amazon FSx, Amazon DCV, AWS Directory Service, and AWS Security Services.
- Developed a custom portal for self-service provisioning of virtual desktops and SaaS accounts.
- Implemented automation for resource provisioning, user management, and cost optimization.
- Integrated on-premise Active Directory with the cloud platform for consistent user information and access control.
- Leveraged SaaS solutions like Autodesk for web-based drawing and data modeling.
- Employed security monitoring via SIEM (Security Information and Event Management) servers.

#### Outcomes

- Enabled handling of graphic-heavy workloads using Amazon EC2 instances optimized for graphics and Amazon DCV.
- Achieved granular control and automation of platform infrastructure through APIs.
- Maintained security robustness and corporate compliance by implementing dedicated security controls.

### Future Plans

- Continuous performance optimization by adopting newer instance types.
- Integration of AI and ML algorithms for data interpretation and decision support.
- Ongoing cost optimization efforts to make the platform more cost-effective.

## Conclusion

Building a complex design platform on AWS allowed Samsung Electronics to overcome limitations of traditional on-premise systems, enabling collaboration, data integration, and efficient design workflows while maintaining security and corporate compliance. The comprehensive AWS services and solutions empowered Samsung to address challenges related to productivity, performance, and management in their FAB construction projects.