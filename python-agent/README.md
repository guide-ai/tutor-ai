# Python Agent

This project is a Python-based agent designed to provide educational assistance for various school subjects.

## Overview

The Python Agent is responsible for handling the backend logic of our mobile learning application. It leverages various libraries (managed by Poetry) such as `langgraph`, `langchain-core`, `langchain-community`, `langchain-openai`, and `trustcall` to perform its tasks. Additionally, `langgraph-cli` is included as a development dependency for extended tooling.

## Setup Instructions

1. **Configure Virtual Environment Location**

   First, configure Poetry to create the virtual environment within your project directory:

   ```bash
   poetry config virtualenvs.in-project true
   ```

2. **Install Dependencies**

   Install project dependencies (this will automatically create the `.venv` directory):

   ```bash
   poetry install
   ```

## Running the Agent

Once the dependencies are installed and the virtual environment is active, you can run the agent with the following command:

```bash
python agent/main.py
```

This will execute the main script located at `agent/main.py`, which contains example functionality.

## Development

- **Development Dependency:** The project includes `langgraph-cli` as a development dependency to support additional tooling during development.
- **Modifying the Code:** The main logic of the agent is found in the `agent` directory. Feel free to modify or extend the functionality to suit your project needs.

## Self-Hosted Deployment

### Prerequisites
- Docker and Docker Compose installed
- Valid API keys for LangSmith and OpenAI

### Deployment Steps

1. **Build the Docker Image**
   ```bash
   langgraph build -t python-agent-image
   ```

2. **Configure Environment**
   Create `.env` file with:
   ```env
   LANGSMITH_API_KEY=your_key
   OPENAI_API_KEY=your_key
   TAVILY_API_KEY=your_key
   LANGCHAIN_TRACING_V2=true
   ```

3. **Run the Container**
   ```bash
   docker compose up -d
   ```

4. **Once running, we can access the deployment through**
      
* API: http://localhost:8123
* Docs: http://localhost:8123/docs
* LangGraph Studio: https://smith.langchain.com/studio/?baseUrl=http://127.0.0.1:8123

[Full deployment guide](https://langchain-ai.github.io/langgraph/how-tos/deploy-self-hosted)

5. ## Using the API  

LangGraph Server exposes [many API endpoints](https://github.com/langchain-ai/agent-protocol) for interacting with the deployed agent.

We can group [these endpoints into a few common agent needs](https://github.com/langchain-ai/agent-protocol): 

* **Runs**: Atomic agent executions
* **Threads**: Multi-turn interactions or human in the loop
* **Store**: Long-term memory

We can test requests directly [in the API docs](http://localhost:8123/docs#tag/thread-runs).

## Additional Information

- Ensure your Python version satisfies the requirement (>= 3.11 and < 4.0) as specified in the project configuration.
- For issues, enhancements, or contributions, please open an issue or submit a pull request.

Happy coding!
