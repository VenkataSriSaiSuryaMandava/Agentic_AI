# CrewAI Projects

This repository contains **AI projects built using CrewAI and LangChain**.
Each project demonstrates how multiple AI agents can collaborate to solve different tasks such as research, content generation, and travel planning.

---

## Projects Included

### 1. News Summarization

A multi-agent system that researches the latest **AI industry trends** and generates a short **blog-style summary**.

**Features**

* Web research using search tools
* AI-generated summaries
* Markdown blog output

**File**

```
News_Summarization/new_summarization.ipynb
```

---

### 2. AI Trip Planner

An AI-powered **travel itinerary generator** that creates personalized travel plans based on user preferences.

The system uses multiple agents to:

* research destination logistics
* suggest attractions and food
* generate a complete travel itinerary

It can run in **two modes**:

* Jupyter Notebook
* Streamlit web application

**Folder**

```
Trip_Planner/
```

---

## Tech Stack

* CrewAI
* LangChain
* Streamlit
* Ollama (local LLMs)
* DuckDuckGo Search
* Python

---

## Requirements

Install dependencies:

```
pip install -r requirements.txt
```

---

## Running the Projects

### News Summarization

Open and run:

```
News_Summarization/new_summarization.ipynb
```

---

### Trip Planner

Run the Streamlit app:

```
streamlit run Trip_Planner/streamlit_trip_advisor_app/my_app_2.py
```

or open the notebook:

```
Trip_Planner/trip_planner.ipynb
```

---

## Purpose

These projects demonstrate how **multi-agent AI systems** can automate complex workflows like:

* research
* summarization
* itinerary planning
* information synthesis