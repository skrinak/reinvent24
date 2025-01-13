# Summary of AWS re_Invent 2024 - Scale clinical diagnostic operations_ Natera_s genomic innovation (HLS206).txt

# AWS re:Invent 2024 - Scale clinical diagnostic operations: Natera's genomic innovation (HLS206)

## Summary

### Introduction

- Margo McDowall, Principal Product Manager for AWS HealthOmics, introduced the session.
- A patient story was shared about how Natera's Signatera test helped detect and monitor bladder cancer early.

### AWS HealthOmics

- AWS HealthOmics is a service designed to accelerate scientific breakthroughs with fully managed biological data stores and workflows.
- It is used for production-scale clinical diagnostics tests, experimenting with generative AI and biological foundation models for drug discovery, and multimodal analysis combining genomics with other data modalities.
- The service has modular components like Sequence Store, Reference Store, Bioinformatics Workflows, Variant Store, and Annotation Store.
- HealthOmics offers features like automated genomic compression, data provenance tracking, and sharing/collaboration capabilities.
- Customers are operating at scale, running thousands of samples daily, with petabyte-scale data storage.

### Natera's Journey

- Mirko Buholzer, VP of Software Engineering at Natera, discussed their journey in scaling clinical diagnostics operations using AWS services.
- Natera has pioneered cfDNA technology for detecting fetal, tumor, and donor DNA from a single blood draw.
- Their focus is on fast innovation cycles to bring more tests and help more patients.
- Signatera, a pan-cancer test, can detect residual disease and monitor for recurrence up to 9 months earlier than standard imaging.
- Natera also offers tests in women's health and organ health.

### Natera's Lab X

- Lab X is Natera's digitally connected lab infrastructure for scalability and reusability.
- It processes over 54,000 tests per week, generating 1.6 petabytes of data weekly.
- The lab uses assays, which consist of wet lab workflows, bioinformatics workflows, and QC steps, reused across different products.
- Natera uses AWS HealthOmics to run bioinformatics pipelines in WDL, leveraging scalability and containerization.
- They also use HealthOmics Variant Store for VCF annotations and cohort building.
- An analytics data mesh stores pipeline outputs, instrument data, lab metrics, and clinical data extracted from unstructured sources using LLMs.
- This data is combined to generate patient cancer journeys, enabling informed patient care.

### New AWS HealthOmics and HealthImaging Features

- HealthOmics Workflows now support call caching, resuming runs from the last successful task, accelerating workflow development.
- AWS HealthImaging now supports lossy medical imaging data, including DICOM whole slide images for digital pathology.
- HealthImaging enables combining pathology images with Omics data and clinical data for a comprehensive patient health view.

## Key Insights and Conclusions

- AWS HealthOmics enables scaling clinical diagnostics pipelines and drug discovery with fully managed data stores and workflows, offering predictable costs and fast turnaround times.
- Natera's Lab X infrastructure, powered by AWS services like HealthOmics, enables rapid innovation, reusable assays, and scalability to bring more tests to market quickly.
- Combining genomic data with clinical data and leveraging generative AI models like LLMs can provide deeper insights and transform patient care.
- New AWS features like HealthOmics call caching and HealthImaging support for digital pathology images further enhance capabilities for healthcare and life sciences customers.