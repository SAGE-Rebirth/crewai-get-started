
# Crewai Quickstart Guide

Welcome to the Crewai project! This guide will help you set up and run your first AI crew using Crewai.

## Prerequisites

- **Python**: Ensure you have Python installed (version >=3.10 and <3.13). Check your version with:

  ```bash
  python3 --version
  ```

  If you need to update Python, download the latest version from the [official website](https://www.python.org/downloads/).

## Installation

1. **Install Crewai**: Use `pip` to install Crewai along with the recommended tools:

   ```bash
   pip install 'crewai[tools]'
   ```

   Alternatively, you can install the core package and tools separately:

   ```bash
   pip install crewai crewai-tools
   ```

2. **Upgrade Crewai** (if updating from an older version):

   ```bash
   pip install --upgrade crewai crewai-tools
   ```

   If you encounter a Poetry-related warning, migrate to the new dependency manager:

   ```bash
   crewai update
   ```

3. **Verify Installation**: Confirm the installation by checking the installed versions:

   ```bash
   pip freeze | grep crewai
   ```

   You should see output similar to:

   ```
   crewai==X.X.X
   crewai-tools==X.X.X
   ```

## Creating a New Project

1. **Generate Project Structure**: Use the Crewai CLI to create a new project:

   ```bash
   crewai create crew <project_name>
   ```

   Replace `<project_name>` with your desired project name. This command creates a directory with the following structure:

   ```
   <project_name>/
   ├── .gitignore
   ├── pyproject.toml
   ├── README.md
   ├── .env
   └── src/
       └── <project_name>/
           ├── __init__.py
           ├── main.py
           ├── crew.py
           ├── tools/
           │   ├── custom_tool.py
           │   └── __init__.py
           └── config/
               ├── agents.yaml
               └── tasks.yaml
   ```

2. **Customize Your Project**:

   - `agents.yaml`: Define your AI agents and their roles.
   - `tasks.yaml`: Set up agent tasks and workflows.
   - `.env`: Store API keys and environment variables.
   - `main.py`: Entry point for project execution.
   - `crew.py`: Handles crew orchestration and coordination.
   - `tools/`: Directory for custom agent tools.

   Begin by editing `agents.yaml` and `tasks.yaml` to define your crew’s behavior. Store sensitive information like API keys in `.env`.

## Running Your First Crew

1. **Navigate to the Project Directory**:

   ```bash
   cd <project_name>
   ```

2. **Execute the Main Script**:

   ```bash
   python src/<project_name>/main.py
   ```

   This command initiates your crew based on the configurations in `agents.yaml` and `tasks.yaml`.

## Next Steps

- **Build Your First Agent**: Follow the [quickstart guide](https://docs.crewai.com/quickstart) to create your first Crewai agent and gain hands-on experience.

- **Join the Community**: Connect with other developers, seek assistance, and share your Crewai experiences on the [Crewai Community Forum](https://community.crewai.com).

For more detailed information, refer to the [official Crewai documentation](https://docs.crewai.com/installation).

Happy crewing! 🚀
