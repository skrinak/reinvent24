# Summary of AWS re_Invent 2024 - Scaling to new heights_ Coinbase migrates to Amazon EKS and scales 10x (PRO303).txt

Here is a comprehensive summary of the transcript, formatted in Markdown with appropriate headers and bullet points:

# AWS re:Invent 2024 - Scaling to New Heights: Coinbase Migrates to Amazon EKS and Scales 10x

## Introduction

- The session covered Coinbase's 18-month journey to scale their infrastructure 10x while reducing costs and modernizing their compute infrastructure by moving from EC2 to Amazon EKS (Elastic Kubernetes Service).
- The three main business objectives were:
  1. Reducing costs
  2. Scaling to support 10x the amount of traffic
  3. Modernizing the compute infrastructure by moving to a Kubernetes-based architecture

## Phase 1: EC2 x86 to Graviton Migration

- Coinbase migrated from x86 to Graviton instances to reduce EC2 costs by 20%.
- Key challenges and learnings:
  - Emulated builds on x86 hosts doubled build times, so they switched to a batch build pipeline with separate x86 and Graviton hosts.
  - Customer experience matters; they ensured build times remained the same for migrated services.
  - Instance availability was a concern, preventing migration of larger services.
  - The warm pool feature in Auto Scaling groups couldn't be used with multiple instance types.
  - Golang services performed better than Ruby services on Graviton.

## Phase 2: EC2 to EKS Migration

- Coinbase migrated from EC2 to EKS to achieve better bin packing and resource utilization.
- Key actions and learnings:
  - Weekly program and senior management check-ins were crucial for coordination.
  - Team assignments with a Coinbase employee and AWS Professional Services personnel helped build trust and domain expertise.
  - Automated reporting and scripts to estimate cost savings were implemented.
  - High ROI services were prioritized, focusing on low effort, high savings, and low customer impact services first.
  - Migrated 3,500 service configurations in 12 months with the help of AWS Professional Services.
  - Achieved 68% reduction in resources and 50% increase in scaling speeds for migrated services.
  - Centralized scaling buffer in the cluster improved efficiency.

## Phase 3: Graviton EKS Migration

- Coinbase combined the previous two phases by migrating to Graviton-based EKS clusters.
- Key actions and learnings:
  - Updated build pipeline and testing procedures for Graviton EKS.
  - Focused on Golang services first due to better compatibility and performance.
  - Cluster-based sprints were used to maximize wins and build velocity.
  - Re-architected the build pipeline to enable parallel builds and reduce build times.
  - Increased the number of Graviton node pools to prioritize Graviton instances while retaining x86 as a fallback.
  - Achieved 10% additional savings on compute costs and better resiliency with multiple instance types.

## Overall Learnings and Results

- Return on investment (ROI) was crucial, and they focused on high ROI programs.
- Breaking the journey into distinct phases allowed them to learn and carry forward learnings.
- A clear single-threaded leader (Coinbase employee + AWS Professional Services team) helped overcome cultural and trust barriers.
- Achieved massive EKS migration in 12 months, enabling faster and more reliable scaling.
- Proved that ROI-based funding works and achieved aggressive cost-saving goals with the help of AWS Professional Services.
- Coinbase's Cloud Center of Excellence team became experts in flexible workforce management.