# Custom MCP Server with LangGraph + Streamlit

Build and connect a custom **MCP (Model Context Protocol) server** with **LangGraph** to enable LLM-powered math tool execution. Includes both a CLI client and a Streamlit web interface.

---

## 🚀 Features

* Custom MCP server exposing math tools:

  * Addition
  * Multiplication
  * Division
  * Square root
  * Factorial
* LangGraph-powered tool orchestration
* Automatic tool calling via LLM
* CLI-based interaction
* Streamlit web UI

---

## 📁 Project Structure

```
.
├── custom_mcp_server.py      # MCP server exposing math tools
├── mcp_client_langgraph.py   # LangGraph client (CLI)
├── web_app.py                # Streamlit UI
├── env.txt                   # Environment variables
├── README.md
```

---

## 🛠️ Installation

Install dependencies:

```bash
pip install python-dotenv langchain-mcp-adapters langgraph "langchain[openai]" mcp streamlit
```

---

## 🔑 Environment Setup

Create a `.env` file in the root directory:

```
OPENAI_API_KEY=your_api_key_here
```

---

## ▶️ Running the Project

### 1. Start MCP Server

```bash
python custom_mcp_server.py
```

The server will run at:

```
http://127.0.0.1:8000/mcp
```

---

### 2. Run CLI Client

```bash
python mcp_client_langgraph.py
```

Example query:

```
what's (3 + 5) x 12?
```

---

### 3. Run Streamlit App

```bash
streamlit run web_app.py
```

This opens a browser-based UI for interacting with the MCP-powered assistant.

---

## ⚙️ How It Works

### MCP Server

The server is built using `FastMCP` and exposes math functions as tools:

* `add(a, b)`
* `multiply(a, b)`
* `divide(a, b)`
* `square_root(x)`
* `factorial(n)`

---

### LangGraph Client

* Fetches tools from MCP server
* Binds tools to the language model
* Uses a graph-based execution flow:

  * Model decides when to call tools
  * Tool results are fed back into the model
  * Final response is generated

---

### Execution Flow

```
START → Model → Tool (if needed) → Model → END
```

---

## 🧪 Example

**Input:**

```
what's (3 + 5) x 12?
```

**Output:**

```
96
```

---

## 🧠 Tech Stack

* MCP (Model Context Protocol)
* LangGraph
* LangChain
* OpenAI
* Streamlit

---

## 📌 Summary

This project demonstrates how to:

* Build a custom MCP server
* Expose tools to an LLM
* Orchestrate tool usage with LangGraph
* Create both CLI and web-based interfaces