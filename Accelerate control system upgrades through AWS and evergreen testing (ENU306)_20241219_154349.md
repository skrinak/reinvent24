# Summary of AWS re_Invent 2024 - Accelerate control system upgrades through AWS and evergreen testing (ENU306).txt

Here is a comprehensive summary of the transcript in Markdown format:

# AWS re:Invent 2024 - Accelerate Control System Upgrades through AWS and Evergreen Testing

## Introduction

- The energy industry is undergoing massive change due to decarbonization of supply, increasing electricity demand, and decentralization.
- These changes are putting pressure on the grid to operate reliably and accommodate renewables while mapping supply to demand.
- AWS has a dedicated business unit, AWS for Energy & Utilities, focused on solving unique challenges in this industry.
- AWS provides industry-specific solutions, guidance, security and compliance support, data strategy assistance, and a partner network.
- AWS hybrid cloud offers a consistent experience across on-premises, cloud, and edge environments, addressing regulatory requirements and low-latency needs.

## GE Vernova's Solution: GridOS and Evergreen Testing

- GE Vernova, a spin-out from the company that invented the grid, is helping utilities manage the rapidly changing operating environment.
- They developed GridOS, a modular, composable, modern, and AI-based software platform for grid management.
- The Evergreen testing model allows frequent software releases, with a cloud instance validated for each customer, then deployed on-premises.
- This reduces the deployment time from 18-36 months to less than 3 months, enabling utilities to keep pace with changes.
- GE Vernova partnered with AWS to build the necessary tooling, processes, and platforms for Evergreen testing.

## PPL's Implementation and Experience

- PPL is implementing GE Vernova's solution for their Advanced Distribution Management System (ADMS).
- In their Customer Reference Environment (CRE), they mirror the production environment for testing and validation.
- The CRE allows PPL to perform failover testing, integration testing, and operator experience testing.
- Deployment times have been reduced from days to around 7-8 hours, enabling frequent testing and validation.
- Test automation is a key focus, with GE and PPL collaborating on automated test scripts.
- The model and configuration are updated monthly, with a pipeline planned for seamless synchronization between CRE and production.
- PPL is exploring AWS Outposts for a hybrid on-premises and cloud deployment, further streamlining the process.

## Benefits and Conclusions

- The Evergreen testing model enables utilities to consume and deploy new software rapidly, addressing the pace of change in the industry.
- It reduces installation times by 92% and test times by 96%, allowing utilities to keep up with emerging challenges.
- AWS partnership and services, such as AppStream and Outposts, have accelerated the development and deployment of this solution.
- The consistent tech stack across on-premises, cloud, and edge environments helps address skills gaps and simplifies the overall process.
- The solution aims to enable utilities to maintain reliable and affordable electricity supply while accommodating the ongoing energy transition.