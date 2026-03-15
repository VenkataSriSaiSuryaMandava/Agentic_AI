# AI Market Research & Blog Generator

This project uses **CrewAI agents** and **LangChain** to automatically research the latest AI industry trends and generate a blog post based on that research.

The system runs two AI agents:

1. **Market Research Analyst** – searches the web and summarizes the latest AI developments.
2. **Content Writer** – converts the research summary into a readable blog post.

The final blog post is automatically saved as a Markdown file.

---

# How It Works

The workflow is built using **CrewAI**, which coordinates multiple AI agents working together on tasks.

### Step 1 — Research Agent

The research agent uses a web search tool to find current AI industry trends and produces a summarized report.

### Step 2 — Writing Agent

The writer agent takes the research summary and converts it into a **4-paragraph blog post** written in Markdown.

### Step 3 — Crew Execution

CrewAI orchestrates both agents and runs the tasks sequentially.

The final output is saved to:

```
blog-posts/new_post.md
```

---

# Installation

Install required dependencies:

```
pip install crewai crewai_tools langchain langchain_community langchain_openai
```

---

# Setup

Set your OpenAI API key before running the notebook:

```
export OPENAI_API_KEY="your_api_key"
```

or inside Python:

```
import os
os.environ["OPENAI_API_KEY"] = "your_api_key"
```

---

# Agents

## Market Research Analyst

**Role:** Market Research Analyst
**Goal:** Provide up-to-date analysis of the AI industry
**Tools:** WebsiteSearchTool

Responsibilities:

* Search the web
* Identify major AI trends
* Produce a concise research summary

---

## Content Writer

**Role:** Content Writer
**Goal:** Write engaging blog posts about AI

Responsibilities:

* Read the research summary
* Turn insights into a structured article
* Output Markdown formatted content

---

# Tasks

### Research Task

Search the web and summarize the **top 3 trending AI developments** and their impact.

### Writing Task

Generate a **4-paragraph blog post** based on the research results.

---

# Running the Project

Execute the notebook or script and start the crew workflow:

```
crew.kickoff()
```

CrewAI will:

1. Run the research agent
2. Pass the results to the writing agent
3. Save the generated blog post

---

# Output Example

The final result is a Markdown blog article like:

```
blog-posts/new_post.md
```

This file can be directly used for publishing or editing.

---

# Technologies Used

* CrewAI
* LangChain
* OpenAI GPT Models
* Python

---

# Possible Improvements

Some useful upgrades you could add:

* Add more research sources (news APIs, RSS feeds)
* Generate multiple blog drafts
* Schedule automated daily trend reports
* Publish directly to a CMS or website
* Add SEO keyword generation