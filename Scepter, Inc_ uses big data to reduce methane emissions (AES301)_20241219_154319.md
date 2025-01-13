# Summary of AWS re_Invent 2024 - Scepter, Inc_ uses big data to reduce methane emissions (AES301).txt

# AWS re:Invent 2024 - Scepter, Inc. uses big data to reduce methane emissions (AES301)

## Summary

### Introduction (Philip Father, Scepter)

- Scepter, in collaboration with AWS and ExxonMobil, has developed a platform to monitor the atmosphere and make the invisible visible.
- The platform detects and quantifies various gases and particulates in the atmosphere, such as nitrogen dioxide (NO2), particulate matter (PM2.5), ground-level ozone, methane, and carbon dioxide.
- These gases and particulates have significant impacts on human health, agriculture, and climate change.
- The platform can detect and quantify methane plumes, geolocate them, and provide a five-step process to inform, abate, and certify the leak mitigation.

### Scepter's Atmospheric Monitoring Platform (Philip Father, Scepter)

- The platform ingests data from thousands of sensors, including terrestrial sensors, aerial sensors, drones, stratospheric platforms, and satellites.
- It normalizes and fuses the data from these disparate sensors into a big data cube.
- Scepter has innovated in flying hyperspectral sensors at the stratosphere (60,000 feet) to detect methane plumes down to 10 kg/hour.
- The platform addresses gaps in coverage, timing, and detection thresholds of existing sensors by combining data from multiple sources.
- Scepter has also developed a stratospheric platform with edge computing capabilities to reduce latency and deliver alerts within minutes.
- The company is expanding its platform to include aerial monitoring of offshore oil platforms and a future satellite constellation.
- The platform aims to provide real-time, global atmospheric data acquisition, enabling new use cases like personalized health and beauty recommendations based on air quality.

### AWS Collaboration and Architecture (Chantz Thomas, AWS)

- AWS Professional Services has been collaborating with Scepter to accelerate and enhance their mission.
- The architecture follows a multi-account setup with separate accounts for management, logging, and applications, ensuring security and separation of duties.
- The platform ingests data from satellites, High-Altitude Pseudo-Satellites (HAPS), and IoT sensors, leveraging AWS services like the Registry of Open Data and IoT Core.
- HAPS missions use edge computing and Starlink connectivity to reduce latency and enable near real-time data processing and alerting.
- The platform uses the Spatio-Temporal Asset Catalog (STAC) specification to organize and catalog geospatial data, running on Amazon Aurora and served via API Gateway.
- Data processing leverages AWS services like Lambda, SageMaker, and open-source libraries for parallelization, machine learning, and interoperability.
- The platform serves data through SNS alerts, APIs for programmatic access, and a user interface built with open-source components like React and MapLibre, hosted on AWS.
- Future plans include exploring LLMs for improved user experience, using SageMaker for custom computer vision models, and optimizing for the future satellite constellation.

### ExxonMobil's Perspective (Emily Reidy, ExxonMobil)

- ExxonMobil has significantly reduced its Scope 1 and Scope 2 emissions since the Paris Agreement and has a 2030 net-zero ambition for operated assets in the Permian Basin.
- Methane emissions pose significant challenges, with a wide range of emission rates from 10 kg/hour to thousands of kg/hour, requiring a combination of sensors and monitoring techniques.
- ExxonMobil uses a data fusion platform called COMET to integrate data from satellites, continuous monitors, aerial surveys, and drones, paired with internal process data.
- The platform needs to be flexible, automated, fast, secure, scalable, and produce clear, actionable alerts to efficiently reduce methane emissions.
- Scepter's data fusion platform meets ExxonMobil's requirements and will help achieve their net-zero goals by efficiently detecting, quantifying, and mitigating methane emissions.

## Key Insights and Conclusions

- Scepter has developed an innovative atmospheric monitoring platform that combines data from various sensors to detect and quantify gases and particulates, with a focus on methane emissions.
- The platform addresses key challenges like coverage gaps, timing differences, and detection thresholds by fusing data from multiple sources and leveraging advanced technologies like hyperspectral sensors and edge computing.
- Collaboration with AWS has enabled Scepter to build a secure, scalable, and low-latency architecture, leveraging various AWS services and open-source components.
- The platform has the potential to enable new use cases beyond methane monitoring, such as personalized health and beauty recommendations based on air quality data.
- ExxonMobil, as a key customer and collaborator, has provided insights into the challenges of methane emissions monitoring and the requirements for an effective data fusion platform.
- The combined efforts of Scepter, AWS, and ExxonMobil aim to significantly reduce methane emissions and contribute to achieving net-zero goals in the energy industry.