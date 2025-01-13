# Summary of AWS re_Invent 2024 - BMW speeds car development with a new app for defect ticket routing (PRO201).txt

# Summary: BMW Speeds Car Development with a New App for Defect Ticket Routing

## Introduction

- BMW aims to provide premium digital experiences for its customers, in addition to the driving experience.
- BMW's software development process involves various stages, from unit testing to vehicle testing, where defect tickets are generated.
- The ticketing process faces challenges like inconsistent quality, unclear responsibilities, hidden dependencies, and duplicate tickets.

## Solution Overview

- BMW partnered with the AWS Generative AI Innovation Center to develop a generative AI companion to improve the ticket routing process.
- The solution involves four main stages:
  1. **Ticket Enrichment**: Using a large language model (LLM) to summarize tickets, eliminate acronyms, reduce redundancies, and translate tickets into a consistent language.
  2. **Finding Duplicates**: Performing a hybrid search using keyword matching and semantic vector embeddings to retrieve potential duplicate tickets.
  3. **Duplicate Classification**: Using an LLM to compare the new ticket with the retrieved candidates and classify whether they are duplicates, providing explanations.
  4. **Human Decision**: Presenting the top candidates to a human expert for final decision and feedback, enabling continuous improvement through reinforcement learning.

## Key Benefits

- Improved ticket quality and consistency
- Reduced duplication of work for developers by detecting duplicate tickets
- Uncovered additional insights and context from related data sources
- Accurate routing of tickets to the right team
- Increased transparency and traceability of the ticketing process

## Lessons Learned

- Generative AI adds value when applied with a value-added approach focused on specific business outcomes.
- Involving subject matter experts and business owners is crucial for understanding the problem and applying generative AI effectively.
- Investing in people with both technical AI and domain knowledge is essential.
- A reinforcement approach with human feedback creates a flywheel effect, leading to higher quality data, faster resolution, and continuous improvement.

## Conclusion

- The generative AI companion solution demonstrated significant impact during the proof-of-concept phase at BMW.
- The solution addresses key challenges in the ticketing process and provides a scalable approach to improve efficiency and quality.
- BMW plans to continue exploring generative AI applications in collaboration with the AWS Generative AI Innovation Center.