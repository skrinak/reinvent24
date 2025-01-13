# Summary of AWS re_Invent 2024 - Effortless game launches_ How League of Legends runs at scale on AWS (GAM307).txt

# Summary

## Main Points

1. **Riot Games and AWS Partnership**
   - Riot Games, an AAA game studio, partnered with AWS in 2022 to leverage cloud technologies for their games.
   - They accomplished milestones like the first global power rankings for eSports, best-in-class remote broadcast center, and migrating Riot's data centers to AWS.

2. **League of Legends Architecture**
   - League of Legends has a client-server architecture with platform servers for out-of-game experiences and game servers for in-game experiences.
   - Game servers have unique requirements like low latency, high computational power, and individual addressability.

3. **Challenges with On-Premises Infrastructure**
   - Scaling was difficult, leading to overprovisioning and waste.
   - DDoS protection appliances had limitations like supporting only 255 games per host and two game versions.
   - Running Windows game servers had licensing costs and management overhead.

4. **Migration to AWS and Linux**
   - Valorant, a new game, was launched on AWS with Linux game servers, containers, and auto-scaling, prompting League of Legends to follow suit.
   - Challenges included porting the game server codebase from Windows to Linux and handling platform-specific bugs.

5. **Game Provisioning Platform (GPP)**
   - Riot's Player Platform team developed GPP, a cloud-based game provisioning platform, to address League of Legends' needs.
   - GPP supports auto-scaling, native patcher support, and end-of-game processing.

6. **Auto-Scaling and Cost Optimization**
   - Auto-scaling thresholds were optimized using simulations and load balancing algorithms like Round Robin.
   - This led to significant cost savings of up to 50% and $10 million yearly.

7. **Player Experience Improvements**
   - Auto-scaling enabled supporting new game modes like Swarm and TFT with different performance profiles.
   - Latency-based matchmaking and geographical optimization became possible.

8. **Future Plans**
   - Expanding GPP to other Riot games and exploring new features like running on Graviton instances.
   - Supporting non-match-based, evergreen game servers for upcoming MMO titles.

## Key Insights

- Cloud technologies like auto-scaling and containerization enabled significant cost savings and flexibility for Riot Games.
- Migrating a long-running game like League of Legends to a new infrastructure required careful planning, simulations, and addressing platform-specific challenges.
- A centralized game provisioning platform (GPP) allowed Riot to standardize and optimize game server deployment across multiple titles.
- Auto-scaling not only reduced costs but also unlocked new player experiences and game modes that were previously impractical.

## Important Conclusions

- Leveraging cloud technologies like AWS can provide substantial benefits for game studios, including cost savings, scalability, and improved player experiences.
- Migrating legacy games to the cloud requires addressing technical challenges and reevaluating assumptions, but the benefits can be significant.
- Centralized platforms like GPP can streamline game server management and enable innovation across multiple titles.
- Continuous optimization, simulations, and data-driven decision-making are crucial for maximizing the benefits of cloud infrastructure.