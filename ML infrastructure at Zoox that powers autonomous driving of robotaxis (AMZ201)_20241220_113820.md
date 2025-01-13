# Summary of AWS re_Invent 2024 - ML infrastructure at Zoox that powers autonomous driving of robotaxis (AMZ201).txt

Here is a comprehensive summary of the transcript, formatted in Markdown with appropriate headers and bullet points:

# AWS re:Invent 2024 - ML Infrastructure at Zoox that Powers Autonomous Driving of Robotaxis (AMZ201)

## Introduction

- Zoox is a company building fully autonomous, all-electric robotaxis designed specifically for riders, not drivers.
- Their vision is to reinvent personal transportation by making it safer, cleaner, and more enjoyable for everyone.
- Zoox's robotaxis aim to reduce traffic accidents caused by human error, minimize idle time and congestion from personal vehicles, and reduce pollution from traditional cars.

## Machine Learning Use Cases at Zoox

### Autonomous Driving

- **Perception**: Detecting and classifying dynamic objects like pedestrians, vehicles, traffic signals, and gestures using sensors like cameras, LiDAR, and radar.
- **Prediction**: Predicting the future actions of detected objects over the next few seconds.
- **Planner**: Determining the actions the robotaxi should take based on perception and prediction outputs, such as changing lanes, accelerating, or braking.
- **Collision Avoidance**: A redundant end-to-end system for predicting and avoiding collisions.

### Other Use Cases

- **Generative AI**: Using diffusion-based models for scenario generation in simulations.
- **Foundation Models**: Building models for tasks like identifying interesting scenarios, data mining, and triaging.

## ML Infrastructure at Zoox

### Data Infrastructure

- Challenges: Data management, discoverability, availability, and governance.
- Architecture: Data from robotaxis is stored in S3 data lake, processed into bronze, silver, and gold tables (using Delta tables and Parquet format), and accessed using Apache Spark, Amazon Athena, and Amazon OpenSearch Service.

### Training Infrastructure

- Built on open-source frameworks like PyTorch, PyTorch Lightning, JAX, and Ray.
- Optimized data loading using techniques like data parallelism, Mosaic Data Shards, S3 streaming, FSx, and EFA.
- Model repository and experiment tracking for reproducibility and sharing.

### Serving Infrastructure

- On-vehicle inference optimization using NVIDIA TensorRT.
- Cloud serving infrastructure built on Amazon EKS and Ray Serve for batch inference use cases, supporting auto-scaling, model multiplexing, and different CPU/GPU architectures.

### Compute and Storage Infrastructure

- Compute: EC2, EKS, and managed with SLURM resource scheduler.
- Storage: Amazon S3 and Amazon FSx.
- Workflow orchestration: Apache Airflow.

## Unique Aspects of Building ML Infrastructure for an AV Company

1. **Simulation**: Extensive use of simulation to validate AI stack before deployment, focusing on less common or difficult driving situations.
2. **GPU Demand and Workload Spikes**: Techniques like priority-based scheduling, preemption, and a mix of on-demand, spot, and reserved instances for cost efficiency and GPU utilization.
3. **Inference Latency Requirements**: Techniques like quantization and pruning to reduce model size and improve inference latency on vehicles.

## AWS Services Enabling Innovation at Zoox

- **ML Capacity Blocks**: Reserving GPU capacity for specific dates and times, enabling Zoox to run experiments beyond scheduled GPU availability.
- **Amazon S3 Intelligent-Tiering**: Automatically optimizing storage costs based on access patterns for Zoox's vast data lake.
- **Amazon FSx for Lustre**: High-performance file system for low-latency access to data from S3, enabling efficient model training on GPUs.
- **Amazon OpenSearch Service**: Log analytics, vector storage, and nearest neighbor searches for ML models and embeddings.