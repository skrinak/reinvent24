# Summary of AWS re_Invent 2024 - How Supercell’s newest game launched with tens of millions of players (GAM309).txt

Here is a comprehensive summary of the transcript, formatted in Markdown with appropriate headers and bullet points:

# AWS re:Invent 2024 - How Supercell's newest game "Squad Busters" launched with tens of millions of players

## Introduction

- The session covers the journey of launching Supercell's latest game "Squad Busters" on AWS, which aimed to be their biggest launch ever, targeting tens of millions of players on launch day.
- Speakers: Phil Ward (AWS Technical Account Manager), Toni Syvanen (Supercell's Cloud Governance Engineer), and Tomi Joki-Korpela (Supercell's Server Engineer).

## About Supercell and "Squad Busters"

- Supercell's mission is to create games that players will remember forever and talk about with friends for years.
- "Squad Busters" is a 10-player multiplayer mobile game where players compete to collect gems, with a global player base and cross-game promotions from other Supercell titles.
- Over 40 million players pre-registered for the game, indicating significant interest.

## Technical Architecture and Preparation

- "Squad Busters" has a stateful architecture with real-time multiplayer simulation, running on both client and server.
- The server is the authoritative source, and the game state is stored with the application, reducing database load.
- The architecture includes a main site for non-battle operations and battle sites spread across AWS regions for low-latency gameplay.
- Extensive load testing was conducted to estimate the required server capacity, targeting 4 million concurrent players on launch day.
- Load testing used a custom client that simulates real players, with tests running up to 100,000 concurrent players or more.
- AWS Countdown Premium was leveraged for dedicated support engineers and architectural guidance during the launch.

## Launch Day Execution

- On launch day, Supercell had 2,300 servers across 7 AWS regions, with over 15,000 CPUs and 20 Aurora database clusters ready.
- Within 30 minutes of the app store launch, 200,000 concurrent players joined, reaching 1 million within 2 hours, even before marketing activities began.
- The launch saw a peak of 17 million players joining within the first 24 hours, making it Supercell's biggest launch ever.
- AWS Countdown engineers provided real-time capacity warnings, though Supercell had over-provisioned capacity for the launch.

## Key Takeaways

- Eliminate unknowns through extensive load testing, quota checks, and involving AWS teams early in the preparation process.
- Leverage AWS Countdown for architectural guidance and dedicated support during critical events like game launches.
- Resources for running game workloads on AWS were shared, including a game industry guide to re:Invent.