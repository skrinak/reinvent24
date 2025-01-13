# Summary of AWS re_Invent 2024 - Centric Brands_ A journey using AWS analytics and Amazon services (BWP303).txt

# AWS re:Invent 2024 - Centric Brands: A Journey Using AWS Analytics and Amazon Services

## Summary

### Introduction

- Madhav Gupta, a senior solution architect at Buy with Prime, introduced the session and the speakers.
- Blair Rafuse, the senior director of e-commerce at Centric Brands, co-presented the session.
- The session focused on Centric Brands' journey in integrating with Buy with Prime and leveraging AWS analytics services.

### About Centric Brands

- Centric Brands is a global lifestyle brand collective that designs, develops, sources, retails, and markets various products.
- They own and operate under license for over 100 brands, including Calvin Klein, Tommy Hilfiger, Joe's Jeans, Under Armour, Disney, and Coach.
- Centric Brands has a strong direct-to-consumer (D2C) e-commerce portfolio with 11 websites and growing.
- The IZOD brand, a classic American apparel brand, was the focus of the session.

### IZOD's E-commerce Journey

- In 2021, Centric Brands aimed to launch a cutting-edge website for IZOD by Black Friday-Cyber Monday.
- However, their 3PL partner couldn't handle the combined wholesale and D2C demand, leading to the website being shelved.
- The global supply chain crisis further delayed the D2C launch.
- Centric Brands needed a solution to operate D2C like wholesale from a logistics perspective, which led them to Amazon Buy with Prime.

### Choosing Buy with Prime

- Speed to market was critical, and Buy with Prime enabled a launch within four months.
- Amazon's fulfillment network provided infinite scale and top-notch service.
- Native integration with their e-commerce platform and free Prime delivery/returns were key benefits.
- Product review syndication from Amazon.com and a trusted checkout experience were valuable features.
- Amazon's robust API capabilities for data analytics and financial reconciliation were crucial.

### Integrating with Buy with Prime and AWS Services

- Centric Brands needed to integrate with multiple Amazon services (Buy with Prime, Multi-Channel Fulfillment, and Amazon Pay) to get the required data.
- Manually joining data from these services was challenging, leading to the development of an analytics solution using AWS services.

### Analytics Solution Architecture

- The solution followed an Extract, Transform, Load (ETL) process to load data into Centric Brands' downstream systems.
- The extract layer used Amazon EventBridge Scheduler to trigger AWS Lambda functions, pulling data from various sources and storing it in Amazon S3.
- The transform layer utilized AWS Glue for schema validation, data cleaning, and filtering, storing the transformed data in S3.
- The load layer used AWS Lambda to load the transformed data into Centric Brands' downstream systems.
- Terraform was used for infrastructure provisioning and deployment across multiple environments.

### Current Status and Future Plans

- Centric Brands successfully launched the revamped IZOD.com website in June 2024, leveraging Buy with Prime and the analytics solution.
- They continue to scale their e-commerce business and support the new technology stack.
- The partnership with Amazon is growing stronger, with plans to onboard more brands onto Buy with Prime and explore moving existing assets to AWS.

## Key Insights and Conclusions

- Buy with Prime enabled Centric Brands to offer Prime benefits on their D2C website, providing a seamless shopping experience.
- Integrating with multiple Amazon services required a robust analytics solution to consolidate and reconcile data.
- AWS services like EventBridge, Lambda, Glue, and S3 played crucial roles in the ETL process and data management.
- Terraform facilitated infrastructure provisioning and deployment across multiple environments.
- The successful integration and analytics solution allowed Centric Brands to optimize their processes and scale their e-commerce business.
- The partnership with Amazon continues to strengthen, with plans for further expansion and adoption of AWS services.