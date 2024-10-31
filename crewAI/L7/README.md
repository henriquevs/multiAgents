
# Automated Job Application Preparation

This project automates the preparation for job applications by coordinating specialized agents to research job requirements, tailor resumes, and prepare interview materials. Each agent in CrewAI focuses on a distinct task, ensuring comprehensive and personalized application support.

## Key Components

- **Agents**: Four agents manage the job application process:
  - **Tech Job Researcher**: Analyzes job postings to extract required skills and qualifications.
  - **Personal Profiler**: Builds a detailed profile of the candidate using provided URLs and resume content.
  - **Resume Strategist**: Customizes the candidate’s resume to match job requirements.
  - **Interview Preparer**: Develops interview questions and talking points to prepare the candidate.

- **Tasks**: Each agent performs specific tasks for application preparation:
  - **Job Requirements Extraction**: Analyzes job listings to identify necessary skills and qualifications.
  - **Candidate Profiling**: Creates a candidate profile based on public and personal information.
  - **Resume Customization**: Adjusts the resume to align with job requirements, outputting a tailored document.
  - **Interview Preparation**: Generates questions and talking points for interview readiness.

## Usage Overview

1. **Define Agents and Tasks**
   - Configures CrewAI agents and tasks for job research, profiling, resume alignment, and interview preparation.
2. **Run Application Preparation Workflow**
   - Input job listing and candidate details, then execute the crew to generate a tailored resume and interview materials.
3. **Display Result**
   - Outputs a customized resume and structured interview materials to support job application.

### Example Code

```python
# Define job application inputs
job_application_inputs = {
    'job_posting_url': 'https://jobs.lever.co/AIFund/6c82e23e-d954-4dd8-a734-c0c2c5ee00f1?lever-origin=applied&lever-source%5B%5D=AI+Fund',
    'github_url': 'https://github.com/joaomdmoura',
    'personal_writeup': "Noah is an accomplished Software Engineering Leader..."
}

# Run Crew
result = job_application_crew.kickoff(inputs=job_application_inputs)

# Display Results
from IPython.display import Markdown
display(Markdown("./tailored_resume.md"))
display(Markdown("./interview_materials.md"))
```

