
# Automated Event Planning and Management

This project automates the planning and management of events by coordinating three specialized agents: a Venue Coordinator, Logistics Manager, and Marketing and Communications Agent. Using CrewAI, each agent carries out key responsibilities to ensure seamless event execution.

## Key Components

- **Agents**: Three agents handle event-specific tasks:
  - **Venue Coordinator**: Identifies and books venues based on event needs and budget.
  - **Logistics Manager**: Arranges all logistical requirements, including catering and equipment.
  - **Marketing and Communications Agent**: Promotes the event to engage potential attendees.

- **Tasks**: Each agent is assigned focused tasks:
  - **Venue Selection**: Finds a venue meeting criteria, outputs details in JSON format.
  - **Logistics Arrangement**: Confirms catering and equipment for participant capacity.
  - **Event Promotion**: Markets the event, outputs a markdown report on activities.

## Usage Overview

1. **Define Agents and Tasks**
   - Configures CrewAI agents and tasks for venue selection, logistics, and marketing.
2. **Run Event Planning Workflow**
   - Input event details and execute the crew to generate venue options, logistics confirmations, and a marketing report.
3. **Display Result**
   - Outputs structured details for venue booking, logistics, and marketing engagement.

### Example Code

```python
# Define event inputs
event_details = {
    'event_topic': "Tech Innovation Conference",
    'event_city': "San Francisco",
    'tentative_date': "2024-09-15",
    'expected_participants': 500,
    'budget': 20000
}

# Run Crew
result = event_management_crew.kickoff(inputs=event_details)

# Display Results
import json
with open('venue_details.json') as f:
    data = json.load(f)

from IPython.display import Markdown
Markdown("marketing_report.md")
```

