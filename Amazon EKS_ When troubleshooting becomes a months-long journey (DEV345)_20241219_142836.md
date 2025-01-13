# Summary of AWS re_Invent 2024 - Amazon EKS_ When troubleshooting becomes a months-long journey (DEV345).txt

# AWS re:Invent 2024 - Amazon EKS: When Troubleshooting Becomes a Months-Long Journey

## Summary

The speaker, Carolina Herrera, a DevOps tech lead at Globant, shared her experience of troubleshooting a production issue with an Amazon EKS cluster that took months to resolve. The main points and key insights from her presentation are as follows:

### The Issue

- The production environment was down, and a critical service was affected.
- The initial symptom was a "Gateway Time-out" error, which is a general error message.
- The cluster, nodes, and pods appeared healthy, but the issue persisted.

### Troubleshooting Journey

- Distinguishing between symptoms and the real problem was crucial.
- The investigation focused on the area between the Application Load Balancer (ALB) and the EKS cluster.
- Restarting pods and killing nodes provided temporary relief, but the issue kept recurring.
- Iterative steps were taken, including:
  - Upgrading the cluster, add-ons, and components to the latest versions.
  - Analyzing logs and error messages.
  - Automating the detection and temporary fix process.

### Root Cause

- After months of investigation, a single log entry mentioning "Disk permission" led to the root cause: an IP exhaustion issue caused by an incompatible third-party agent installed on the cluster.
- Removing the incompatible agent resolved the issue permanently.

### Lessons Learned

1. **Consider all components**: When troubleshooting EKS issues, consider all components, including external tools and agents installed on the cluster.
2. **Validate compatibility**: Ensure that external applications and tools are compatible with the EKS environment before installing them.
3. **Monitor configurations**: Regularly validate and update configurations, such as the autoscaler settings, especially after upgrades or changes.
4. **Be patient**: Troubleshooting complex issues can be a long journey, requiring patience, iteration, and learning.

The presentation highlighted the importance of thorough investigation, considering all components, validating compatibility, and maintaining patience when troubleshooting complex issues in an Amazon EKS environment.