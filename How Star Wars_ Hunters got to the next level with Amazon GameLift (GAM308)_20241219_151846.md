# Summary of AWS re_Invent 2024 - How Star Wars_ Hunters got to the next level with Amazon GameLift (GAM308).txt

# Summary

## Main Points

1. **Overview of Star Wars: Hunters**
   - Star Wars: Hunters is a 4v4 arena-based combat game developed by NaturalMotion within Zynga.
   - It's a character class-based game focused on multiplayer gameplay.
   - The game is available on iOS, Android, Nintendo Switch, and will be released on PC in early access next year.

2. **Requirements for a Multiplayer Game**
   - Fair matchmaking: Matching players with similar skill levels.
   - Low latency: Matching players in the same region for low latency.
   - Quick matchmaking: Minimizing the time players spend in queues.

3. **Using Amazon GameLift**
   - GameLift provides global presence, cost optimization, and built-in matchmaking capabilities.
   - Key GameLift resources used: FlexMatch rule sets, game builds, instances, fleets, and game session queues.
   - Metrics tracked: Instance-level metrics, matchmaking time, fleet utilization, inventory counts, and transactions per second.

4. **FleetDeployer Tool**
   - A custom tool built by NaturalMotion to simplify the deployment and management of GameLift resources.
   - Allows non-engineering teams to spin up and manage deployment groups without understanding GameLift internals.
   - Provides features like scheduled scaling, automatic shutdowns, and cost estimation.

5. **Integration with Unreal Engine**
   - Implemented GameLift integration within the Unreal game server.
   - Used platform services as the central communication point for matchmaking.
   - Developed a matchmaking simulator tool to fine-tune matchmaking rules.

6. **Launch Successes**
   - Scaling met player demand during launch week.
   - Ability to optimize costs by leveraging Spot instances.
   - Adjusting matchmaking rules on the fly.
   - Excellent support from the Amazon GameLift team.

7. **Recommendations**
   - Consider latency requirements for multi-region fleets.
   - Define matchmaking goals and data requirements.
   - Determine appropriate instance types and game session capacity.
   - Decide on the extent of GameLift integration and testing strategies.

8. **GameLift Anywhere**
   - Allows setting up a local GameLift-like environment for testing.
   - Enables easy transition from local testing to a GameLift Managed Fleet.
   - Recommended for local development and future game iterations.

## Key Insights

- Amazon GameLift provides a comprehensive solution for managing multiplayer game servers, matchmaking, and scaling, enabling a smooth launch experience.
- Building custom tooling like FleetDeployer can simplify the management of GameLift resources and enable non-engineering teams to participate in the deployment process.
- Thorough testing, including load testing and matchmaking simulations, is crucial for fine-tuning matchmaking rules and ensuring a successful launch.
- Leveraging Spot instances and multi-region fleets can optimize costs and provide global coverage for multiplayer games.
- Close collaboration with the Amazon GameLift team and their support during the launch phase is invaluable.

## Important Conclusions

- Amazon GameLift, combined with custom tooling and thorough testing, enabled a successful and smooth launch for Star Wars: Hunters, meeting player demand and optimizing costs.
- Careful consideration of latency requirements, matchmaking goals, instance types, and integration strategies is essential when adopting GameLift for multiplayer games.
- GameLift Anywhere provides a valuable local testing environment for game development and future iterations, enabling seamless transition to a GameLift Managed Fleet.