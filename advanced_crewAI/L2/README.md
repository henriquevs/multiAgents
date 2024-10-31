
# L2: Automated Trello Board Data Analysis and Reporting

This project automates the data collection, analysis, and reporting process for Trello board data, using specialized CrewAI agents to retrieve and process information efficiently.

## Key Components

- **Agents**: Two agents manage data collection and analysis tasks:
  - **Data Collection Agent**: Retrieves card details, activity, and attachments from a Trello board.
  - **Analysis Agent**: Analyzes the collected data to produce structured insights.

- **Tasks**: The agents perform specific tasks for comprehensive analysis:
  - **Data Collection**: Collects data from Trello cards, such as due dates, activity, and labels.
  - **Data Analysis**: Analyzes collected information for trends, completion rates, or any specified metrics.
  - **Report Generation**: Summarizes insights and compiles them into a report format.

## Usage Overview

1. **Define Agents and Tasks**
   - Configures CrewAI agents and tasks for data collection from Trello, analysis, and reporting.
2. **Run Analysis Workflow**
   - Execute the workflow to collect, analyze, and compile a report from the Trello data.
3. **Display Result**
   - Outputs a structured report in markdown format, along with cost metrics and usage insights.

### Example Code

```python
# Kick off the Crew
result = crew.kickoff()

# Display Results
import pandas as pd
from IPython.display import Markdown

# Display Cost Metrics
costs = 0.150 * (crew.usage_metrics.prompt_tokens + crew.usage_metrics.completion_tokens) / 1_000_000
print(f"Total costs: ${costs:.4f}")

# Display Analysis Result
Markdown(result.raw)
```

