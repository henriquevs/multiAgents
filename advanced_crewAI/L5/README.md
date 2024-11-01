
# L5: Automated Content Creation at Scale

This project automates large-scale content creation using CrewAI agents that handle monitoring, data analysis, content generation, and quality assurance. The output includes a structured article and social media posts related to a specified topic.

## Key Components

- **Agents**: Four agents manage the end-to-end content creation pipeline:
  - **Market News Monitor Agent**: Tracks financial news and trends relevant to the topic.
  - **Data Analyst Agent**: Analyzes financial and market data to provide insights for content creation.
  - **Content Creator Agent**: Drafts the main article and related social media posts.
  - **Quality Assurance Agent**: Reviews content for accuracy and quality.

- **Tasks**: The agents perform tasks to produce structured content:
  - **News Monitoring**: Tracks market news for relevant information.
  - **Data Analysis**: Gathers and analyzes data for insightful content.
  - **Content Creation**: Drafts the article and social media posts.
  - **Quality Assurance**: Ensures content meets quality standards before final output.

## Usage Overview

1. **Define Agents and Tasks**
   - Configures CrewAI agents and tasks for news monitoring, data analysis, content drafting, and quality checks.
2. **Run Content Creation Workflow**
   - Executes the workflow to produce a structured article and social media posts.
3. **Display Results**
   - Outputs the final article and related social media content in markdown format.

### Example Code

```python
# Run the Crew with a specified subject
result = content_creation_crew.kickoff(inputs={
  'subject': 'Inflation in the US and the impact on the stock market in 2024'
})

# Display Social Media Content
import textwrap
posts = result.pydantic.dict()['social_media_posts']
for post in posts:
    platform = post['platform']
    content = post['content']
    print(platform)
    print(textwrap.fill(content, width=50))
    print('-' * 50)

# Display Article
from IPython.display import display, Markdown
display(Markdown(result.pydantic.dict()['article']))
```

