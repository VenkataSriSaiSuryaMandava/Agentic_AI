# LangGraph Agent Examples

Simple examples of building AI agents using **LangGraph**.
This project shows how to build single agents, agents with tools, and multi-agent systems.

---

## Project Structure

```
LangGraph/
│
├── langgraph_single_agent.py
├── langgraph_single_agent_single_tool.ipynb
├── langgraph_single_agent_multi_tools.ipynb
├── langgraph_multi_agents_multi_tools.ipynb
└── README.md
```

---

## Examples

### 1. Single Agent

`langgraph_single_agent.py`

A basic LangGraph chatbot.

Features:

* simple LangGraph workflow
* terminal interaction
* basic agent structure

Run:

```
python langgraph_single_agent.py
```

---

### 2. Single Agent + Single Tool

`langgraph_single_agent_single_tool.ipynb`

Agent that can use **Wikipedia**.

Features:

* tool calling
* LangGraph tool node
* LLM + external knowledge

---

### 3. Single Agent + Multiple Tools

`langgraph_single_agent_multi_tools.ipynb`

Agent with multiple tools.

Tools:

* DuckDuckGo Search
* Addition Tool
* Multiplication Tool

Features:

* multi-tool usage
* conditional routing
* tool selection

---

### 4. Multi-Agent + Multiple Tools

`langgraph_multi_agents_multi_tools.ipynb`

Supervisor-based **multi-agent system**.

Agents:

* Research Agent (search tasks)
* Math Agent (calculation tasks)

Features:

* agent collaboration
* supervisor routing
* task delegation

---

## Installation

Install dependencies:

```
pip install langgraph langchain langchain-community
pip install langchain-openai
pip install duckduckgo-search
pip install wikipedia
pip install langgraph-supervisor
```

---

## Setup API Key

Set your OpenAI API key.

Linux / Mac:

```
export OPENAI_API_KEY="your_api_key"
```

Windows:

```
set OPENAI_API_KEY=your_api_key
```

---

## How to Run

Run Python agent:

```
python langgraph_single_agent.py
```

Run notebooks:

Open the `.ipynb` files in **Jupyter Notebook** or **VS Code** and run the cells.

---

## Learning Path

Recommended order:

1. `langgraph_single_agent.py`
2. `langgraph_single_agent_single_tool.ipynb`
3. `langgraph_single_agent_multi_tools.ipynb`
4. `langgraph_multi_agents_multi_tools.ipynb`

---

## Concepts Covered

* LangGraph workflows
* Nodes and edges
* Tool calling
* Conditional routing
* Multi-agent systems
* Supervisor architecture

---

## Notes

* Do not store API keys directly in code.
* Some tools require internet access.
* Install all dependencies before running notebooks.
