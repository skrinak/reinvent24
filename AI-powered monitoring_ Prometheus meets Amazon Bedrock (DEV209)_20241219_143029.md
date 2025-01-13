# Summary of AWS re_Invent 2024 - AI-powered monitoring_ Prometheus meets Amazon Bedrock (DEV209).txt

# AWS re:Invent 2024 - AI-powered monitoring: Prometheus meets Amazon Bedrock (DEV209)

## Summary

The speaker introduced Epimetheus (or Kepimetheus for Kubernetes), an open-source project that leverages natural language processing (NLP) and large language models (LLMs) like Amazon Bedrock to assist in creating PromQL queries for Grafana and Prometheus. The main points and key insights are:

### Introduction

- Epimetheus aims to simplify the process of writing PromQL queries by allowing users to express their queries in natural language.
- It was created to address the challenge of remembering PromQL syntax, especially during critical situations like production issues.

### Key Features

- Integrates with Amazon Bedrock and other LLMs for natural language processing.
- Provides a Grafana plugin and Helm chart for easy installation in Kubernetes environments.
- Supports AWS environments and complies with security and compliance standards like PCI and HIPAA.

### Benefits

- No need to remember PromQL syntax, as queries can be expressed in natural language.
- Works seamlessly with AWS environments and Kubernetes clusters.
- Enhances observability and troubleshooting capabilities by simplifying query creation.
- Open-source and community-driven, encouraging contributions.

### Future Roadmap

- Support for local LLM options and other open-source or commercial LLMs.
- Real-time monitoring and automated remediation capabilities, such as adjusting resource limits based on pod metrics.

### Live Demo

The speaker demonstrated the installation and usage of Kepimetheus in a Minikube environment, showcasing the ability to transform natural language queries into PromQL and execute them in Grafana.

## Conclusion

Epimetheus (or Kepimetheus) aims to simplify the process of creating and managing PromQL queries by leveraging natural language processing and LLMs. It provides an open-source solution for enhancing observability and troubleshooting in AWS and Kubernetes environments, while encouraging community contributions and future enhancements.