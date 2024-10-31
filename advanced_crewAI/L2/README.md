
# L1: Automated Project Planning, Estimation, and Allocation

This project automates the initial stages of project management by planning tasks, estimating time and resources, and allocating agents accordingly. Using CrewAI, this notebook defines agents and tasks to generate structured project plans, including task breakdowns and milestones.

## Key Components

- **Agents & Tasks**: CrewAI agents are configured for project planning, estimation, and allocation based on YAML configurations.
- **Structured Output**: Pydantic models are used to structure the output, including task estimates and milestones.
- **Cost Tracking**: Calculates API usage cost based on token consumption.

## Usage Overview

1. **Set Up CrewAI Agents and Tasks**
   - Loads configurations for agents (planning, estimation, allocation).
2. **Run CrewAI Execution**
   - Defines project inputs and runs the crew, creating a structured project plan.
3. **Output Structured Results**
   - Displays task estimates, milestones, and cost metrics.

### Example Code

```python
# Define project inputs
inputs = {
    'project_type': 'Website',
    'project_objectives': 'Create a website for a small business',
    'industry': 'Technology',
    'team_members': "John Doe, Jane Doe, Bob Smith, Alice Johnson, Tom Brown",
    'project_requirements': "Responsive design, modern UI, SEO optimization, etc."
}

# Run Crew
result = crew.kickoff(inputs=inputs)

# Display Results
print(result.pydantic.dict())
```

