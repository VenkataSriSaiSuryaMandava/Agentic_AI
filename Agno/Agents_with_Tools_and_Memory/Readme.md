# Agents with Tools and Memory (Agno)

This project demonstrates how to build **AI agents using the Agno framework** with tool usage and environment configuration. The notebook shows how an agent can interact with external tools such as search, Python execution, and custom functions.

The goal is to understand how **agentic AI systems** work when they are able to call tools and respond dynamically.

---

## Project Structure

```
.
├── agno_agent_tools_memory.ipynb
├── env.txt
└── README.md
```

* **agno_agent_tools_memory.ipynb** – Main notebook demonstrating agent creation, tool integration, and responses.
* **env.txt** – Stores environment variables such as API keys.
* **README.md** – Project documentation.

---

## Requirements

Python 3.9+

Main libraries used:

* agno
* python-dotenv
* googlesearch-python
* pycountry

Install dependencies:

```bash
pip install -U agno
pip install python-dotenv
pip install googlesearch-python pycountry
```

---

## Environment Setup

Create an `.env` file or use the provided environment configuration.

Example:

```
OPENAI_API_KEY=your_openai_api_key
```

The project loads the API key from the environment file. The uploaded configuration file includes this variable:

`OPENAI_API_KEY` 

Load it in Python:

```python
from dotenv import load_dotenv
import os

load_dotenv()
api_key = os.getenv("OPENAI_API_KEY")
```

---

## Creating a Basic Agent

Example agent using OpenAI through Agno:

```python
from agno.agent import Agent
from agno.models.openai import OpenAIChat

agent = Agent(
    model=OpenAIChat(id="gpt-4o"),
    description="You’re a cheerful AI pal who loves a good chat!",
    markdown=True
)

agent.print_response("Summarize the story of The Lion King.", stream=True)
```

---

## Using Tools with an Agent

Agents can use external tools to perform tasks such as search or computation.

### Google Search Tool

```python
from agno.tools.googlesearch import GoogleSearchTools

agent = Agent(
    model=OpenAIChat(id="gpt-4o-mini"),
    tools=[GoogleSearchTools()]
)

agent.print_response("What are the trending AI tools in 2025?", stream=True)
```

---

### Python Tool

Allows the agent to execute Python code.

```python
from agno.tools.python import PythonTools
from agno.agent import Agent

agent = Agent(
    tools=[PythonTools()],
    show_tool_calls=True
)

agent.print_response("Write a function to reverse a string without using slicing")
```

---

### Custom Tool Example

You can create your own tool functions.

```python
from datetime import datetime

def get_today_date():
    return datetime.now().strftime("Today is %B %d, %Y")
```

Attach it to the agent:

```python
agent = Agent(
    tools=[get_today_date],
    show_tool_calls=True,
    markdown=True
)

agent.print_response("What is today’s date?", stream=True)
```

---

## Key Concepts Demonstrated

* Creating agents using **Agno**
* Connecting **OpenAI models**
* Allowing agents to **call tools**
* Integrating **Google search**
* Running **Python code inside agents**
* Creating **custom tools**

---

## Running the Notebook

Open the notebook in:

* **Google Colab**
* **Jupyter Notebook**
* **VS Code**

Then run cells sequentially.

---

## Learning Outcome

After completing this notebook you should understand:

* How agent frameworks work
* How tools extend agent capabilities
* How to build simple agentic workflows