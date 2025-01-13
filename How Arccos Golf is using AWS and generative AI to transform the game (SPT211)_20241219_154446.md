# Summary of AWS re_Invent 2024 - How Arccos Golf is using AWS and generative AI to transform the game (SPT211).txt

# AWS re:Invent 2024 - How Arccos Golf is using AWS and Generative AI to Transform the Game

## Overview

Ryan Johnson, VP of Software Engineering at Arccos Golf, presented their approach to using AWS and generative AI to enhance golf analytics and improve the golfing experience for their users. The key points covered in the presentation are:

## Challenges in Golf Analytics

- People generally have an aversion to complex analytics and prefer simple, one-dimensional metrics like fairways hit or number of putts, which have low predictive value.
- Advanced multi-dimensional analytics like "strokes gained" are highly probative but difficult for most golfers to comprehend.
- Communicating complex analytics effectively to users is a significant challenge.

## Arccos Driver Report: Using LLMs for Summarization

- Arccos developed a "Driver Report" to help golfers improve their driving performance, a critical aspect of the game.
- They used Large Language Models (LLMs) to summarize and communicate the complex driving data in a concise and understandable way.
- Key considerations:
    - Orchestrating the report generation process with AWS Step Functions
    - Choosing the right LLM model and optimizing prompts
    - Using XML data format and including charts/graphs for better LLM performance
    - Separating data analysis and summarization tasks for the LLM

## Ensuring Accuracy with LLMs

- Initially, the LLM outputs were inconsistently accurate, prompting concerns about the project's viability.
- They solved this by using a second LLM prompt to evaluate and correct the initial output, ensuring accuracy.
- The "LLM as a judge" concept proved to be a crucial solution for maintaining data integrity.

## LLMs for Golf Course and Pin Location Data

- Golf courses and pin locations vary widely, posing a challenge for accurate analytics.
- Arccos used LLMs to extract pin location data from course pin sheets, a task that would have been intractable without LLMs.
- This demonstrates the potential of LLMs for data capture and analysis, in addition to communication.

## Conclusion

Arccos Golf's experience highlights the potential of LLMs and generative AI in transforming complex data into actionable insights and improving user experiences, particularly in the sports analytics domain. Their approach emphasizes the importance of prompt engineering, model selection, and ensuring data accuracy while leveraging the power of LLMs for various tasks along the data pipeline.