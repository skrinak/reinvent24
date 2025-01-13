# Summary of AWS re_Invent 2024 - Try again_ The tools and techniques behind resilient systems (ARC403).txt

# AWS re:Invent 2024 - Try again: The tools and techniques behind resilient systems (ARC403)

## Summary

### Retries

- Jitter (adding randomness) is good for systems as it helps break up spikes.
- Retries can introduce metastable or tipping point failures, where they knock systems over in a way that they don't recover, even with best practices like exponential backoff.
- Using a token bucket algorithm, like the one used in the AWS SDK, can avoid this failure mode for most types of systems with just a few lines of client-side code.
- Backoff is not particularly effective in open systems (with a large number of random clients), but it is effective in closed systems.

### Circuit Breakers

- Circuit breakers are powerful tools for reducing optional functionality (reducing harvest) and ensuring clients are generous to downstream systems during overload.
- However, caution is needed with circuit breakers in sharded systems and deep service architectures, as they can reduce availability.
- Pushing circuit breakers deeper into the architecture or exposing more architectural details to the client can be effective but comes with trade-offs.

### Tail Latency

- Techniques like hedging (calling twice), erasure coding, and constant work strategies can flatten the tail and reduce outlier latency.
- Erasure coding is particularly effective and underutilized in distributed caches and immutable data systems.
- Token buckets can limit additional work for techniques that require more work during failures.

### Simulations

- Simulations are powerful mathematical tools that fit the mental model of most programmers well.
- Simple simulations can be reviewed, tested, and understood like code, but provide powerful insights into system behavior.
- Simulations can help discover potential issues and avoid long and painful outages.
- Generative AI can accelerate the creation of simulations, allowing for faster exploration of system behavior.

### Key Takeaways

- Write more simulations to understand the behavior of your systems, clients, and servers.
- Simulations can save time and effort by identifying potential issues before implementing complex solutions.
- Understand the trade-offs and potential pitfalls of techniques like retries, circuit breakers, and tail latency mitigation strategies.
- Leverage tools like token buckets, erasure coding, and constant work strategies to build more resilient systems.