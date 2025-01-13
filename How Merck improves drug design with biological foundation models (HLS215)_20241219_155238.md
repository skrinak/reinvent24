# Summary of AWS re_Invent 2024 - How Merck improves drug design with biological foundation models (HLS215).txt

# Summary

## Introduction
- The talk focuses on how Merck is using state-of-the-art biological foundation models (bio FMs) to improve drug discovery.
- Aaron Friedman, a principal product manager at AWS, introduces the topic and discusses the importance of computational approaches in drug discovery.
- Computation allows for generating more data points faster, breaking through bottlenecks, and testing hypotheses more efficiently.

## Biological Foundation Models in Drug Discovery
- Bio FMs have applications in various areas like drug design, biomarker discovery, target assessment, and more.
- There are different types of models emerging, from RNA/DNA-based algorithms to protein models, immunogenicity assessment, antibody design, and digital twins.
- Models like AlphaFold, ESMFold, RoseTTAFold, and others are revolutionizing protein structure prediction and design.
- Orchestration of these models is a key challenge, as organizations need to test, run, track, and swap different models and versions.

## AWS HealthOmics
- AWS HealthOmics is a service that helps customers get started with proven scientific recipes, adapt them to their needs, collaborate and share workflows, and scale up computations.
- It provides a way to run complex scientific workflows with a single API call, abstracting away the underlying infrastructure.
- Customers can use ready-to-run workflows or build their own private workflows, share them securely with collaborators, and run batch inferences at scale.

## Merck's Use Cases
- Matt Studney (VP of R&D IT at Merck) discusses how Merck has been partnering with AWS to unlock new capabilities and insights.
- Danny Bitton (from Merck's team) presents various use cases where HealthOmics has helped accelerate protein design:
  - Generative AI pipelines for creating thousands of protein designs at scale
  - Protein language models for antibody discovery and humanization
  - Collaborative protein annotation and design with Autoban
  - Molecular dynamics simulations for optimizing protein linkers and identifying cryptic pockets
  - Biocatalysis and enzyme engineering using machine learning models

## Conclusion
- The talk highlights the power of combining computational approaches, bio FMs, and traditional methods like molecular dynamics to accelerate drug discovery.
- AWS HealthOmics provides a streamlined way to orchestrate and scale these workflows, enabling organizations to focus on scientific outcomes rather than infrastructure.