# Summary of AWS re_Invent 2024 - Harnessing AWS for natural disaster early warning at scale (IMP212).txt

# Summary

## Main Points

1. **Earthquake Early Warning Systems**: EarthScope Consortium is responsible for measuring and reporting the movement of the Earth's crust, helping power earthquake early warning systems like USGS ShakeAlert.

2. **GNSS Data Integration**: EarthScope has integrated Global Navigation Satellite Systems (GNSS) data into the ShakeAlert system, enabling accurate real-time estimation of large earthquake magnitudes, which seismic data alone struggles with.

3. **Real-Time Data Ingestion and Processing Pipeline**: EarthScope has built a scalable and resilient real-time data ingestion and processing pipeline on AWS using services like Managed Streaming for Kafka (MSK), Elastic Container Service (ECS), and Fargate.

4. **Observability and Monitoring**: EarthScope leverages AWS observability services like Amazon Managed Service for Prometheus, AWS X-Ray, Amazon Managed Grafana, and Amazon Timestream for comprehensive monitoring of system health and data characteristics.

5. **Long-Term Data Archival**: EarthScope archives the scientific data in Amazon S3, leveraging intelligent tiering and the durability of S3 to preserve the priceless dataset for long-term access by the scientific community.

6. **Organizational Transformation**: EarthScope has undergone a three-year journey of organizational transformation, adopting AWS best practices, leveraging the Well-Architected Framework, and collaborating with AWS teams and partners to build this scalable and resilient system.

## Key Insights

- Integration of GNSS data with seismic data enables accurate real-time estimation of large earthquake magnitudes, which is crucial for effective early warning systems.
- AWS services like MSK, ECS, and Fargate provide a scalable and resilient foundation for real-time data ingestion and processing pipelines.
- Comprehensive observability and monitoring using AWS services like Managed Prometheus, X-Ray, Managed Grafana, and Timestream are essential for ensuring system health and data validity.
- Amazon S3's durability and intelligent tiering make it an ideal choice for long-term archival of priceless scientific datasets.
- Organizational transformation and adoption of AWS best practices, including the Well-Architected Framework, are critical for successful cloud migration and building resilient and scalable systems.

## Important Conclusions

- EarthScope's integration of GNSS data with the ShakeAlert system has significantly improved the accuracy of real-time earthquake magnitude estimation, potentially saving lives and reducing damage during large seismic events.
- The scalable and resilient real-time data processing pipeline built on AWS using services like MSK, ECS, and Fargate enables EarthScope to handle large volumes of data and ensure system reliability.
- Comprehensive observability and monitoring using AWS services provide EarthScope with visibility into system health and data characteristics, ensuring the accuracy and timeliness of delivered data.
- The long-term archival of scientific data in Amazon S3 preserves an irreplaceable and priceless dataset with high durability, enabling future research and analysis by the scientific community.
- EarthScope's organizational transformation and adoption of AWS best practices, including the Well-Architected Framework, have been critical to the successful implementation of this scalable and resilient system, enabling them to focus on their core mission of advancing scientific understanding.