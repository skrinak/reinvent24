# Summary of AWS re_Invent 2024 - Replatforming for reinvention_ Modernizing mainframes at Goldman Sachs (FSI312).txt

# Summary

## Introduction

- This session discusses Goldman Sachs' journey of migrating and modernizing their mainframe-based InvestOne application to the AWS cloud.
- The primary driver for the migration was the need to scale the application horizontally to accommodate business growth of 30% annually.
- The chosen approach was "replatforming," which involves lifting and shifting the application to the cloud without changing the application logic or binaries.

## Business Context

- Goldman Sachs' Asset Management division oversees more than $2 trillion in assets under supervision.
- The InvestOne application, provided by FIS, is a critical system for portfolio accounting, creating investment book records, and managing shadow books.
- InvestOne runs on a mainframe along with Goldman's proprietary COBOL orchestration layer, which encapsulates InvestOne for their unique use cases.

## Legacy Architecture

- The legacy architecture was a monolithic mainframe system, including the application, SDLC, security, monitoring, storage, and database.
- Data interactions occurred via batch file transfers (SFX) and real-time messaging (MQ).
- Challenges included vendor pressure to migrate, high costs, integration complexity, and sourcing skilled COBOL developers.

## Reinvented Architecture on AWS

- The core components were migrated to an emulator (NTT Data) running on EC2 instances with EBS volumes for storage.
- Other components like databases, scheduling, and security were extracted and replaced with AWS services like RDS, Lambda, and EventBridge.
- Resiliency was achieved by deploying the infrastructure across two AWS regions, with EBS volumes replicated using AWS Disaster Recovery Service (DRS).
- Data transfer patterns were standardized using AWS services like S3, SNS, CloudWatch, and AWS Systems Manager (SSM) for automation and control.

## SDLC and Development

- A new SDLC process was built using tools like Nix, Coder, VS Code, and GitLab, tailored for COBOL developers.
- Multiple environments (dev, UAT, prod) were created with varying costs by tokenizing the infrastructure code.
- Data transfer between accounts was secured using a three-key, three-snapshot process, with strict access controls and logging.

## Lessons Learned

- Getting the application running on the emulator was the first step, followed by recreating the entire environment.
- Consistent interfaces were maintained to reduce the blast radius of changes.
- A pragmatic approach of lift-and-shift was successful, with plans for further modernization in the future.

## Key Insights

- Replatforming accelerated the mainframe migration while enabling future modernization on the cloud.
- Standardized design patterns and automation tools simplified the migration process and improved control and auditability.
- Close collaboration with AWS teams and internal stakeholders was crucial for overcoming challenges and pushing boundaries.

## Conclusion

The session demonstrated how Goldman Sachs successfully migrated their critical mainframe application to AWS, addressing scalability and cost challenges while maintaining business continuity and data security. The replatforming approach, combined with standardized patterns and automation, enabled a smooth migration and set the stage for future modernization efforts.