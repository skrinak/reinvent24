# Summary of AWS re_Invent 2024 - How ICEYE uses satellite data & generative AI to speed flood response (AES305).txt

# AWS re:Invent 2024 - How ICEYE uses satellite data & generative AI to speed flood response

## Summary

### Introduction

- The session explores the intersection of advanced satellite technology, AWS cloud capabilities, and generative AI to close the data gap on natural disasters from space, enabling objective data-driven decision-making that can save lives and protect communities.
- ICEYE is revolutionizing natural disaster monitoring and response using their synthetic aperture radar (SAR) satellite constellation and AWS cloud services.

### ICEYE and SAR Technology

- ICEYE owns and operates the largest constellation of SAR satellites, miniaturizing the technology to build small, cost-effective satellites.
- SAR can see through clouds, smoke, and volcanic ash, providing precise ground-level insights.
- ICEYE's solutions focus on defense, intelligence, and civil security use cases, as well as selling imagery and providing analytical expertise.

### ICEYE's Natural Catastrophe Solutions

- ICEYE has developed solutions for monitoring and responding to natural disasters, such as floods, wildfires, volcanic eruptions, and wind damage.
- The Flood Insights solution combines satellite data, social media, weather data, and ground sensors to provide real-time flood depth and extent information to customers.
- ICEYE aims to create a global source of truth for hazard impact information to better understand and mitigate disasters.

### ICEYE's Architecture on AWS

- ICEYE leverages AWS services like AWS Ground Station, Amazon EKS, Amazon EC2, Amazon S3, Amazon RDS, and Amazon Aurora to implement their end-to-end workflow.
- AWS Ground Station enables direct downlinking of satellite data to ICEYE's AWS environment, reducing latency.
- Amazon SageMaker is used for building, training, and deploying models for tasks like flood segmentation.

### Generative AI for Flood Response Automation

- ICEYE collaborated with the AWS Space Team to build an AI-based solution to automate manual work and accelerate flood response.
- The solution includes an ETL pipeline for ingesting social media data, using generative AI models from Amazon Bedrock for flood depth estimation and geolocation, and secure product access for ICEYE's infrastructure.
- Generative AI models are integrated into ICEYE's workflow using AWS services like Amazon EventBridge, AWS Glue, Amazon API Gateway, AWS Lambda, and Amazon Athena.

### Conclusion

- AWS enables ICEYE to implement an integrated architecture, leverage cloud-native services, and incorporate emerging technologies like generative AI.
- The cloud-centric approach and collaboration with AWS have empowered ICEYE to innovate and deliver impactful solutions for natural disaster monitoring and response.