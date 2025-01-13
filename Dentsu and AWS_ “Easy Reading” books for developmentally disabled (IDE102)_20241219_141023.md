# Summary of AWS re_Invent 2024 - Dentsu and AWS_ “Easy Reading” books for developmentally disabled (IDE102).txt

# AWS re:Invent 2024 - Dentsu and AWS: "Easy Reading" books for developmentally disabled

## Overview

Jeremy Bartosiewicz (AWS Solutions Architect) and Thiago Winkler (Head of Innovation at Dentsu Creative Brazil) presented their collaboration on the "Easy Reading" project, which aims to convert books into an accessible format for people with intellectual disabilities. The project utilizes generative AI models to simplify text, generate images, and produce easy-to-read versions of books following specific standards.

## Key Points

### Background
- Around 200 million people worldwide experience difficulties in reading literature due to intellectual disabilities.
- The "easy-to-read" standard, created in 2010, provides guidelines for making text more accessible, but the manual conversion process is lengthy and expensive.
- Visit Portugal approached Dentsu to explore new ways of promoting tourism through literature, making their classic books accessible to a wider audience.

### The Easy Reading Project
- Developed a platform that can upload a book, simplify the content, generate images, and produce a draft easy-to-read version.
- Follows the easy-to-read standards, with final review by experts.
- Utilizes various AWS services, including Amazon Bedrock for generative AI models.
- Iteratively improved the process and output quality over three months, evaluating multiple models.

### Technical Approach
- Used different models for specific tasks, such as text simplification, image generation, and book segmentation.
- Employed an orchestration engine built on AWS Step Functions to process the book chapter by chapter.
- Implemented rule sets to ensure compliance with easy-to-read standards.
- Incorporated human-AI collaboration, involving rights holders, easy-to-read specialists, and final editors.

### Impact and Benefits
- Reduced the conversion cost and time significantly compared to manual processes.
- Enabled scaling the solution to potentially serve the 200 million people with intellectual disabilities.
- Opened up opportunities to generate content in multiple formats (audio, podcasts) for different disability types.

### Future Developments
- Support multiple formats and content types.
- Leverage advancements in generative AI models for improved quality.
- Explore AWS Bedrock Flows for creating generative AI-specific workflows.

## Conclusion
The Easy Reading project showcases the potential of generative AI in making content more accessible for people with intellectual disabilities. Through collaboration between Dentsu and AWS, the solution demonstrates how AI can be used for good, enabling broader access to literature and promoting inclusivity.