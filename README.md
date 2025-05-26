# MultiAgents Project

![License](https://img.shields.io/github/license/henriquevs/multiAgents)
![Last Commit](https://img.shields.io/github/last-commit/henriquevs/multiAgents)

## Overview

The MultiAgents project is a collection of experiments and implementations exploring various frameworks and techniques for building intelligent agents. Each subdirectory focuses on a specific domain or framework, providing modular and extensible solutions for different use cases.

## Directory Structure

### `ai_voice_agents/`

- **1_voice_agent_components/**: Implements foundational components for voice-based AI agents, including speech-to-text (STT), text-to-speech (TTS), and natural language processing (NLP). [Explore Components](./ai_voice_agents/1_voice_agent_components/project.ipynb)
- **2_optimizing_latency/**: Focuses on optimizing latency in voice interactions and collecting performance metrics. [Optimize Latency](./ai_voice_agents/2_optimizing_latency/project.ipynb)

### `web_agents/`

- **1_simple_web_agent/**: Basic web agent implementation and demonstration. [Simple Web Agent](./web_agents/1_simple_web_agent/project.ipynb)
- **2_autonomous_web_agents/**: Advanced autonomous web agent using the MultiOn API, with session management, navigation, and task execution. Includes workflows for automating real-world web tasks and a demo interface for step-by-step task execution and visualization. [Autonomous Web Agent](./web_agents/2_autonomous_web_agents/project.ipynb)
- **3_agentQ_MCTS/**: Integration of AgentQ and Monte Carlo Tree Search (MCTS) for web-based environments. Features gridworld visualization, browser-based agent planning, and tools for analyzing the agent's search tree and decision process. [AgentQ & MCTS](./web_agents/3_agentQ_MCTS/project.ipynb)

### `advanced_crewAI/`

- Contains lessons (L1 to L6) exploring advanced AI techniques for crew management and decision-making. [Explore Advanced CrewAI](./advanced_crewAI/)
- Includes visualizations, data analysis, and configuration files for various experiments.

### `code_agents/`

- **1_intro_to_code_agents/**: Introduces code agents and their applications. [Introduction to Code Agents](./code_agents/1_intro_to_code_agents/project.ipynb)
- **2_secure_code_execution/**: Explores secure execution environments for code agents. [Secure Code Execution](./code_agents/2_secure_code_execution/project.ipynb)
- **3_monitoring_evaluating_agent/**: Focuses on monitoring and evaluating agent performance. [Monitor and Evaluate Agents](./code_agents/3_monitoring_evaluating_agent/project.ipynb)
- **4_deep_research_agent/**: Implements agents for deep research tasks. [Deep Research Agent](./code_agents/4_deep_research_agent/project.ipynb)

### `crewAI/`

- Contains lessons (L2 to L7) focused on customer support, outreach, event planning, and other business-related tasks. [Explore CrewAI](./crewAI/)
- Includes utilities and instructions for implementing and testing AI solutions.

## Requirements

Each subdirectory has its own `requirements.txt` file specifying the dependencies for the experiments within that folder. Ensure you install the required packages before running the code in a specific subdirectory.

## How to Use

1. Navigate to the desired subdirectory.
2. Install dependencies using:

   ```bash
   pip install -r requirements.txt
   ```

3. Open the relevant Jupyter Notebook or Python script to explore the experiments.

## Future Work

- Expand the scope of experiments to include more frameworks and use cases.
- Enhance modularity and reusability of agent components.
- Optimize performance across all implementations.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
