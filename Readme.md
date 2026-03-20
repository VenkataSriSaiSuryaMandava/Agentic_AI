# Agentic AI

This repository contains experiments and implementations of different **AI agent architectures** built using Python and modern LLM frameworks.

Each agent implementation lives in its own folder with a dedicated README explaining how it works and how to run it.

---

# Projects

## Goal Based Agent

An interactive agent that gathers required information from the user and works step-by-step toward completing a defined objective.

---

## Reflex Agent

A simple rule-based agent that immediately responds to inputs using predefined conditions without reasoning or planning.

---

## Learning Agent

A reinforcement learning experiment where an agent learns to play a small Snake game using **Q-learning**, improving its behavior through rewards and penalties.

---

## LangGraph Agents

Examples of building LLM-powered agents using **LangGraph**, including:

* single agent workflows
* agents using tools
* agents using multiple tools
* multi-agent systems with supervisor coordination
* retrieval-augmented generation (RAG) pipelines

---

## Custom MCP Server (LangGraph)

A custom **MCP (Model Context Protocol) server** exposing math tools (add, multiply, divide, etc.) and integrated with a LangGraph agent.

Demonstrates:

* Building your own MCP tool server
* Connecting MCP tools to an LLM via LangGraph
* Tool calling through both CLI and Streamlit UI

---

## MCP Server on Cloud

A setup where the MCP server runs as a standalone HTTP service and is accessed remotely by a LangGraph client.

Demonstrates:

* Running MCP server over HTTP (`/mcp` endpoint)
* Remote tool access instead of local execution
* End-to-end tool calling through API-based architecture

---

## MCP Server with Agno

An implementation of MCP servers integrated with the **Agno framework**, showcasing both local and remote MCP usage inside AI agents.

Demonstrates:

* Running MCP servers as tools inside Agno agents
* Using single and multiple MCP servers
* Creating custom MCP servers with math operations
* Combining built-in MCP servers (calculator, Wikipedia) with custom tools
* Connecting to remote MCP servers over HTTP
* Streaming responses using Agno agents

Files included:

* `Single_MCP_Server.py` – basic MCP integration
* `Multiple_MCP_Server.py` – multiple MCP servers
* `Multiple_MCP_Server_Custom.py` – custom + default MCP tools
* `Custom_MCP_Server.py` – custom math MCP server
* `MCP_Server_on_Cloud.py` – remote MCP connection

---

## OpenAI Agents SDK (MCP Demo)

Implementation of AI agents using the **OpenAI Agents SDK** with support for MCP, multi-agent workflows, and structured tool execution.

Demonstrates:

* Building single and multi-agent systems
* Agent-to-agent communication and handoffs
* MCP server and client integration
* Session and context management
* Tool calling using custom function tools
* Applying guardrails for controlled execution

Key files:

* `Single_Agent.py` – basic agent
* `Multi_Agents_Manager.py` – multi-agent coordination
* `Multi_Agent_Handoff.py` – agent handoff
* `Multi_Sessions.py` – session handling
* `Session_Demo.py` – session example
* `Tools_Demo.py` – tool usage
* `Demo_Function_Tool.py` – custom tools
* `Guardrail.py` – safety rules
* `Context.py` – context handling
* `Demo.py` – entry point

MCP components:

```
OpenAI_Agents_SDK/MCP_Demo/
```

* `Custom_MCP_Server.py` – custom MCP server
* `MCP_Client.py` – single server client
* `Multi_MCP_Client.py` – multi-server client

---

## Agentic RAG System

An advanced **Retrieval-Augmented Generation (RAG)** system with agent-based decision making.

This implementation combines:

* **LLM reasoning + dynamic retrieval**
* **PostgreSQL + pgvector for vector search**
* **external knowledge sources (e.g., Arxiv)**

The agent decides when to retrieve information, fetches relevant context, and generates grounded responses — demonstrating a more reliable and scalable alternative to standalone LLMs.

---

# Agno Agents

This repository also includes examples of building AI agents using the **Agno framework**.

These projects demonstrate simple agent creation, tool usage, and memory-enabled workflows powered by OpenAI models.

* **Simple Multimodal Agent** – minimal agent setup
* **Agents with Tools and Memory** – agents with tools and context handling

---

# CrewAI Projects

This repository also contains **CrewAI based multi-agent systems** for real-world automation tasks.

---

## News Summarization

A multi-agent workflow that researches recent **AI industry news** and generates a summarized report.

Location:

```
CrewAI/News_Summarization/new_summarization.ipynb
```

---

## AI Trip Planner

A multi-agent travel planning system that generates personalized travel itineraries.

Agents involved:

* **Location Expert** – transport, weather, stay
* **Guide Expert** – attractions, food, experiences
* **Planner Expert** – builds final itinerary

Run options:

**Notebook**

```
CrewAI/Trip_Planner/trip_planner.ipynb
```

**Streamlit App**

```
streamlit run CrewAI/Trip_Planner/streamlit_trip_advisor_app/my_app_2.py
```

---

## Multi MCP Servers

A LangGraph-based agent that connects to multiple MCP servers (Weather + Calculator) and dynamically selects tools.

Demonstrates:

* Tool orchestration across MCP servers
* Real-time API interaction
* Hybrid reasoning + execution

---

# Technologies

* Python
* NumPy
* Pygame
* LangChain
* LangGraph
* CrewAI
* Agno
* Streamlit
* LLM APIs

---

# Purpose

These projects demonstrate how **AI agents and multi-agent systems** can automate complex workflows such as:

* research
* summarization
* itinerary planning
* information synthesis