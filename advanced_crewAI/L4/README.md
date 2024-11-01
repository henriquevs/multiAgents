
# L4: Automated Support Report Generation

This project automates the generation of support reports by orchestrating agents for suggestion generation, data analysis, table generation, and chart creation. Each agent in CrewAI contributes to producing a comprehensive report from support ticket data.

## Key Components

- **Agents**: Three agents manage specific aspects of report generation:
  - **Suggestion Generation Agent**: Analyzes support ticket data to generate recommendations.
  - **Reporting Agent**: Compiles data into tables and a final report structure.
  - **Chart Generation Agent**: Creates visualizations and charts, with sandboxed code execution enabled for secure operations.

- **Tasks**: Each agent performs a task as part of the report generation pipeline:
  - **Suggestion Generation**: Provides recommendations based on support ticket trends.
  - **Table Generation**: Summarizes data into a structured table format.
  - **Chart Generation**: Creates visualizations to support data insights.
  - **Final Report Assembly**: Integrates suggestions, tables, and charts into a cohesive report.

## Usage Overview

1. **Define Agents and Tasks**
   - Configures CrewAI agents and tasks for suggestion generation, table and chart creation, and report assembly.
2. **Run Report Generation Workflow**
   - Execute the workflow to generate suggestions, tables, and charts from the support ticket data.
3. **Display Results**
   - Outputs the final report in markdown format, complete with suggestions, structured tables, and visualizations.

### Example Code

```python
# Run the Crew
result = support_report_crew.kickoff()

# Display Results
from IPython.display import display, Markdown
display(Markdown(result.raw))
```

