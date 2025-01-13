# Summary of AWS re_Invent 2024 - Learnings from BMW_s global software development platform on AWS (AUT319).txt

# Summary of AWS re:Invent 2024 - Learnings from BMW's global software development platform on AWS

## Introduction

- The presentation covers BMW's migration of their software development platform, CodeCraft, to AWS.
- Christian, a principal solutions architect at AWS, and Céline Laurent-Winter from BMW, discuss the challenges, learnings, and business results of this migration.

## Background

- Modern vehicles contain hundreds of electronic control units and millions of lines of code.
- BMW's CodeCraft platform supports over 12,000 developers, 165,000 daily builds, and 5,500 concurrent builds.
- Key goals for the platform include reliability, developer productivity, and cost efficiency.
- Scaling on-premises was challenging, leading BMW to migrate CodeCraft to AWS.

## Migration to AWS

- A hybrid solution was designed, with some resources remaining on-premises and others migrated to AWS.
- Core services like GitHub and Artifactory, as well as CI tools like BuildBarn and Sewell CI, were moved to AWS.

## Cost Optimization Strategies

### Instance Right-Sizing

- BMW used the open-source sysstat utility to collect metrics on CPU, memory, network, and I/O usage for each CI job.
- This data helped identify if jobs were running on appropriately sized EC2 instances.
- Different CPU architectures (AMD, Intel, Graviton) were benchmarked for performance differences.

### Containerization and Karpenter

- Core and sonal services were containerized and run on Amazon EC2.
- Adopting Karpenter, a Kubernetes cluster autoscaler, reduced infrastructure costs by up to 66%.
- Karpenter optimizes EC2 instance utilization (up to 94%) and provisions right-sized instances.

### Spot Instances

- Using EC2 Spot instances, which leverage unused EC2 capacity at a discount of up to 90%, provided significant cost savings.
- Initially, AWS provided hints on instance types to use to minimize Spot reclaims.
- Later, EC2 Fleet was adopted, allowing CodeCraft to specify a list of capable instance types.
- The EC2 Instance Selector tool helped identify additional suitable instance types.
- By tripling the number of Spot pools used (to 300) and changing the allocation strategy, Spot reclaims were reduced.

## Business Results

- Customer (developer) satisfaction increased, with no disruptions during the migration.
- Developer productivity improved due to faster feedback on code changes.
- CodeCraft won an award for "Business Impact" from the Automotive IT Congress.
- Overall platform costs and cost per CI job were reduced, contributing to a more sustainable future.