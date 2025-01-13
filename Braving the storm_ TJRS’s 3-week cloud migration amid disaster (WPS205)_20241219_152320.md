# Summary of AWS re_Invent 2024 - Braving the storm_ TJRS’s 3-week cloud migration amid disaster (WPS205).txt

# AWS re:Invent 2024 - Braving the Storm: TJRS's 3-Week Cloud Migration amid Disaster

## Overview

This session recounts the remarkable story of the Court of Justice in Porto Alegre, Brazil, and their successful migration to the AWS cloud in just 21 days amidst a devastating flood. The speakers share the challenges faced, lessons learned, and the crucial role of AWS support and solutions in enabling this rapid migration.

## Main Points

### The Disaster and Its Impact

- Porto Alegre was hit by the biggest flood in the city's history, causing widespread damage and disruption.
- The Court of Justice's two data centers were rendered inoperable, one flooded and the other running on generators with limited fuel supply.
- The court's critical system, eproc, with over 350,000 users, 384 million documents, and 10 TB of data, was at risk of going offline.

### The Migration Timeline

- May 2nd: Water levels rose rapidly, prompting the decision to switch to the secondary data center.
- May 3rd: The main data center was flooded, and the court building was evacuated.
- May 4th: Both data centers were shut down, leaving the court systems offline for 24 hours.
- May 5th: The decision was made to migrate eproc to the AWS cloud.
- Within 21 days, eproc was fully operational on AWS, an astonishing feat.

### Key Lessons Learned

1. **Break the problem into chunks and assign dedicated owners**: The migration was divided into five squads: application, financial, database, documents, and integration.
2. **Choose solution-driven leaders**: Leaders with a positive, solution-oriented mindset were crucial in overcoming skepticism and driving progress.
3. **Have contingency plans beyond Plan B**: In highly critical situations, having multiple backup plans is essential for success.
4. **Maintain clear and consistent communication**: Regular checkpoints and alignment among all stakeholders were vital.
5. **Choose the right partners**: AWS, Serpro, and Hitachi provided essential support and expertise.
6. **Foster a strong sense of purpose**: Despite personal challenges, the team's commitment to keeping justice accessible during the crisis drove their efforts.

### AWS Support and Solutions

- **AWS Disaster Response**: A strategic pillar within AWS, providing credits, innovation investments, and specialized technical support during disasters.
- **AWS Professional Services**: Experienced professionals with deep AWS knowledge guided critical architecture, security, and reliability decisions.
- **AWS Solutions Architects**: Allyson Oliveira, an AWS Solutions Architect, provided tailored guidance based on the customer's specific needs.
- **AWS Partners**: Partners like Serpro and Hitachi played crucial roles in scaling and delivering the migration.

### Technical Challenges and Solutions

1. **Moving Objects (Documents and Files)**: AWS DataSync was used to identify and copy modified files from on-premises storage to Amazon S3.
2. **Migrating Databases**: AWS Database Migration Service (DMS) and Percona backup software were used, with data eventually migrated to Amazon Aurora for its performance and scalability benefits.
3. **Migrating Servers**: Initially, fresh installations were attempted, but the plan pivoted to converting VMware OVA files to Amazon Machine Images (AMIs) for faster deployment.

### Final AWS Architecture

The migrated eproc system leveraged various AWS services for security (AWS WAF, AWS Shield, Amazon Route 53, Amazon GuardDuty), infrastructure (Application Load Balancer, Amazon EC2, Amazon Aurora), caching (Amazon ElastiCache), backup (AWS Backup), and shared storage (Amazon EFS, Amazon S3).

## Key Takeaways

- Strong leadership, effective communication, improvisation, and a shared sense of purpose were critical success factors in this rapid migration.
- AWS Disaster Response and the expertise of AWS teams and partners played a vital role in enabling the court's systems to remain operational during the crisis.
- Leveraging AWS services like DataSync, DMS, Aurora, and EC2 allowed for efficient data migration and scalable infrastructure deployment.
- The migration showcased the resilience and adaptability of the team, overcoming numerous challenges to achieve their mission of keeping justice accessible.