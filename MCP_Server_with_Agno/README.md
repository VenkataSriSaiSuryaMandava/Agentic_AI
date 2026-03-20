# MCP Server with Agno

This project shows how to build and use Model Context Protocol (MCP) servers with Agno. It includes examples for single servers, multiple servers, custom tools, and connecting to a cloud MCP server.

---

## Overview

This repo covers:

* Running MCP servers (calculator, Wikipedia)
* Creating your own custom MCP tools
* Connecting MCP servers to an AI agent
* Using multiple MCP servers together
* Connecting to a remote MCP server

---

## Project Structure

* `Single_MCP_Server.py`
  Basic setup using one MCP server

* `Multiple_MCP_Server.py`
  Uses multiple MCP servers together

* `Multiple_MCP_Server_Custom.py`
  Combines default and custom MCP servers

* `Custom_MCP_Server.py`
  Custom MCP server with math tools

* `MCP_Server_on_Cloud.py`
  Connects to a remote MCP server

* `env.txt`
  Example environment file

---

## Installation

```bash
pip install -U agno
pip install python-dotenv
```

---

## Setup

Create a `.env` file:

```env
OPENAI_API_KEY=your_api_key_here
```

---

## Usage

Run any of the following:

```bash
python Single_MCP_Server.py
```

```bash
python Multiple_MCP_Server.py
```

```bash
python Custom_MCP_Server.py
```

```bash
python Multiple_MCP_Server_Custom.py
```

```bash
python MCP_Server_on_Cloud.py
```

---

## Custom MCP Tools

The custom server includes:

* Addition
* Multiplication
* Division
* Square root
* Factorial

---

## Requirements

* Python 3.9+
* agno
* python-dotenv