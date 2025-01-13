# Summary of AWS re_Invent 2024 - Tool use & agents at the frontier_ Advanced techniques for LLM actions (AIM306).txt

Here is a comprehensive summary of the transcript, formatted in Markdown with appropriate headers and bullet points:

# AWS re:Invent 2024 - Tool use & agents at the frontier: Advanced techniques for LLM actions (AIM306)

## Introduction

- Large Language Models (LLMs) have evolved quickly, and the promise of automation using these models is becoming a reality.
- This talk covers reasoning, planning, orchestration, and tool use with LLMs.

## What is Function Calling or Tool Use?

- Function calling, also known as tool use, allows LLMs to read from and write to the outside world.
- It started as a way to provide real-time data to LLMs, which were previously limited to their training data.
- The model is given access to a set of tools or functions and can call them to retrieve or manipulate data.

## Best Practices for Tool Use

- Provide a function calling syntax and available functions in the prompt.
- Combine the prompt with the user message.
- Generate a model response and check if it contains a function call.
- Parse and execute the function call using traditional software.
- Pass the results back to the model, along with the previous context.
- Repeat until the model doesn't call a function, indicating it has an answer.

## Origins of Function Calling

- The "Miracle Systems MRKL" paper in 2022 had a significant impact on the architecture and evolution of agents and function calling.
- It showed that LLMs struggle with multi-digit arithmetic due to limited exposure during training.
- Providing a calculator tool and prompting the model to use it brought accuracy back to near 100%.

## Combining LLM Knowledge with Function Calling

- LLMs can leverage their pre-trained knowledge, including business domain knowledge, and combine it with function calling to solve complex problems.
- Example: Calculating the percentage return for a stock symbol using a price tool and Claude's understanding of financial practices.

## What are Agents?

- The term "agent" has become overloaded, with no consensus on its definition.
- Agents can be viewed on two axes: agency (the model's autonomy) and effect (the impact of the model's actions, including tool use).
- Different perspectives exist, from considering any model response an agent to requiring virtual employee-level capabilities.

## Agent Orchestration

- Orchestration styles govern how agents plan and execute tasks.
- ReAct (Reason and Action) is the default orchestrator in Amazon Bedrock agents, where the model develops a plan and decides the next action at each step.
  - Advantages: Accurate, resilient, works naturally with tool use.
  - Disadvantages: Latency, may forget plans over longer trajectories, difficult to follow a predefined plan.
- ReWoO (Reason Without Observation) prompts the model to output all steps at once, reducing latency but requiring more code to handle dependencies.
- Custom orchestrators can be used, allowing flexibility in prompt engineering.

## Complex Example with an Agent

- Calculating the annualized volatility of the S&P 500 based on the past 30 days, using a price tool and a code interpreter.
- The agent combines Claude's business domain knowledge with tool use to solve the problem, generating code to calculate log returns, standard deviation, and annualized volatility.

## Considerations for Agents and Tool Use

- Choose an orchestration style based on requirements (latency, plan flexibility, resilience).
- Decide between generic tools (e.g., code interpreter, database access) or specific tools for accuracy vs. versatility trade-offs.
- Explore the model's business domain knowledge through prompt engineering.

## Conclusion

- Function calling is a powerful construct supported by advanced models like Claude, utilizing tools and business domain knowledge to solve complex problems with a standardized syntax.
- Agents build on function calling, providing planning and orchestration to automate work using generative AI models on Amazon Bedrock.

## Resources

- Blogs and additional resources are provided for further learning.