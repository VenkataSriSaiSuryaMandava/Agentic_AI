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

## 🧮 Calculator MCP Server

No build required. Installed via pip.

Runs automatically using:

```python
"command": "python",
"args": ["-m", "mcp_server_calculator"]
```

---

## ▶️ Running the Project

### Run the Client

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

**Weather:**

* `What's the weather in London?`
* `Temperature in New York`

**Math:**

* `25 * 48`
* `sqrt(144)`

---

## ⚙️ How It Works

* `MultiServerMCPClient` connects to multiple MCP servers
* Tools are dynamically loaded
* LangGraph manages execution flow:

  * Model → Tool → Model loop
* The agent decides when to call:

  * Weather tools
  * Calculator tools

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

## 📚 Resources

* MCP Servers List:
  https://github.com/modelcontextprotocol/servers

* Weather MCP:
  https://github.com/mschneider82/mcp-openweather

---
