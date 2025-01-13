# Summary of AWS re_Invent 2024 - Accelerate innovation with generative AI and no-code machine learning (AIM227).txt

Here is a comprehensive summary of the transcript, formatted in Markdown with appropriate headers and bullet points:

# AWS re:Invent 2024 - Accelerate innovation with generative AI and no-code machine learning

## Introduction

- The session covered how to accelerate machine learning without writing code using Amazon SageMaker Canvas.
- It demonstrated how SageMaker Canvas enables building high-quality ML models without coding or deep ML expertise.
- A success story from Gosoft Thailand showcased the tangible business benefits achieved using SageMaker Canvas.

## SageMaker Canvas: No-Code Machine Learning

- SageMaker Canvas is a visual, no-code interface for end-to-end machine learning.
- It provides access to ready-to-use ML models, including foundation models, without needing ML knowledge.
- Key features of SageMaker Canvas:
  - End-to-end model building: data preparation, training, deployment, without writing code.
  - Exports models as Python code and Jupyter Notebooks for collaboration with data scientists.
  - Supports a variety of domains and use cases: forecasting, regression, classification, computer vision, NLP, and fine-tuning foundation models.

### Data Preparation

- Connect to 50+ data sources (AWS, third-party).
- Automate data preparation pipelines to scale to petabytes of data.
- Generate detailed data insights and quality reports with recommendations.
- Built-in visualizations and 300+ transformations for data preparation.
- Support for natural language instructions for data transformations and visualizations.

### Model Training

- Leverages AutoML techniques (hyperparameter optimization, ensembling) to build high-quality models.
- Suggests default configurations but allows customization.
- Detailed model insights (metrics, feature importance, leaderboard) for evaluation.
- Fine-tune foundation models from Amazon Bedrock and SageMaker JumpStart.

### Model Deployment and Collaboration

- In-app predictions and "what-if" analysis for model evaluation.
- Batch predictions and automated scheduling.
- Deploy models for real-time inference on SageMaker Endpoints.
- Share predictions and models with Amazon QuickSight for predictive analytics dashboards.
- Export models to SageMaker Model Registry for ML ops and governance.
- Share Jupyter Notebooks with data scientists for collaboration and iteration.

## Forecasting Demo with SageMaker Canvas

- Demonstrated the end-to-end process of building time series forecasting models using SageMaker Canvas.
- Covered data preparation, model training, evaluation, and making predictions.
- Highlighted the architecture created with Gosoft Thailand for training and inference pipelines.
- Explained the concept of back-testing and balancing supply dilemmas using quantile forecasts.

## Gosoft Thailand Success Story

- Gosoft Thailand (IT arm of CP Group, owner of 7-Eleven Thailand) implemented an AI demand forecasting solution using SageMaker AutoML.
- Key objectives: simplify replenishment activity, handle massive data cost-effectively, and improve accuracy.
- Leveraged AWS services like Step Functions, Glue, S3, and SageMaker AutoML.
- Achieved significant results:
  - Reduced time for replenishment from 120 minutes to 1.5 minutes (95% improvement).
  - Decreased stock days by 5%.
  - Reduced stock-outs by 40%.
  - Enabled store staff to focus on customer service instead of forecasting.

## Conclusion

- SageMaker Canvas enables accelerating machine learning innovation without writing code.
- Build high-quality ML models confidently and put them into production.
- Achieve tangible business results, as demonstrated by Gosoft Thailand's success story.