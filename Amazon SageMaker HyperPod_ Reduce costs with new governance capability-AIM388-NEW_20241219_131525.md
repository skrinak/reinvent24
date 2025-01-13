# Summary of AWS re_Invent 2024-Amazon SageMaker HyperPod_ Reduce costs with new governance capability-AIM388-NEW.txt

# Summary

## Amazon SageMaker HyperPod Task Governance

### Introduction

- The advent of generative AI led to rapid growth in model sizes and dataset sizes, resulting in challenges like data collection, cluster provisioning, infrastructure stability, and distributed training strategies.
- Amazon SageMaker HyperPod was introduced to address these challenges, enabling resilient environments, easier distributed training, and better resource utilization control, reducing training time by up to 40%.

### Key Features and Benefits

- **Dynamic Compute Allocation**: Enables dynamic allocation of compute resources across teams while maintaining budgets.
- **Task Prioritization**: Ensures high-priority tasks get prioritized over low-priority tasks during resource contention.
- **Real-time Monitoring**: Provides real-time monitoring and auditing of compute resource utilization and governance for administrators.
- **Increased Utilization and Cost Reduction**: Increases utilization of compute resources and reduces costs by up to 40%.

### Use Cases

- **Resource Management**: Set budgets and allocate quotas to teams.
- **Dynamic Allocation**: Teams can burst into idle compute when needed.
- **Task Orchestration**: Tasks are guaranteed compute per quotas, with preemption and prioritization.
- **Real-time Monitoring**: Monitor cluster health, team allocations, utilization, and waiting tasks.
- **Cost Optimization**: Inputs enable administrators to optimize cluster costs.

### Articul8 AI's Experience

- Articul8 AI is a generative AI platform company that faced challenges in managing GPU resources and fine-tuning models at scale.
- HyperPod Task Governance helped Articul8 AI automate processes, optimize GPU utilization, handle interruptions, prioritize tasks, manage costs, and track resource allocation and utilization.
- With HyperPod, Articul8 AI could develop a new SaaS product (A8 Essential) in just 2-3 months, which would have been difficult without the task governance capabilities.

### Conclusion

Amazon SageMaker HyperPod Task Governance enables organizations to maximize accelerator utilization while reducing costs for various AI/ML workloads. It provides dynamic compute allocation, task prioritization, real-time monitoring, and cost optimization, addressing key challenges faced by organizations in the generative AI space.