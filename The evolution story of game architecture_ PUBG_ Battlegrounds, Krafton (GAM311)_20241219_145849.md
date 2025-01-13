# Summary of AWS re_Invent 2024 - The evolution story of game architecture_ PUBG_ Battlegrounds, Krafton (GAM311).txt

# Summary of AWS re:Invent 2024 - The evolution story of game architecture: PUBG: Battlegrounds, Krafton (GAM311)

## Introduction

This session covers the modernization journey of PlayerUnknown's Battlegrounds (PUBG), a popular online multiplayer game developed by KRAFTON. The focus is on how KRAFTON migrated PUBG's architecture to a fully containerized environment using Amazon Elastic Kubernetes Service (EKS) and the lessons learned during the process.

## Modernization Overview

### What is Modernization?

- Transforming an application environment to be more agile, elastic, and highly available.
- It involves incremental technology and architectural adoption, people and process transformation, and scaling operations and governance.

### Modernization Pathways

- KRAFTON chose the container pathway, re-architecting PUBG on top of Amazon EKS.
- They further moved EKS worker nodes to AWS Graviton for better price-performance optimization.

## PUBG's Modernization Journey

### Initial Architecture (2017)

- PUBG was hosted on Windows-based EC2 Auto Scaling groups, deployed and managed by Terraform.
- It had two main components: the lobby server (web services) and the GameServer (managing player states).

### Challenges

- Inefficiencies, decreasing productivity, and limited operational agility due to the initial architecture.
- Frequent updates to Terraform code and infrastructure maintenance strained the DevOps team's resources.

### Modernization Steps

1. **Lobby Server Migration**
   - QA environment migrated to containers in November 2018.
   - Production environment migrated to a fully containerized environment in October 2019.

2. **GameServer Migration**
   - GameServers re-architected and migrated to containers in July 2021.

3. **Lobby Server Migration to AWS Graviton**
   - Lobby servers migrated to AWS Graviton-based worker nodes for cost optimization.

## Lessons Learned

### QA Environment Modernization

- Goals: Efficient resource provisioning, standard and scalable solution, and self-service environment management.
- Solution: Containerized QA environment managed with Kubernetes, using a web UI tool for self-service.

### Production Environment Migration

- Focus on traffic control and load balancing for graceful migration.
- Adopted Istio as a service mesh for traffic management and observability.

### GameServer Migration

- Adopted Agones for GameServer orchestration and lifecycle management.
- Reduced instance costs through efficient resource bin-packing.
- Challenges: Initial bootstrapping delays and resource contention during initialization.
- Solutions: Karpenter for node management, ECR proxy registry, and ImagePuller DaemonSet.

### AWS Graviton Adoption

- Migrated lobby server to AWS Graviton for cost optimization (35% cost savings).
- Challenges: Different virtual core utilization and higher CPU usage on ARM architecture.

### Key Lessons

- Focus on what matters by utilizing AWS Managed Services and open-source software.
- Be aware of potential side effects during migration.
- Prepare for rollbacks and have a plan to address unexpected issues.

## AWS Support and Collaboration

- Countdown program for Enterprise Support customers, providing assistance during major changes.
- Operational reviews and workshops for Enterprise Support customers at no additional cost.
- Engaging with the AWS account team to provide feedback and drive service improvements.

## Conclusion

KRAFTON's modernization journey highlights the benefits of containerization, Kubernetes adoption, and leveraging AWS services like EKS and Graviton. The session emphasizes the importance of focusing on core tasks, being prepared for challenges, and collaborating with AWS for support and service improvements.