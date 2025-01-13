# Summary of AWS re_Invent 2024 - How Ford unlocked real-time insights using Apache Iceberg on AWS (AUT311).txt

# Summary

## AWS re:Invent 2024 - How Ford Unlocked Real-Time Insights Using Apache Iceberg on AWS

### Overview

- Connected vehicles are a key enabler for remote operations like remote start, vehicle warm-up, etc.
- In the era of connected vehicles, it's crucial to use real-time data insights to enhance customer experience and improve operational efficiency.
- The session explores Ford's Event Store, a key service for their connected vehicle platform, built using Apache Iceberg on AWS.

### Connected Vehicles and Data Challenges

- AWS infrastructure enables building innovative mobility features and applications for connected vehicles.
- Connected vehicle data lake allows organizations to drive meaningful insights, leading to improved customer experience, operational efficiency, and decision-making.
- Data challenges include volume, complexity, real-time consumption, scalability, and high volume/concurrency.

### Apache Iceberg on AWS

- Apache Iceberg is an open table format that provides a cost-effective, scalable solution for transactional data lakes.
- Iceberg is witnessing widespread adoption, with an 81% increase in end-users over one year.
- AWS positions Apache Iceberg as a strategic open table format due to its performance, scalability, and ease of use.

#### Benefits for Connected Vehicle Platforms

- **ACID Compliance**: Ensures data consistency and reliability, crucial for vehicle safety systems.
- **Schema Enforcement and Evolution**: Handles schema changes without disrupting existing data.
- **Scalability and Performance**: Supports petabyte-scale data and handles data spikes without impacting downstream users.
- **Engine Agnostic**: Supports querying Iceberg tables from various compute engines like Spark, Trino, and Presto.

### Ford's Connected Vehicle Platform and Event Store

- Ford's connected vehicle platform enables bidirectional communication between vehicles and the cloud, managing over 20 million vehicles globally.
- Event Store is an analytical solution built using Iceberg and AWS serverless technologies (Glue and Athena).
- Event Store collects and analyzes events from various workflows (telemetry, remote functions, connectivity) and provides a unified view.

### Ford's Journey with Event Store

1. **Initial Scope**: Focused on high-cardinality data with moderate data freshness requirements, using a cost-efficient serverless solution.
2. **Scalability Challenges**: As more workflows were onboarded, the platform faced scalability issues, delayed data processing, degraded query experience, increased costs, and data aging problems.
3. **Optimization Journey**:
   - **Clean Zone Improvements**: Optimized existing jobs and adopted Iceberg to address scalability issues.
   - **Stream Processing Adoption**: Ongoing work to support both streaming and batching for real-time use cases using EMR Serverless.

#### Benefits of Adopting Iceberg

- Improved query performance by up to 80% compared to the Hive format.
- Reduced S3 costs by compacting small files.
- Simplified schema evolution without reprocessing historical data.
- Enabled real-time data availability for critical use cases through streaming processing.

### Conclusion

- Apache Iceberg, combined with AWS analytics services, provides a transformative power for modernizing transactional data lakes.
- AWS ecosystem services like EMR, Glue, Athena, SageMaker, and Redshift seamlessly support Apache Iceberg.
- AWS Glue Catalog provides a unified metadata repository for Iceberg tables.
- Amazon S3 offers a cost-effective, scalable storage solution for transactional data lakes.