# Summary of AWS re_Invent 2024 - IaC and AI_ Tales from the trenches (DEV342).txt

# AWS re:Invent 2024 - IaC and AI: Tales from the Trenches (DEV342)

## Summary

The presentation covers the use of generative AI (Gen AI) in Infrastructure as Code (IaC) and the associated risks and learnings from real-world scenarios. The speaker, Bojan Zivic, an AWS Ambassador and Principal Consultant, shares insights from three different personas: SRE/DevOps/DevSecOps, Security Engineer, and Developer.

### Key Points

#### SRE/DevOps/DevSecOps Persona

- A FinTech organization using Python and TypeScript for CDK, without unit tests, experienced a security breach where a fake library stole API keys during the CDK build process.
- Learnings: Implement guardrails, best practices, and security measures. Gen AI can speed up development but requires contextual awareness and critical thinking.

#### Security Engineer Persona

- A data startup using Terraform and Django models extensively faced cost overruns due to Gen AI recommending a public module with expensive storage options.
- Gen AI also introduced security vulnerabilities like SQL injections.
- Learnings: Implement security across all layers, from IDE to pre-commit and pipelines. Use tools like Amazon Q IaC scanning to identify potential issues.

#### Developer Persona

- A financial institution using Java 8 and moving to containers faced issues like out-of-memory incidents with heavy Java containers and delayed Java 8 to 17 migration due to slow Gen AI adoption.
- Gen AI suggested infrastructure patterns without proper inspection, leading to potential security risks.
- Learnings: Collaborate between developers and infrastructure teams. Leverage Gen AI's strengths for specific tasks like Java version migrations. Prioritize security and quality code over containerization alone.

### Important Conclusions

1. **Embrace Gen AI, but reflect**: Gen AI can significantly speed up development, but contextual awareness and critical thinking are crucial.

2. **Context is King**: Understanding the context and implications of Gen AI suggestions is essential to avoid security risks and costly mistakes.

3. **Security, Security, Security**: Gen AI usage necessitates heightened security measures across all layers, from IDE to deployment.

4. **Collaborate, Never Silo**: Cross-team collaboration between developers, DevOps, and security engineers is vital for leveraging Gen AI effectively and mitigating risks.

5. **Quality over Containerization**: Containerization alone does not guarantee improvements; quality code and proper infrastructure choices are paramount.

The presentation emphasizes the potential benefits of Gen AI in IaC while highlighting the importance of responsible adoption, security-focused practices, and cross-functional collaboration to mitigate risks and maximize the advantages of this emerging technology.