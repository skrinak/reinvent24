# Summary of AWS re_Invent 2024 - Scaling GPU infrastructure and using LLMs for Roblox_s metaverse (GAM312).txt

# Scaling GPU Infrastructure and Using LLMs for Roblox's Metaverse

## Overview

This talk discusses the challenges and solutions implemented by Roblox for scaling their GPU infrastructure to support AI and large language model (LLM) workloads in their metaverse platform. The speaker, Denis Goupil, shares insights into their journey of GPU scheduling on an EKS (Elastic Kubernetes Service) cluster environment.

## Context

- Roblox is a creation platform and an immersive 3D generation platform where creators build experiences for players.
- AI use cases at Roblox include safety (text and voice filtering, bot detection, abuse reports), creator assistance (code and documentation assistance, generative AI for avatar setup), player recommendations, and scene generation.
- The AI platform at Roblox aims to democratize AI by providing a golden path from ideation to production for ML engineers and data scientists.

## Challenges

1. **Kubernetes not designed for AI workloads:** Kubernetes was designed for web server applications, where workloads are spread across multiple nodes, which is not ideal for AI workloads.
2. **GPU type heterogeneity:** Different GPU types (e.g., T4, H200) have varying capabilities, but Kubernetes treats them similarly.
3. **Budget and cost constraints:** Teams work within budget constraints, and cloud providers have limited on-demand resources for high-end GPUs (e.g., A100, H100).
4. **Resource fragmentation:** Kubernetes' default scheduling can lead to inefficient resource utilization, requiring additional nodes for new workloads.

## Version 1: GPU as Pets

The initial solution treated GPUs as "pets" (precious resources) and involved:

- Capacity reservations on AWS to ensure availability of high-end GPUs.
- Instance owner nodes for teams to guarantee access to their reserved capacity.
- Modified Kubernetes scheduler to bin-pack workloads on nodes (MostAllocated strategy).
- Custom preemption plugin to reclaim instance owner nodes when needed.
- GPU type tiering (e.g., A10 or better) and workload tiering (Tier-0: instance owner, Tier-1: shared pool, Tier-2: preemptible).

While an improvement, this approach still had inefficiencies, preemption issues, and high operational costs.

## Version 2: GPU as Cattle

The second iteration treated GPUs as "cattle" (disposable resources) and focused on:

- Better monitoring and dashboards for pending time, preemption, and tiering.
- Abandoning instance owner nodes in favor of shared resources.
- Moving from fixed quotas to quota-as-code with GPU types.
- Minimizing user experience changes and enforcing good behavior (e.g., proportional CPU/memory requests).

The solution involved:

- Using YuniKorn for virtual queues and scheduling workflows.
- Custom webhook for injecting YuniKorn annotations and enforcing policies.
- Bin-packing workloads on available nodes.
- Culling idle workloads (notebooks, training jobs) to save costs.

## Results

The version 2 approach led to significant improvements:

- Increased bin-packing efficiency (unused GPUs consolidated on empty nodes).
- Reduced percentage of nodes needed for Tier-0 workloads, freeing capacity for other tiers.
- Near-zero pending time for workloads.
- Elimination of preemption due to free node availability.
- Ability to fulfill new resource requests immediately, reducing lead time for capacity procurement.

## Next Steps

Roblox plans to further optimize their GPU infrastructure by:

1. Adjusting capacity reservations based on actual usage patterns rather than requested resources.
2. Improving GPU efficiency by closing the gap between available, allocated, and utilized GPUs.
3. Implementing dynamic rescheduling to bin-pack workloads on-demand as they complete.

Overall, the talk highlights Roblox's journey in scaling their GPU infrastructure to support AI and LLM workloads efficiently while addressing challenges around resource utilization, cost optimization, and user experience.