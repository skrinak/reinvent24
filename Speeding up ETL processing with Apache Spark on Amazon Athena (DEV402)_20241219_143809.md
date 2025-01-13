# Summary of AWS re_Invent 2024 - Speeding up ETL processing with Apache Spark on Amazon Athena (DEV402).txt

# Summary

## Main Points

1. **Causes of Slow ETL Pipelines**
   - Processing more data than necessary (e.g., full loads instead of incremental loads)
   - Poorly structured data (e.g., lack of partitioning, inefficient file formats)
   - Lack of parallelization (single machine or process handling all data)

2. **Optimization Case 1: Rethinking the Data Pipeline**
   - Identified an unnecessary step that aggregated data for all time
   - Created an aggregate table at a daily level, incrementally loaded
   - Reduced a 6-hour process to 8 minutes by processing less data

3. **Apache Spark and Amazon Athena**
   - Athena: Serverless, managed Presto-based query engine for Data Lake
   - Apache Spark: Fast, in-memory processing with familiar APIs (SQL, DataFrames)
   - Spark on Athena: Serverless, managed Spark environment on Athena

4. **Optimization Case 2: Spark on Athena for Parallelization**
   - Replaced a 3-hour Python/Pandas process with Spark on Athena
   - Reduced runtime to 2 minutes by leveraging parallelization
   - Demonstrated using custom libraries and productionizing Spark on Athena jobs

5. **Key Takeaways**
   - Long-running jobs tend to get longer and lead to instability
   - Question assumptions and rethink processes when possible
   - Leverage parallelization for scalability and performance
   - Spark on Athena simplifies Spark usage and reduces complexity

## Important Conclusions

- Addressing the root causes of slow ETL pipelines (processing too much data, poorly structured data, lack of parallelization) can lead to significant performance improvements.
- Rethinking and simplifying data pipeline processes can sometimes yield remarkable performance gains with minimal effort.
- Spark on Athena provides a serverless, managed Spark environment that simplifies parallelization and reduces operational overhead.
- Continuously optimizing and questioning assumptions about data pipelines is crucial to maintaining performance and avoiding instability as data volumes grow.

The presentation highlighted the importance of identifying and addressing the root causes of slow ETL pipelines, leveraging parallelization frameworks like Spark on Athena, and continuously rethinking and optimizing data pipeline processes to maintain performance and scalability.