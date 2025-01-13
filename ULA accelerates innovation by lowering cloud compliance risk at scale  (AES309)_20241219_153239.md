# Summary of AWS re_Invent 2024 - ULA accelerates innovation by lowering cloud compliance risk at scale  (AES309).txt

# Summary

## Title: AWS re:Invent 2024 - ULA accelerates innovation by lowering cloud compliance risk at scale (AES309)

### Introduction

- The session is aimed at anyone using highly regulated GovCloud environments or facing challenges in such environments.
- The concepts and framework discussed are also applicable to commercial cloud environments.

### About United Launch Alliance (ULA)

- ULA is a joint venture between Lockheed Martin and Boeing, formed in 2006.
- They build and launch rockets for commercial and government missions, including space exploration, satellite launches, and supporting the military.
- ULA has launched 163 missions with a 100% success rate.

### Early Cloud Adoption Challenges at ULA

- User provisioning was complex, taking hours or days, hindering productivity.
- Scaling identity management was a problem.
- Defining and implementing least privilege access was difficult due to diverse user roles.
- Workloads were difficult due to a lift-and-shift mentality.
- Lack of cloud knowledge among the user base.

### Approach to Solving the Problem

- Deep dive into policies and user requirements.
- Educating users on cloud-centric concepts.
- Identifying inefficiencies in the request process.
- Cleaning up overly broad permissions.
- Attempting role-based access controls (RBAC) but facing challenges.
- Partnering with AWS Professional Services for a fresh perspective.

### Effective Permissions and Functional Privilege Model

- Effective Permissions: Combining service control policies, identity policies, and boundary policies.
- Functional Privilege Model:
  - Implementing an "onboarding account" for developers to explore with wider permissions.
  - Using AWS tools like IAM Access Analyzer and CloudTrail to capture actual usage.
  - Generating least-privileged policies based on usage data.
  - Deploying these policies to permanent accounts using permission boundary policies.
  - Iterating and adjusting policies as usage evolves.

### Key Enablers

- Cloud Center of Excellence (CCoE) for governance and user enablement.
- Architecture Community of Practice for standards and policies.
- Service approval process for thorough security review and control implementation.
- Custom CLI tools and integration with infrastructure-as-code repositories.

### Conclusion

- The functional privilege model accelerated innovation by providing secure, controlled access tailored to actual usage.
- It reduced provisioning times from days to minutes while maintaining compliance.
- The principle of "leash privilege" empowers users while preventing security risks.