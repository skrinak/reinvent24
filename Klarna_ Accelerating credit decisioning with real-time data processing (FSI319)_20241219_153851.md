# Summary of AWS re_Invent 2024 - Klarna_ Accelerating credit decisioning with real-time data processing (FSI319).txt

# AWS re:Invent 2024 - Klarna: Accelerating Credit Decisioning with Real-Time Data Processing

## Overview

This session covers Klarna's journey in improving their data processing system for creating customer features used in credit underwriting. The main points and key insights are:

## Main Points

1. **Klarna and Credit Underwriting**
   - Klarna is a FinTech company providing payment solutions and enhancing customer shopping experience.
   - Credit underwriting involves accepting or rejecting purchases based on customer risk assessment.
   - Customer features and data points are crucial for accurate risk assessment and credit underwriting.

2. **Previous System Challenges**
   - Reliance on internal database dumps as data sources, lacking strict contracts between producers and consumers.
   - Inefficient batch processing of full data history, leading to scalability and cost issues.
   - Significant differences between real-time and batch processing layers, hindering feature engineering innovation.
   - Long iteration cycles due to the need to wait for data to mature before assessing new features.

3. **New System Architecture**
   - Strict contracts between producers and consumers through well-defined event streams and schemas.
   - Real-time processing of only incremental changes, reducing redundant computations.
   - Business logic libraries decouple business logic from runtime, enabling consistent feature calculations across real-time and batch layers.
   - Offline processing and retrospective calculation enable experimentation with new features on historical data.

4. **Key Benefits**
   - Improved cost efficiency and scalability by processing only real-time changes.
   - Reduced differences between real-time and batch processing layers through shared business logic.
   - Faster feature engineering iterations by enabling experimentation on historical data.

5. **Challenges and Learnings**
   - Data modeling challenges: balancing read performance and flexibility.
   - Inefficiencies in running Python UDFs on Spark for offline processing.
   - Feature quality heavily dependent on the quality and understanding of source data.

## Important Conclusions

- Klarna's new system architecture addresses the challenges faced in their previous setup, enabling more efficient, scalable, and innovative credit decisioning through real-time data processing.
- Strict contracts between data producers and consumers, decoupling of business logic, and offline processing capabilities are key enablers for accelerating feature engineering and improving credit risk assessment.
- Continuous improvement and learning, particularly in data modeling, offline processing optimization, and source data quality, are essential for maintaining and enhancing the system's performance.