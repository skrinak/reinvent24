# Summary of AWS re_Invent 2024 - How the PGA TOUR is transforming live player commentary in golf (SPT209).txt

# Summary: How the PGA TOUR is Transforming Live Player Commentary in Golf

## Introduction
- The session discusses how the PGA TOUR, in collaboration with NLP Logix and AWS, is transforming the live golf viewing experience by providing AI-generated commentary for every shot during a tournament.

## The Challenge
- Golf is not a linear sport, making it difficult for fans to follow their favorite players continuously.
- The goal was to provide an immersive experience by generating accurate and contextually relevant commentary for all 32,000 shots in a tournament, with minimal human involvement.

## The Solution
- The team leveraged AWS Generative AI services and Amazon Bedrock to develop a solution that generates real-time commentary for every shot.
- A gold standard dataset of 30-35 examples of good commentary was created to train and validate the AI models.
- Amazon Bedrock's features like guardrails and real-time validation ensured accuracy and brand alignment.
- The PGA TOUR's domain expertise in golf was crucial in structuring the data and providing context to the AI models.

## Operationalizing the Solution
- Validating the generated commentary for accuracy and writing style was a critical step.
- A scoring system was implemented to determine if the commentary should be published directly, regenerated, or sent for human review.
- Continuous monitoring and incorporating feedback are essential to adapt to changing conditions.

## Key Takeaways
- Understand the problem and focus on delivering an accurate and maintainable solution, rather than rushing to adopt the latest tools.
- Start with validation datasets to ensure the solution works at scale and instill confidence in leadership.
- Embrace a culture of innovation and be willing to experiment, iterate, and discard ideas if necessary.
- Leverage domain expertise and collaborate across teams for successful AI implementation.
- Continuously monitor and incorporate feedback to adapt to changing conditions.

## Conclusion
The PGA TOUR's collaboration with NLP Logix and AWS has resulted in a successful AI-driven solution that enhances the golf viewing experience by providing real-time, contextually relevant commentary for every shot during a tournament.