# LangGraph Agent Examples

This repository contains practical examples of building AI agents using **LangGraph**.

The project demonstrates different agent architectures, from a simple single agent to multi-agent systems with tools and a Retrieval-Augmented Generation (RAG) pipeline.

---

# Project Structure

```
LangGraph/
│
├── langgraph_single_agent.py
├── langgraph_single_agent_single_tool.ipynb
├── langgraph_single_agent_multi_tools.ipynb
├── langgraph_multi_agents_multi_tools.ipynb
├── langgraph_RAG.ipynb
└── README.md
```

---

# Examples

## 1. Single Agent

**File:** `langgraph_single_agent.py`

A minimal LangGraph chatbot demonstrating the basic workflow of a single AI agent.

### Features

- Basic LangGraph workflow
- Terminal-based interaction
- Simple agent loop

### Run

```bash
python langgraph_single_agent.py
```

---

## 2. Single Agent + Single Tool

**File:** `langgraph_single_agent_single_tool.ipynb`

This example shows how a LangGraph agent can use a **Wikipedia tool** to retrieve external knowledge.

### Features

- Tool calling
- Integration with Wikipedia
- LangGraph tool nodes

---

## 3. Single Agent + Multiple Tools

**File:** `langgraph_single_agent_multi_tools.ipynb`

This notebook demonstrates how an agent can choose between multiple tools depending on the task.

### Tools Included

- DuckDuckGo Search
- Addition Tool
- Multiplication Tool

### Features

- Multiple tool usage
- Conditional routing
- Tool selection logic

---

## 4. Multi-Agent System + Multiple Tools

**File:** `langgraph_multi_agents_multi_tools.ipynb`

A supervisor-based **multi-agent architecture** where specialized agents collaborate to complete tasks.

### Agents

- **Research Agent** – handles search-related tasks
- **Math Agent** – handles mathematical calculations

### Features

- Agent collaboration
- Supervisor routing
- Task delegation

---

## 5. Retrieval Augmented Generation (RAG)

**File:** `langgraph_RAG.ipynb`

This notebook demonstrates how to build a **RAG pipeline using LangGraph**.

### Features

- Document loading
- Text chunking
- Vector embeddings
- Vector database retrieval
- LLM response generation

---

# Installation

Install the required dependencies:

```bash
pip install langgraph
pip install langchain
pip install langchain-community
pip install langchain-openai
pip install duckduckgo-search
pip install wikipedia
pip install chromadb
pip install transformers
pip install torch
```

Or install everything at once:

```bash
pip install langgraph langchain langchain-community langchain-openai duckduckgo-search wikipedia chromadb transformers torch
```

---

# Setup API Key

Set your OpenAI API key before running the agents.

### Linux / Mac

```bash
export OPENAI_API_KEY="your_api_key"
```

### Windows

```bash
set OPENAI_API_KEY=your_api_key
```

---

# How to Run

### Run Python Agent

```bash
python langgraph_single_agent.py
```

### Run Notebooks

Open the `.ipynb` files in:

- Jupyter Notebook
- JupyterLab
- VS Code

Then execute the cells sequentially.

---

# Recommended Learning Path

To understand LangGraph step by step, follow this order:

1. `langgraph_single_agent.py`
2. `langgraph_single_agent_single_tool.ipynb`
3. `langgraph_single_agent_multi_tools.ipynb`
4. `langgraph_multi_agents_multi_tools.ipynb`
5. `langgraph_RAG.ipynb`

---

# Concepts Covered

This project demonstrates several important concepts:

- LangGraph workflows
- Nodes and edges
- Tool calling
- Conditional routing
- Multi-agent systems
- Supervisor architecture
- Retrieval-Augmented Generation (RAG)

---

# Notes

- Do not store API keys directly in code.
- Some tools require internet access.
- Make sure all dependencies are installed before running notebooks.

---

# Purpose of This Repository

This repository is designed for learning **LangGraph agent architectures**, starting from simple chatbot agents and progressing toward advanced multi-agent systems and RAG pipelines.
