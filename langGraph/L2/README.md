
# Lesson 2: LangGraph Components

This experiment demonstrates the use of LangGraph components to create a research assistant that leverages an OpenAI-based model to interact with a search engine tool. The assistant utilizes a state graph to manage agent states and actions for handling user queries effectively.

### Prerequisites

- Python 3.8+
- Install required packages from `requirements.txt` (not provided here but typically includes langchain-core, langgraph, and OpenAI libraries).

### Experiment Structure

1. **Environment Setup**:
   - Loads environment variables using `dotenv` for secure management of API keys and configurations.

2. **Tool Initialization**:
   - Uses `TavilySearchResults` tool to retrieve search results, with a maximum of 4 results for each query.

3. **Agent Class**:
   - Defines an `Agent` class that operates with a `StateGraph` to handle user queries, invoke model responses, and execute tool actions.
   - The agent includes error handling to address potential model hallucinations, where it retries in cases of invalid tool names.

4. **State Graph Configuration**:
   - Configures states and transitions in `StateGraph`:
     - `llm` node for invoking the language model (e.g., OpenAI's GPT).
     - `action` node for executing the appropriate tool action.
   - The graph ensures continuous operation by looping between `llm` and `action` states as necessary.

5. **Execution Flow**:
   - Demonstrates queries to the agent, including weather information retrieval and complex, multi-part questions, showcasing the assistant's ability to fetch and process information in sequence.

### Key Concepts

- **State Graphs**: Used to organize and manage agent states and interactions.
- **Agent Handling**: Manages errors gracefully to maintain smooth operation.
- **Tool Integration**: Integrates external tools and binds them to the model, allowing flexible information retrieval.

### Usage Example

Run the experiment by invoking `Agent` with queries such as:

```python
messages = [HumanMessage(content="What is the weather in SF and LA?")]
result = abot.graph.invoke({"messages": messages})
print(result['messages'][-1].content)
```

> **Note**: Results may vary over time as they depend on the latest information available from the search tool and model.

### License

This experiment is intended for educational purposes only.
