# Multi MCP Servers (Weather + Calculator)

This project demonstrates how to connect multiple MCP (Model Context Protocol) servers to a LangGraph-based agent using LangChain.

The agent can:

* Fetch weather data from a Weather MCP server
* Perform calculations using a Calculator MCP server
* Automatically decide which tool to use

---

## 📦 Requirements

* Python 3.9+
* Go (only required if building weather server from source)
* OpenAI API key
* OpenWeatherMap API key

---

## 🔑 Environment Setup

Create a `.env` file in the root directory:

```
OPENAI_API_KEY=your_openai_key_here
OWM_API_KEY=your_openweather_key_here
```

⚠️ Your current file is named `env.txt`. Rename it to `.env` or it won’t load. 

---

## 📥 Install Dependencies

```
pip install python-dotenv langchain-mcp-adapters langgraph "langchain[openai]" mcp mcp-server-calculator
```

---

## 🌦️ Weather MCP Server Setup

### Option 1 (Recommended): Use Prebuilt Binary

Download or build the weather MCP server:

```
git clone https://github.com/mschneider82/mcp-openweather.git
cd mcp-openweather
go build -o mcp-weather
```

This generates:

* Windows → `mcp-weather.exe`
* Mac/Linux → `mcp-weather`

---

## ⚠️ IMPORTANT FIX (Your Code Issue)

Your script uses a hardcoded path:

```python
"command": "E:/langraph_mcp-demo/mcp-openweather/mcp-weather.exe"
```

This will break on other machines.

### ✅ Replace with:

```python
"command": "./mcp-weather.exe"  # Windows
```

or

```python
"command": "./mcp-weather"  # Mac/Linux
```

---

## 🧮 Calculator MCP Server

No build required. Installed via pip.

Runs automatically using:

```python
"command": "python",
"args": ["-m", "mcp_server_calculator"]
```

---

## ▶️ Running the Project

### Step 1 — Start MCP Servers (Optional)

Your code already launches servers via stdio, so **manual startup is NOT required**.

---

### Step 2 — Run the Client

```
python Multiple_MCP_Servers.py
```

---

## 💬 Usage

You’ll get an interactive prompt:

```
Ask me anything (weather or calculation) →
```

### Examples

* Weather:

  * `What's the weather in London?`
  * `Temperature in New York`

* Math:

  * `25 * 48`
  * `sqrt(144)`

---

## ⚙️ How It Works

* `MultiServerMCPClient` connects to multiple MCP servers 
* Tools are dynamically loaded
* LangGraph routes:

  * Model → Tool → Model loop
* Agent decides when to call:

  * Weather API
  * Calculator

---

## 🧠 Architecture Flow

```
User Input
   ↓
LLM (GPT-4o-mini)
   ↓
Tool Decision
   ↓
MCP Server (Weather / Calculator)
   ↓
Response → User
```

---

## 🛠️ Common Issues

### 1. Keys Not Loading

* Make sure `.env` is in the root
* Do NOT use `env.txt`

---

### 2. Weather Not Working

* API key may take a few hours to activate
* Check OpenWeather dashboard

---

### 3. Path Errors

* Fix hardcoded Windows path in code
* Use relative paths instead

---

### 4. Module Errors

If you see missing modules:

```
pip install -U langchain langgraph
```

---

## 📚 Resources

* MCP Servers List:
  https://github.com/modelcontextprotocol/servers

* Weather MCP:
  https://github.com/mschneider82/mcp-openweather

---

## ✅ Improvements You Should Consider

* Remove hardcoded paths completely
* Add CLI arguments for server paths
* Add logging instead of print statements
* Handle tool errors more gracefully

---

## 🚀 Summary

You now have a multi-tool AI agent that:

* Uses real APIs
* Dynamically selects tools
* Runs locally with MCP servers