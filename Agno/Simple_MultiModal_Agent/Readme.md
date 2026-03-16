# Simple Multimodal Agent (Agno)

This project demonstrates a **basic AI agent built using the Agno framework and OpenAI models**.
The agent loads an API key from an environment file and answers user questions using a chat model.

It is a minimal example designed to show how to:

* Configure API keys
* Initialize an AI agent
* Connect the agent to an OpenAI model
* Generate responses from prompts

---

## Project Structure

```
.
├── simple_agent.py
├── env.txt
└── README.md
```

**simple_agent.py**
Main script that creates and runs the Agno agent.

**env.txt**
Contains environment variables such as the OpenAI API key.

**README.md**
Project documentation.

---

## Requirements

* Python 3.9+
* Agno
* python-dotenv

Install dependencies:

```bash
pip install -U agno
pip install python-dotenv
```

---

## Environment Setup

Create an environment variable file.

Example:

```
OPENAI_API_KEY=your_openai_api_key
```

The provided environment file contains the API key variable:

`OPENAI_API_KEY` 

The script loads this variable using `python-dotenv`.

---

## How the Agent Works

The script:

1. Loads environment variables
2. Retrieves the OpenAI API key
3. Initializes an Agno agent
4. Connects the agent to an OpenAI chat model
5. Sends a prompt to the agent and prints the response

Key implementation example:

```python
from dotenv import load_dotenv
import os

load_dotenv()
api_key = os.getenv("OPENAI_API_KEY")
os.environ["OPENAI_API_KEY"] = api_key
```

The agent is created with:

```python
from agno.agent import Agent
from agno.models.openai import OpenAIChat

agno_agent = Agent(
    model=OpenAIChat(id="gpt-3.5-turbo"),
    description="Agno Q&A agent",
    markdown=False
)
```

The agent responds to prompts like:

```python
agno_agent.print_response("What is the capital of India?", stream=True)
```

This example demonstrates how an agent can generate answers using an OpenAI model. 

---

## Running the Project

Run the Python script:

```bash
python simple_agent.py
```

Expected output:

```
The capital of India is New Delhi.
```

---

## What You Learn

This project helps you understand:

* Basic AI agent setup using Agno
* Connecting OpenAI models to agents
* Handling API keys securely
* Running a simple question-answering agent