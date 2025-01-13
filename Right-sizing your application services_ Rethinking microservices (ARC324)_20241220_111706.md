# Summary of AWS re_Invent 2024 - Right-sizing your application services_ Rethinking microservices (ARC324).txt

# Summary of the Transcript

## Introduction

- The talk is about rethinking the approach to microservices and right-sizing application services based on the context of the organization.
- The speaker, Tod Golding, has been working with organizations at various stages of building and delivering SaaS solutions on AWS.
- He has witnessed the adoption of microservices and the challenges organizations face in implementing them effectively.

## The Microservices Mindset

### The Shiny Object Syndrome

- Early examples of microservices architectures from companies like Netflix showcased complex and impressive implementations.
- This led to organizations adopting microservices as a methodology without considering their specific context and needs.
- The number of microservices became a metric for success, leading to over-decomposition and complexity.

### The Need for Context

- The core principles of microservices (agility, innovation, loose coupling, autonomy) are valid, but the size and granularity of services should be determined by the organization's context.
- Factors like operational complexity, resilience profile, business pressures, release frequency, and team profile should influence the sizing of services.
- The term "microservices" itself carries a bias towards small services, which may not always be appropriate.

## Determining the Right Size

### The Value Map

- Create a value map by plotting candidate services on a quadrant based on two axes:
  1. Business criticality, throughput, and scaling needs
  2. Frequency of deployment and evolution
- Services in the top-right quadrant (high throughput, frequent changes) are good candidates for smaller, more granular microservices.
- Services in the bottom-left quadrant (low throughput, infrequent changes) may benefit from being more coarse-grained.

### Factors to Consider

- Scale efficiency: Decompose services to enable independent scaling of high-consumption components.
- Storage scaling: Separate services with different storage scaling needs to optimize resource allocation.
- Fault tolerance: Size services to isolate failures and prevent cascading outages.
- Performance bottlenecks: Identify and decompose services causing performance issues.

### Drawing the Value Line

- Separate services into two categories:
  1. Coarse-grained services that don't require the full benefits of microservices
  2. Fine-grained services that benefit from the agility and resilience of microservices
- Continuously evaluate and evolve the categorization based on operational data and feedback.

## The Evolutionary Approach

- Start with a coarse-grained architecture and iteratively decompose services based on observed data and feedback.
- For modernization efforts, use the strangler pattern to gradually replace the monolith with microservices.
- The end state may not be a fully decomposed architecture with numerous small services; the right size depends on the organization's context.

## Data-Driven Insights

- Instrument microservices to gather performance profiles and consumption data.
- Involve operations teams in analyzing data to identify sizing issues and bottlenecks.
- Use data to determine if services are too small (lacking value) or too large (causing complexity).

## Takeaways

- Don't chase the "shiny object" of having numerous microservices; focus on achieving value.
- Start with a coarse-grained architecture and let services "earn" their way to finer granularity.
- Consider the complexity introduced by microservices and balance it against the expected value.
- Expect the microservices architecture to evolve continuously based on operational data and feedback.
- Size microservices within the broader context of the organization, teams, and domain.