# OpenAI Agents SDK – MCP Demo

This project demonstrates how to build and manage AI agents using a Model Context Protocol (MCP) approach. It includes examples of single agents, multi-agent coordination, session handling, tool usage, and guardrails.

## Project Structure

```
OpenAI_Agents_SDK/
│
├── MCP_Server/
│   ├── .env
│   ├── Custom_MCP_Server.py
│   ├── MCP_Client.py
│   ├── Multi_MCP_Client.py
│
├── .env
├── .gitattributes
├── Context.py
├── Demo_Function_Tool.py
├── Demo.py
├── Guardrail.py
├── Multi_Agents_Manager.py
├── Multi_gent_Handoff.py
├── Multi_Sessions.py
├── Session_Demo.py
├── Single_Agent.py
├── Tools_Demo.py
├── README.md
```

## Overview

This repository is focused on:

* Building AI agents with structured context
* Connecting to MCP servers and clients
* Managing multiple agents and sessions
* Implementing guardrails and tool integrations
* Demonstrating agent-to-agent handoffs

## Key Components

### MCP Layer

* **Custom_MCP_Server.py**
  Implements a custom MCP server for handling requests.

* **MCP_Client.py**
  Basic client for interacting with a single MCP server.

* **Multi_MCP_Client.py**
  Handles communication with multiple MCP servers.

### Agent System

* **Single_Agent.py**
  Basic example of a single agent workflow.

* **Multi_Agents_Manager.py**
  Coordinates multiple agents.

* **Multi_gent_Handoff.py**
  Demonstrates agent-to-agent task delegation.

### Sessions

* **Session_Demo.py**
  Example of session lifecycle.

* **Multi_Sessions.py**
  Managing multiple concurrent sessions.

### Tools & Functions

* **Tools_Demo.py**
  Demonstrates tool usage inside agents.

* **Demo_Function_Tool.py**
  Custom function tools for agent execution.

### Context & Control

* **Context.py**
  Handles structured context for agents.

* **Guardrail.py**
  Defines safety and constraint logic.

### Entry Point

* **Demo.py**
  Main script to test core functionality.

## Setup

1. Clone the repository:

```bash
git clone the repo
cd OpenAI_Agents_SDK
```

2. Create environment file:

```bash
cp .env.example .env
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Add your API keys to `.env`

## Usage

Run basic demo:

```bash
python Demo.py
```

Run single agent:

```bash
python Single_Agent.py
```

Run multi-agent system:

```bash
python Multi_Agents_Manager.py
```

Run MCP client:

```bash
python MCP_Server/MCP_Client.py
```

## Notes

* Keep `.env` files out of version control
* Ensure API keys are properly configured
* Scripts are modular and can be combined as needed