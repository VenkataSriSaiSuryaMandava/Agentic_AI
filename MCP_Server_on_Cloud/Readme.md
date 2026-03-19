# MCP Math Server + LangGraph Client

A minimal working example of:

* An MCP server exposing math tools
* A LangGraph client that calls those tools via an LLM

---

## 📁 Project Structure

```
MCP_Server_on_Cloud/
├── Custom_MCP_Server.py
├── MCP_Client_LangGraph.py
├── Readme.md
```

---

## ⚙️ Requirements

Install dependencies:

```bash
pip install uvicorn python-dotenv langchain langgraph langchain-openai langchain-mcp-adapters
```

---

## 🔐 Environment Variables

Create a `.env` file in the project root:

```env
OPENAI_API_KEY=your_openai_api_key
```

---

## 🚀 Step 1: Start MCP Server

Run:

```bash
python Custom_MCP_Server.py
```

Server will start at:

```
http://127.0.0.1:8080/mcp
```

### Available Tools

Defined in the server :

* `add(a, b)` → returns sum
* `multiply(a, b)` → returns product

---

## 🤖 Step 2: Run Client

Make sure the client uses the correct server URL:

```python
"url": "http://127.0.0.1:8080/mcp"
```

(Defined in )

Then run:

```bash
python MCP_Client_LangGraph.py
```

---

## 🧠 What Happens

1. Client connects to MCP server
2. Fetches available tools
3. LLM decides when to use tools
4. Tools execute on server
5. Final answer is returned

---

## 🧪 Example

Input:

```
what's (3 + 5) x 12?
```

Execution:

* add(3, 5) → 8
* multiply(8, 12) → 96

Output:

```
96
```

---

## ⚠️ Notes

* Server must be running before client
* Port must match (`8080`)
* `.env` must contain a valid OpenAI key

---

## 📌 Summary

This project shows a basic working flow:

* MCP server (tools)
* LangGraph client (agent loop)
* LLM-driven tool usage

Use this as a base to build more advanced tool-based agents.