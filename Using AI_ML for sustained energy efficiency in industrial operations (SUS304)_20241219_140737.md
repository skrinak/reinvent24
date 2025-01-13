# Summary of AWS re_Invent 2024 - Using AI_ML for sustained energy efficiency in industrial operations (SUS304).txt

# AWS re:Invent 2024 - Using AI/ML for Sustained Energy Efficiency in Industrial Operations

## Summary

### Introduction

- Energy consumption and its impact on the environment are crucial topics that affect individuals, businesses, and the planet.
- Amazon Web Services (AWS) is committed to sustainability and reducing its carbon footprint through renewable energy sources and energy-efficient operations.
- The session highlights two use cases where AWS customers, Volkswagen and Amazon, leveraged machine learning (ML) on AWS to reduce energy consumption and CO2 emissions in their operations.

### Volkswagen Poznan: Reducing Energy Consumption in Air Compressors

- Volkswagen Poznan aimed to optimize the energy consumption of air compressors in their factory, which accounted for 20% of the plant's total electricity usage.
- They developed an ML solution to predict future air consumption based on production schedules and derive an optimal compressor sequence to minimize energy loss.
- The solution architecture was built using AWS services like SageMaker, S3, Glue, and CloudWatch, following best practices for security, data management, and model deployment.
- By implementing the ML-driven approach, Volkswagen Poznan achieved:
  - 12% reduction in energy usage compared to their initial 5% target.
  - Savings of approximately 1,000 tons of CO2 emissions per year.
  - Cost savings of around $250,000 per year.
- The success of this use case has led Volkswagen to explore similar solutions for optimizing energy consumption in other areas, such as air ventilation, heating, cooling, and drying processes across their global manufacturing sites.

### Amazon: Optimizing HVAC Energy Consumption in Warehouses

- Amazon aimed to optimize the energy consumption of Heating, Ventilation, and Air Conditioning (HVAC) systems in their warehouses, which can account for 20-40% of a site's total energy consumption.
- They developed a prescriptive model that provides optimal schedules for HVAC systems by integrating weather forecasting data and site-specific data from sensors and meters.
- The model uses machine learning for predictive modeling and mathematical optimization techniques to minimize energy consumption while maintaining indoor temperature within a comfortable range.
- The solution architecture leverages AWS services like S3, Glue, SageMaker, Lambda, DynamoDB, and EC2 for data ingestion, preprocessing, model training, optimization, and execution.
- Preliminary results from applying the model to a single site on a summer day showed:
  - 25% reduction in energy consumption and carbon footprint.
  - Potential savings of 468 tons of CO2 emissions per year by scaling to a fraction of Amazon sites (equivalent to planting 22,000 trees annually).
  - Cost savings of approximately $395,000 per year.
- Amazon's long-term vision is to scale this solution across their entire network, enabling dynamic energy management and optimizing energy consumption across multiple sites and renewable energy sources.

### Conclusion

- The session showcased how Volkswagen and Amazon are leveraging AWS and machine learning to drive sustainability goals and reduce CO2 emissions in their industrial operations.
- The successful use cases demonstrate the potential for significant energy savings, cost reductions, and environmental impact through innovative applications of AI/ML technologies.
- AWS encourages attendees to explore resources and attend additional sessions on sustainable urban spaces and Volkswagen's platform strategy to learn more about these topics.