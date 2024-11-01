
# Automated Lead Generation and Personalized Outreach

This project automates the lead generation and personalized outreach process by coordinating two main agents in CrewAI. The Sales Representative identifies high-value leads, while the Lead Sales Representative crafts personalized outreach strategies to engage decision-makers.

## Key Components

- **Agents**: Two agents focus on distinct tasks to drive lead engagement:
  - **Sales Representative**: Gathers detailed insights on potential leads using multiple data sources.
  - **Lead Sales Representative**: Develops personalized outreach materials that connect our solutions to the lead's needs.

- **Tasks**: The agents are assigned tasks as follows:
  - **Lead Profiling**: Analyzes a lead's background, key personnel, milestones, and potential needs.
  - **Personalized Outreach**: Crafts targeted messages for decision-makers, tailored to their company’s recent achievements.

## Usage Overview

1. **Define Agents and Tasks**
   - Configures CrewAI agents and tasks for lead profiling and outreach strategy development.
2. **Run Lead Engagement Process**
   - Input lead details and execute the crew to generate a complete lead profile and personalized campaign.
3. **Display Result**
   - Outputs structured insights and outreach drafts for engaging high-value leads.

### Example Code

```python
# Define lead inputs
inputs = {
    "lead_name": "DeepLearningAI",
    "industry": "Online Learning Platform",
    "key_decision_maker": "Andrew Ng",
    "position": "CEO",
    "milestone": "product launch"
}

# Run Crew
result = crew.kickoff(inputs=inputs)

# Display Result
from IPython.display import Markdown
Markdown(result)
```

