
# Lesson 4: Persistence and Streaming

This lesson explores the use of state persistence and streaming within an agent framework using LangGraph. The agent interacts with an external tool, stores conversational states using SQLite, and streams responses for real-time interaction.

### Prerequisites

- Python 3.8+
- Required packages: `dotenv`, `sqlite`, `langgraph`, `langchain_openai`, and relevant utilities.

### Experiment Overview

1. **Environment Setup**:
   - Loads environment variables for API keys and other configurations using `dotenv`.

2. **Tool and State Management**:
   - Implements `TavilySearchResults` tool to retrieve search results, integrating it within the agent.
   - Stores agent messages and states using `SqliteSaver` and `AsyncSqliteSaver` for synchronous and asynchronous data handling.

3. **Agent Configuration**:
   - Defines an `Agent` class equipped with a state graph for managing dialogue and tool actions.
   - Uses checkpointing for state persistence, allowing conversations to resume from previous states if interrupted.

4. **Streaming Responses**:
   - Demonstrates streaming of responses, which is useful for handling long outputs or interactive queries.
   - Supports asynchronous streaming with `astream_events`, allowing token-by-token streaming output.

### Usage Example

To start a search and handle responses:

```python
messages = [HumanMessage(content="What is the weather in sf?")]
thread = {"configurable": {"thread_id": "1"}}

for event in abot.graph.stream({"messages": messages}, thread):
    for v in event.values():
        print(v['messages'])
```

To asynchronously stream responses:

```python
messages = [HumanMessage(content="What is the weather in SF?")]
thread = {"configurable": {"thread_id": "4"}}
async for event in abot.graph.astream_events({"messages": messages}, thread, version="v1"):
    kind = event["event"]
    if kind == "on_chat_model_stream":
        content = event["data"]["chunk"].content
        if content:
            print(content, end="|")
```

### Key Features

- **Persistence**: Maintains conversational state across interactions using SQLite for flexible recovery and session management.
- **Streaming**: Enables real-time response output, useful for interactive applications.
- **Checkpointing**: Incorporates SQLite checkpointing to enable a modular and recoverable dialogue flow.

### Additional Notes

- **Error Handling**: Error handling is demonstrated to manage interruptions in streaming and unexpected tool responses.
- **Thread IDs**: Thread IDs allow multiple conversation threads to be managed independently.

### License

This experiment is for educational purposes only.
