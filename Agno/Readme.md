# Agno Agents Examples

This repository contains simple examples of building AI agents using the **Agno framework** and **OpenAI models**.
The projects demonstrate how agents can answer questions, use tools, and manage memory.

## Projects

### 1. Agents with Tools and Memory

Shows how to build an AI agent that can:

* Use external tools
* Handle tasks dynamically
* Work with additional capabilities beyond simple Q&A

**Files**

* `agno_agent_tools_memory.ipynb` – Notebook demonstrating agent setup and tool usage
* `env.txt` – Environment variables (API key)

---

### 2. Simple Multimodal Agent

A minimal example of creating an Agno agent using a Python script.

**Files**

* `simple_agent.py` – Basic agent that answers questions using an OpenAI model
* `env.txt` – Environment variables (API key)

---

## Requirements

* Python 3.9+
* agno
* python-dotenv

Install dependencies:

```bash
pip install -U agno
pip install python-dotenv
```

---

## Setup

Create an environment file and add your OpenAI API key:

```
OPENAI_API_KEY=your_api_key_here
```

---

## Purpose

This repository is intended for learning how to:

* Build AI agents with **Agno**
* Connect agents to **OpenAI models**
* Extend agents with **tools and additional capabilities**