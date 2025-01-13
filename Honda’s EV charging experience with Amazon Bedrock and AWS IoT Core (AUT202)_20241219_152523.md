# Summary of AWS re_Invent 2024 - Honda’s EV charging experience with Amazon Bedrock and AWS IoT Core (AUT202).txt

# Honda's EV Charging Experience with Amazon Bedrock and AWS IoT Core

## Overview

This presentation showcased the collaboration between Honda and AWS to improve the electric vehicle (EV) charging experience for customers using software-defined vehicles (SDV) and AWS technologies. The key points covered were:

## Honda's Vision

- Honda aims to achieve carbon neutrality and zero traffic fatalities involving its vehicles by 2050.
- The Honda 0 Series lineup of EVs will be launched in 2026, featuring SDV technology to enhance the value of EVs and improve people's quality of life.
- Honda envisions providing a seamless EV charging experience that eliminates range anxiety and perceived charging time.

## Challenges in EV Charging

- Lack of charging stations and limited driving range per charge are major concerns for EV buyers.
- Pain points in the EV charging journey include trip planning, locating charging spots, and waiting times.

## Honda's Solutions

1. Eliminate time wasted searching for optimal charging spots.
2. Provide guidance to charging points, even in unfamiliar locations.
3. Enable simple payment methods.

## AWS Technologies

- **AWS IoT Core**: Collect real-time vehicle data, including battery status, charging patterns, and driving behavior.
- **Amazon Bedrock**: Analyze data from IoT Core and historical trip data to understand driver preferences and provide personalized charging station recommendations.

## Key Benefits

- Personalized EV experience tailored to individual usage habits, charging preferences, and frequently visited locations.
- Optimized route planning and enhanced overall EV ownership experience.

## Demo: Smart Routing

A demo showcased a proof-of-concept (POC) solution called "Smart Routing," which provides personalized charging plans and routes based on user preferences and interests. Key features included:

- Learning user interests from historical data using Amazon Location Service and Amazon Bedrock.
- Implementing business logic with AWS Lambda, API Gateway, and DynamoDB.
- Calling external APIs for real-time data like traffic conditions and charging station status.
- Leveraging Amazon Bedrock's generative AI to recommend the best route and plan based on user preferences and nearby points of interest.

The demo illustrated how different personas (e.g., a golf enthusiast and a family) would receive tailored recommendations for charging stops and activities based on their interests and vehicle types.

In conclusion, the collaboration between Honda and AWS aimed to address EV charging challenges by leveraging AWS IoT Core, Amazon Bedrock, and other services to provide a personalized, intelligent, and user-friendly EV ecosystem.