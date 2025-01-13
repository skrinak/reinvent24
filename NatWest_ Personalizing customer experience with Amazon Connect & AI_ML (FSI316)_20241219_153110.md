# Summary of AWS re_Invent 2024 - NatWest_ Personalizing customer experience with Amazon Connect & AI_ML (FSI316).txt

# Summary: NatWest's Journey with Amazon Connect and AI/ML for Personalizing Customer Experience

## Introduction

- NatWest is a FTSE 100 UK-based bank with 19 million customers across retail, commercial, and affluent businesses.
- Despite the adoption of digital channels, NatWest's contact centers play a crucial role, handling 25 million calls annually with 9,000 agents across 9 contact centers.
- NatWest migrated to Amazon Connect to leverage its rich data and AI/ML capabilities to improve customer and agent experiences.

## Migration to Amazon Connect

- NatWest started the migration journey in 2019, piloting with the credit card center.
- By the end of 2022, they received full approval to migrate all 9 contact centers and 9,000 agents to Amazon Connect.
- The migration was completed in 1 year and 10 months, spanning 22 migration events, with the final contact center migrated by October 2024.
- The migration approach involved changing the direct dial numbers pointed to Amazon Connect while keeping production traffic on the legacy system, minimizing risk and disruption.

## Benefits of Amazon Connect

1. **Data-driven Insights**:
   - Amazon Connect provides rich data, including contact trace records, call transcriptions, and agent data.
   - NatWest leverages this data to improve customer and agent experiences through initiatives like sentiment analysis-driven coaching and identifying and addressing call hangups.

2. **Speed and Agility**:
   - NatWest implemented over 30 new self-serve journeys in the telephony estate within 3 weeks, a process that previously took 6 months.
   - The pay-as-you-go model incentivizes optimization, as improvements in customer experience and reduced call volumes directly impact costs the following month.

3. **Simplified Architecture**:
   - Amazon Connect consolidated NatWest's previously distributed architecture, reducing complexity and enabling cost savings.
   - Features like speech analytics, call recordings, and NLCS (Natural Language Call Steering) are now available out-of-the-box.

## Leveraging AI/ML

1. **Natural Language Call Steering (NLCS)**:
   - NatWest implemented a Lex chaining architecture with parent and child Lex bots to handle over 1,700 intents more effectively.
   - A federated development model allows the business to update NLCS utterances and mappings, enabling fortnightly releases instead of months.

2. **Amazon Q Integration**:
   - NatWest experimented with Amazon Q to support agents in getting to the right outcomes and actions faster, aiming to reduce average handle time (AHT) and improve NPS.
   - Learnings include the importance of structured knowledge articles and considering agent conversations in intent recognition.

3. **Future Initiatives**:
   - NatWest is exploring call summarization using AI to reduce agent wrap-up time.
   - Agent Evaluate is being tested to automatically analyze calls against predefined rules, enabling targeted coaching and process adherence monitoring.

## Conclusion

NatWest's journey with Amazon Connect and AI/ML has enabled data-driven insights, improved customer and agent experiences, and architectural simplification. The integration of AI/ML capabilities like NLCS, Amazon Q, call summarization, and Agent Evaluate is driving further optimization and personalization of the customer experience.