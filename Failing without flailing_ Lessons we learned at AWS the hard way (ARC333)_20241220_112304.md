# Summary of AWS re_Invent 2024 - Failing without flailing_ Lessons we learned at AWS the hard way (ARC333).txt

# AWS re:Invent 2024 - Failing without flailing: Lessons learned at AWS the hard way

## Summary

### Persistent Connections and Resilience
- Presented by Alec Peterson, VP of Resilience at AWS

#### Key Points:
- Persistent connections can negatively impact resilience at scale
- Regularly reestablishing connections helps exercise recovery workflows
- Resilience is proportional to how often recovery workflows are executed
- Embrace and expect failures at all layers of the system

### Scaling Reliably
- Presented by Becky Weiss, VP and Distinguished Engineer

#### Key Points:
- Stateful hosts can slow down scaling and deployments
- Measure and optimize the time it takes to bring new hosts into service
- Common patterns: snapshots, cellular architectures, synthetic traffic warmup
- Avoid situations where you can't distinguish between a deployment and a problem

### Measuring Bottlenecks
- Presented by Mike Furr, Senior Principal Engineer, EC2 team

#### Key Points:
- Identify and measure scaling bottlenecks before reaching them
- Graph the sum of latency to measure concurrency and headroom
- Little's Law: Concurrency = Arrival Rate × Latency
- Use dimensions (instance ID, node ID, etc.) to quickly identify problematic hosts

### Bonus: Quick Mitigation Techniques
- Post zeros for error metrics to easily detect recovery
- Use dimensions to quickly identify and remove problematic hosts
- "Bounce first, ask questions later" - restart hosts to mitigate issues quickly

## Important Conclusions
- Resilience requires embracing failures and regularly exercising recovery workflows
- Measure and optimize bottlenecks to avoid being caught off-guard during scaling events
- Use techniques like posting zeros, dimensionality, and restarts for quick mitigation
- Focus on reducing the duration of customer impact during operational events