# Simple ReAct Agent Experiment

This project demonstrates a basic implementation of a ReAct (Reason + Action) agent using OpenAI's GPT model. The agent processes user queries in a structured loop of thought, action, and observation to reach answers. The experiment showcases:

- **ReAct Pattern**: The agent follows a specific sequence of reasoning ("Thought"), performing an action, pausing for an observation, and providing an answer.
- **Action Handling**: Available actions include calculations and retrieving average weights for certain dog breeds, executed via predefined Python functions.
- **Interactive Loop**: Through the `query` function, the agent processes multiple rounds of input, identifying and running actions until an answer is reached.

This experiment provides a foundation for building agents that handle logical reasoning and dynamic actions in response to user queries.
