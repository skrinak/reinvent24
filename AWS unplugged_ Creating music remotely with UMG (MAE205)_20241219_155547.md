# Summary of AWS re_Invent 2024 - AWS unplugged_ Creating music remotely with UMG (MAE205).txt

# AWS re:Invent 2024 - AWS unplugged: Creating music remotely with UMG (MAE205)

## Introduction

- The music industry is experiencing explosive growth, with global music streaming revenue surpassing $20 billion and over 120,000 new tracks being released every day.
- Standing out in such a crowded market requires artists to focus on making their ideas as good as possible, as fast as possible, and getting them to other artists quickly.
- Collaboration is key, but distance remains a major challenge, adding cost and time delays.

## The Problem

- Traditional collaboration methods involve:
  - Traveling to the same location (expensive and inflexible)
  - Using video chat tools (not designed for real-time collaboration)
  - Exchanging files (loses creative momentum and slows the process)

## The Solution

- AWS, in partnership with Universal Music Group (UMG) and Open Sesame, has developed a solution to enable real-time, high-quality remote music collaboration.
- The solution leverages AWS cloud services and Open Sesame's patented SyncStage audio pipeline and Sync Studio application.

## Key Features

- Low latency (< 20-30 ms) for real-time collaboration
- High-quality audio (highest bit depth and sampling rate)
- Bidirectional audio for natural communication
- File storage with metadata for archiving takes
- Unified communication (headphone mix, talkback)

## Architecture

1. The producer launches the session and DAW (Digital Audio Workstation).
2. The producer invites artists and writers to the session via an invite code.
3. Participants authenticate and join the session.
4. The producer sets levels, creates the audio bridge, and launches the session.
5. Session files are written to block storage post-take.
6. Files can be archived in S3 for later use.
7. Notifications can be sent to collaborators about session updates.
8. Storage can be tiered for cost optimization.

## Demonstration

- A live demonstration was shown, featuring musicians in Nashville (Andy Wood and Eli Bishop) collaborating with a producer in Hoboken, NJ.
- The performance showcased the low latency, high-quality audio, and real-time collaboration capabilities of the solution.

## Next Steps

- Integrate video directly into the solution
- Implement a virtual patch bay
- Increase the bit rate for higher quality streams
- Enhance file storage options
- Improve login and access control

## Conclusion

The solution presented by AWS, UMG, and Open Sesame addresses a major challenge in the music industry by enabling real-time, high-quality remote collaboration for artists and producers. By leveraging cloud technologies, the solution promises to revolutionize the way music is created and accelerate the creative process.