
# L3: Automated Lead Qualification and Email Engagement

This experiment automates the lead qualification and email engagement process through a coordinated flow of specialized agents. Each agent in CrewAI is assigned a unique role to ensure effective scoring, engagement, and communication with potential leads.

## Key Components

- **Agents**: The workflow includes multiple agents responsible for scoring and email engagement:
  - **Lead Data Agent**: Gathers lead data, including personal and professional information.
  - **Cultural Fit Agent**: Assesses how well the lead's profile fits culturally with the company's values.
  - **Scoring Validation Agent**: Assigns and validates scores to prioritize high-value leads.
  - **Email Content Specialist**: Crafts personalized emails for leads.
  - **Engagement Strategist**: Optimizes email drafts for higher engagement.

- **Tasks**: The agents are assigned focused tasks for efficient lead engagement:
  - **Lead Data Collection**: Collects detailed information about each lead, including company details.
  - **Cultural Fit Analysis**: Analyzes the lead's cultural fit with the company.
  - **Lead Scoring and Validation**: Scores each lead and validates the scoring process.
  - **Email Drafting**: Crafts emails that are personalized to the lead's needs.
  - **Engagement Optimization**: Refines the email drafts to maximize response rates.

## Flow Overview

The sales pipeline consists of several steps, orchestrated in a flow using CrewAI's `Flow` class:
1. **Fetch Leads**: Pulls leads from the database.
2. **Score Leads**: Uses agents to score the lead data based on predefined criteria.
3. **Store Lead Scores**: Stores the calculated scores for each lead.
4. **Filter Leads**: Selects high-scoring leads for further engagement.
5. **Email Writing and Engagement**: Crafts and sends personalized emails to the high-value leads.

### Example Code

```python
# Instantiate and execute the Flow
flow = SalesPipeline()
emails = await flow.kickoff()

# Display the Lead Scoring Results
import pandas as pd
lead_scoring_result = flow.state["score_crews_results"][0].pydantic

# Convert result to DataFrame for display
data = {
    'Name': lead_scoring_result.personal_info.name,
    'Job Title': lead_scoring_result.personal_info.job_title,
    'Company Name': lead_scoring_result.company_info.company_name,
    'Lead Score': lead_scoring_result.lead_score.score,
}
df = pd.DataFrame.from_dict(data, orient='index', columns=['Value'])
display(df)

# Calculate total costs
costs = 0.150 * flow.state["score_crews_results"][0].token_usage.total_tokens / 1_000_000
print(f"Total costs: ${costs:.4f}")
```
