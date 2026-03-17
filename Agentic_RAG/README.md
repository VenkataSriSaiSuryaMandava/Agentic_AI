# 🚀 Agentic RAG System

An **Agentic Retrieval-Augmented Generation (RAG)** system that combines LLM reasoning with dynamic information retrieval using PostgreSQL + pgvector.

This project demonstrates how to build **AI agents that can autonomously search, retrieve, and reason over external knowledge sources in real-time**.

---

## 🔥 What This Project Does

* Uses LLM-powered agents to **plan, decide, and execute queries dynamically**
* Retrieves relevant documents using **semantic vector embeddings**
* Stores and queries embeddings efficiently via **PostgreSQL + pgvector**
* Enhances responses with **context-aware retrieval (RAG pipeline)**
* Integrates external knowledge sources like **Arxiv for live data retrieval**

---

## 🧠 Why This Matters

Traditional LLMs:

* Limited to static training data
* Prone to hallucination when lacking context

This system:

* Fetches **up-to-date, relevant information at runtime**
* Improves **response accuracy and grounding**
* Enables **agentic workflows with multi-step reasoning**

---

## 🏗️ Architecture Overview

1. **User Query**
2. **Agent Planning**

   * Determines whether retrieval is required
3. **Embedding Generation**
4. **Vector Similarity Search (pgvector)**
5. **Context Injection into Prompt**
6. **LLM Response Generation**

---

## ⚙️ Tech Stack

* **Python**
* **PostgreSQL**
* **pgvector**
* **Agno (Agent framework)**
* **Arxiv API**
* **LLMs (OpenAI / compatible APIs)**

---

## 📦 Setup Instructions

### 1. Install Dependencies

```bash
pip install -U agno
pip install arxiv
pip install pgvector psycopg[binary]
```

---

### 2. Setup PostgreSQL

Download PostgreSQL:
https://www.postgresql.org

Check version:

```bash
psql --version
```

Login:

```bash
psql -U postgres
```

Create DB and user:

```sql
CREATE USER ai WITH PASSWORD 'ai';
CREATE DATABASE ai;
GRANT ALL PRIVILEGES ON DATABASE ai TO ai;
```

---

### 3. Install pgvector Extension

Download:
https://github.com/andreiramani/pgvector_pgsql_windows/releases

Steps:

* Copy `vector.dll` → PostgreSQL `/lib`
* Copy `.control` and `.sql` → `/share/extension`
* Restart PostgreSQL

```bash
net stop postgresql-x64-17
net start postgresql-x64-17
```

---

### 4. Environment Variables

Create `.env` file:

```env
GOOGLE_API_KEY=your_api_key_here
```

---

## ▶️ Running the Project

```bash
jupyter notebook
```

Open:

* `RAG.ipynb`
* `AgenticRAG.ipynb`

---

## 📊 Example Workflow

* User asks: *"Summarize recent research on LLM agents"*
* Agent:

  * Queries Arxiv API
  * Retrieves and ranks relevant papers
  * Generates embeddings and context
  * Produces a structured, grounded response

---

## 📁 Project Structure

```
.
├── AgenticRAG.ipynb
├── RAG.ipynb
├── README.md
├── env.txt
├── laptops_info.txt
```

---

## 🚀 Key Features

* Autonomous agent decision-making
* Real-time knowledge retrieval
* High-performance vector search with pgvector
* Modular and extensible architecture
* Easy integration with external data sources

---

## ⚠️ Limitations

* Requires PostgreSQL + pgvector setup
* Dependent on external APIs (latency + limits)
* No production UI (notebook-based execution)

---

## 🔮 Future Improvements

* Add FastAPI backend for API access
* Build frontend (Next.js / React)
* Introduce multi-agent collaboration
* Add document ingestion (PDFs, Notion, internal data)
* Optimize caching and retrieval latency

---