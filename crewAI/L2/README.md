
# Automated Blog Content Creation: Planning, Writing, and Editing

This project automates blog content creation by orchestrating three main agents: a Content Planner, a Writer, and an Editor. Using CrewAI, each agent performs a role in developing engaging, well-researched blog posts aligned with journalistic standards and SEO requirements.

## Key Components

- **Agents**: Three agents manage distinct stages of content creation:
  - **Content Planner**: Develops a structured content plan for a given topic.
  - **Content Writer**: Drafts a well-organized blog post based on the planner's outline.
  - **Editor**: Proofreads and aligns the blog with brand voice and journalistic best practices.

- **Tasks**: Each agent has specific tasks:
  - **Planning**: Research trends, define target audience, create an outline with SEO keywords.
  - **Writing**: Draft the blog post using the outline, ensuring an engaging format.
  - **Editing**: Finalize the post by editing for grammar and brand alignment.

## Usage Overview

1. **Define Agents and Tasks**
   - Configures CrewAI agents and tasks for planning, writing, and editing.
2. **Run Content Creation Process**
   - Input the topic (e.g., "Artificial Intelligence") and execute the crew, which outputs a structured markdown post.
3. **Display Result**
   - Final content is ready for publication in markdown format.

### Example Code

```python
# Define topic input
inputs = {"topic": "Artificial Intelligence"}

# Run Crew
result = crew.kickoff(inputs=inputs)

# Display Result
from IPython.display import Markdown
Markdown(result)
```

