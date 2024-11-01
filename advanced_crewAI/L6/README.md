
# L6: Building Your Crew for Production

This project demonstrates how to set up a production environment for CrewAI, including creating a new project, configuring the environment, and running the crew with the necessary flows.

## Steps to Build a Production-Ready Crew

1. **Creating a New Project**  
   Use the CrewAI CLI to initialize a new project structure.
   ```bash
   crewai create crew new_project --provider openai
   ```

2. **Setting up the Environment**  
   Change directories to your new project and install dependencies. This step may take a few minutes.
   ```bash
   cd new_project && crewai install
   ```

3. **Configuring Environment Variables**  
   Access and edit environment variables, including API keys and model configuration.
   ```bash
   cat new_project/.env
   ```

4. **Running the Crew**  
   Run your crew to test the initial project setup and verify configurations.
   ```bash
   cd new_project && crewai run
   ```

5. **Using the Flows CLI**  
   The CrewAI CLI can also be used to create flows for automating sequences.
   ```bash
   crewai create flow new_flow
   ls -1 new_flow
   ls -1 new_flow/src/new_flow/
   ```

## Notes

- **Kernel Starting**: Starting the kernel may take 30 seconds; you can begin exploring other setup tasks while waiting.
- **File Access**: Use the "File" menu to access `requirements.txt` and `helper.py` files, if needed.

This setup guide provides all essential steps to initialize, configure, and run a CrewAI project ready for production.
