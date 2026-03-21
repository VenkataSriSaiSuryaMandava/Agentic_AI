# MCP Math Server & Client

## Overview

This project demonstrates how to build and use a custom MCP (Model Context Protocol) server with Python.

It includes:

* A math MCP server with basic operations
* A single MCP client
* A multi-server MCP client (math + Wikipedia)

---

## Project Structure

```
MCP_Server/
│── .env
│── Custom_MCP_Server.py
│── MCP_Client.py
│── Multi_MCP_Client.py
│── Readme.md
```

---

## Features

### Math MCP Server

Provides the following tools:

* Addition
* Multiplication
* Division
* Square root
* Factorial

Defined in:


---

### MCP Client

* Connects to the math server
* Sends a query
* Prints the response

Defined in:


---

### Multi MCP Client

* Connects to:

  * Math MCP server
  * Wikipedia MCP server
* Handles both calculation and general knowledge queries

Defined in:


---

## Setup

### 1. Install Dependencies

```bash
pip install openai python-dotenv
```

---

### 2. Configure Environment

Create a `.env` file:

```
OPENAI_API_KEY=your_api_key_here
```

---

## Usage

### Run the MCP Server

```bash
python Custom_MCP_Server.py
```

---

### Run Single Client

```bash
python MCP_Client.py
```

Example output:

```
Agent reply: 12
```

---

### Run Multi Client

```bash
python Multi_MCP_Client.py
```

Example output:

```
Math result: 120
Wiki result: Isaac Newton discovered gravity.
Mixed result: 100 and Taj Mahal is a famous monument in India.
```

---

## How It Works

* The MCP server exposes tools (math functions)
* The agent connects to the server via stdio
* The agent decides when to call tools based on the query
* Results are returned and displayed

---

## Notes

* The server runs locally using Python
* Clients communicate using MCP over stdio
* The agent automatically selects the right tool