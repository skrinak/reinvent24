# Summary of AWS re_Invent 2024 - Fidelity Investments_ Building for mission-critical resilience (FSI318).txt

# Summary

## Main Points

1. **Enterprise Resilience Challenge**: Running mission-critical applications 24/7 is challenging as things can break unexpectedly, both from external events and internal changes. The goal is to build resilient systems that can withstand failures and continue operating.

2. **Chaos Engineering Approach**: Chaos engineering is a disciplined approach to proactively identifying and addressing potential failure modes in systems. It involves:
   - Failure Mode and Effects Analysis (FMEA) to identify potential failure modes and their impacts
   - Creating hypotheses about system behavior under failure scenarios
   - Conducting controlled experiments to validate hypotheses and learn about system dependencies and failure modes

3. **Fidelity Investments' Implementation**: Fidelity Investments adopted chaos engineering at scale to build resilience into their mission-critical trading and financial systems:
   - Developed a platform called "Chaos Buffet" to execute chaos experiments across applications
   - Partnered with AWS to develop the AWS Fault Injection Service (FIS) for injecting faults into services like Lambda
   - Achieved significant improvements in resilience, with increased chaos engineering coverage and reduced mean time to resolution (MTTR)

4. **Key Learnings and Outcomes**: Through chaos engineering, Fidelity gained insights into:
   - Surviving failures: Improving retry logic, timeouts, and other configurations
   - System performance: Optimizing memory allocations and scaling policies
   - Matching demand: Adjusting scaling configurations to handle peak loads
   - Reducing impact area: Identifying and isolating failure domains

5. **Future Goals**: Continuing to expand chaos engineering coverage, depth of failure mode testing, and maturity across teams. Democratizing the practice and making it foundational for mission-critical applications in regulated industries like financial services.

## Important Conclusions

- Chaos engineering is a valuable approach for building resilient systems, especially for mission-critical applications with high availability requirements.
- Proactively identifying and addressing potential failure modes through controlled experiments can significantly improve system resilience and reduce downtime.
- Adopting chaos engineering at scale requires a structured approach, with platforms and tooling to execute experiments safely and efficiently across applications.
- Collaboration between organizations and cloud providers can accelerate the development of chaos engineering capabilities and best practices.
- Regulated industries like financial services should embrace chaos engineering as a foundational practice for ensuring the resilience of critical systems that underpin the global economy.