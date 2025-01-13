# Summary of AWS re_Invent 2024 - Fast evolving GraphQL schema with federation (BWP304).txt

# Summary

## Main Points

1. **Buy with Prime** is a service that allows merchants to offer Prime benefits (fast delivery, returns, customer service) on their websites, attracting more shoppers and increasing conversion rates.

2. **GraphQL Schema Versioning and Federation**:
   - Versioning challenges: Adding/removing fields, changing field types can break existing clients.
   - Solution: "Schema Projection" - a configuration layer that generates versioned schemas from a base schema using directives.
   - Allows independent teams to define schema changes, compose schemas, and manage releases.

3. **Federated Architecture**:
   - Pushed down GraphQL composition to individual services (products, inventory, etc.) for independent development and testing.
   - Used containers with shared networking (AWS Fargate) to minimize latency between composed services.
   - Included execution directives in schemas to delegate requests across versioned services.

4. **Release Management**:
   - Introduced "draft" and "release" states for schema projections.
   - Parent projections can only include released child projections.
   - Changes to released projections break the build, enforcing controlled releases.

5. **Generative AI for Test Case Generation**:
   - Used AI language models (LLMs) to generate comprehensive test cases from the schema definition.
   - Employed prompt engineering techniques (chain-of-thought, feedback loops) to improve test case quality.
   - Combined generative AI and programmatic approaches for synergistic benefits.

## Key Insights

- Versioning and federation allow evolving complex APIs while maintaining stability for existing clients.
- Pushing down composition enables independent development, testing, and controlled releases across teams.
- Generative AI can create comprehensive test cases, complementing programmatic approaches.
- Prompt engineering is crucial for effective use of AI in test case generation.

## Important Conclusions

- Buy with Prime's GraphQL API leverages versioning, federation, and generative AI to evolve rapidly while ensuring stability and quality.
- The architecture and processes allow independent teams to contribute while maintaining a cohesive, well-tested API surface.
- Combining programmatic and AI-driven approaches can provide a synergistic solution for comprehensive API testing.