# Agentic AI

This repository contains experiments and implementations of different **AI agent architectures** built using Python and modern LLM frameworks.

Each agent implementation lives in its own folder with a dedicated README explaining how it works and how to run it.

---

# Projects

## Goal Based Agent

An interactive agent that gathers required information from the user and works step-by-step toward completing a defined objective.

## Reflex Agent

A simple rule-based agent that immediately responds to inputs using predefined conditions without reasoning or planning.

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

## Agentic RAG System

An advanced **Retrieval-Augmented Generation (RAG)** system with agent-based decision making.

This implementation combines:

* **LLM reasoning + dynamic retrieval**
* **PostgreSQL + pgvector for vector search**
* **external knowledge sources (e.g., Arxiv)**

The agent decides when to retrieve information, fetches relevant context, and generates grounded responses — demonstrating a more **reliable and scalable alternative to standalone LLMs**.

---

# Agno Agents

This repository also includes examples of building AI agents using the **Agno framework**.
These projects demonstrate simple agent creation, tool usage, and memory-enabled workflows powered by OpenAI models.

* **Simple Multimodal Agent** – a minimal Agno agent that loads an API key and answers user queries
* **Agents with Tools and Memory** – demonstrates agents capable of using external tools and maintaining context

---

# CrewAI Projects

This repository also contains **CrewAI based multi-agent systems** for real-world automation tasks.

## News Summarization

A multi-agent workflow that researches recent **AI industry news** and generates a summarized report or blog-style output.

Location:

```
CrewAI/News_Summarization/new_summarization.ipynb
```

---

## AI Trip Planner

A multi-agent travel planning system that generates personalized travel itineraries based on user preferences.

The system uses three specialized agents:

* **Location Expert** – researches logistics such as transport, weather, and accommodation
* **Guide Expert** – recommends attractions, food, and experiences
* **Planner Expert** – combines the information into a complete travel itinerary

It can run in two ways:

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

A LangGraph-based agent that connects to multiple **MCP servers** (Weather + Calculator) and dynamically selects tools based on user queries.

Demonstrates:

* Tool orchestration across multiple MCP servers
* Real-time API interaction (weather data)
* Hybrid reasoning + tool execution workflow

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
* Ollama / LLM APIs

---

# Purpose

These projects demonstrate how **AI agents and multi-agent systems** can automate complex workflows such as:

* research
* summarization
* itinerary planning
* information synthesis
