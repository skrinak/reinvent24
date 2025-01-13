# Summary of AWS re_Invent 2024 - Efficient incremental processing with Apache Iceberg at Netflix (NFX303).txt

# Summary

## Title: Efficient Incremental Processing with Apache Iceberg at Netflix

### Main Points:

1. **Introduction**:
   - Netflix is a data-driven company, and many business decisions are driven by data insights from various data pipelines.
   - Common problems faced by data practitioners include data accuracy, freshness, and cost efficiency.
   - Late-arriving data is a major challenge, as the event time matters more than the processing time.

2. **Apache Iceberg and Netflix Maestro**:
   - Apache Iceberg is a high-performance format for huge analytics tables, providing rich metadata features.
   - Netflix Maestro is a horizontally scalable workflow orchestrator developed by Netflix to manage data pipelines.

3. **Architectural Design**:
   - The solution aims to efficiently capture changes without reading user data and provide a seamless user experience with minimal code changes.
   - Iceberg's metadata is used to create a zero-data-copy incremental change capturing table, containing only the changed data references.
   - Maestro provides interfaces (IpCapture and IpCommit steps) to enable incremental processing with minimal user code changes.

4. **Use Cases and Examples**:
   - Three emerging patterns enabled by the solution:
     - Incrementally process change data and append to the target table.
     - Use change data as a filter to remove unnecessary transformations.
     - Use captured range parameters in the business logic.
   - Real-world examples demonstrate how the solution is implemented, enabling significant cost savings and improved data freshness.

5. **Key Takeaways**:
   - The solution enables new patterns and allows rethinking batch ETL pipelines, achieving data accuracy, freshness, and cost efficiency.
   - Decoupling change capturing from business logic provides a seamless user experience with minimal code changes.
   - The zero-data-copy approach ensures efficiency and compliance with security and privacy requirements.

6. **Future Work**:
   - Adding a view to the Iceberg SQL extension for change data capture.
   - Supporting other types of snapshots (overwrites, deletes) in the solution.
   - Enabling multi-stage auto-cascading data backfill support using incremental processing.

### Important Conclusions:

The solution developed by Netflix, combining Apache Iceberg and Netflix Maestro, enables efficient incremental processing of late-arriving data. It addresses the challenges of data accuracy, freshness, and cost efficiency while providing a seamless user experience with minimal code changes. The zero-data-copy approach ensures efficiency and compliance with security and privacy requirements. The solution unlocks new patterns and allows rethinking batch ETL pipelines, enabling significant cost savings and improved data freshness.