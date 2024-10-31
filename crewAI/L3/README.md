
# Automated Customer Support and Quality Assurance

This project automates the customer support process by orchestrating a support agent and a quality assurance specialist to provide comprehensive, friendly, and high-quality support responses. The workflow ensures that inquiries are fully addressed with external references as needed.

## Key Components

- **Agents**: Two agents handle the support and review process:
  - **Senior Support Representative**: Responds to the customer inquiry, providing a complete and friendly answer.
  - **Support Quality Assurance Specialist**: Reviews and refines the response for accuracy, comprehensiveness, and alignment with support standards.

- **Tasks**: The agents handle two main tasks:
  - **Inquiry Resolution**: Creates a detailed response to the customer’s inquiry, using external data sources as needed.
  - **Quality Assurance Review**: Checks the response for quality and completeness, ensuring a professional and friendly tone.

## Usage Overview

1. **Define Agents and Tasks**
   - Configures CrewAI agents and tasks for support and quality assurance.
2. **Run Support Workflow**
   - Input customer inquiry details and execute the crew to generate a high-quality response.
3. **Display Result**
   - Final response is reviewed and ready for delivery to the customer.

### Example Code

```python
# Define inquiry inputs
inputs = {
    "customer": "DeepLearningAI",
    "person": "Andrew Ng",
    "inquiry": "I need help with setting up a Crew and adding memory to it. Can you provide guidance?"
}

# Run Crew
result = crew.kickoff(inputs=inputs)

# Display Result
from IPython.display import Markdown
Markdown(result)
```

