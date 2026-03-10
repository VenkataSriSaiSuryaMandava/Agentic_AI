# Goal Based Agent – Job Application Assistant

## Overview

This project implements a **Goal-Based AI Agent** that collects required information for a job application.

The agent interacts with the user and continues asking questions until it gathers:

* Name
* Email
* Skills

Once all required data is collected, the agent confirms the application is ready.

Two versions of the application are included:

| Version                    | Interface | Description                     |
| -------------------------- | --------- | ------------------------------- |
| **goal_based_agent_v1.py** | CLI       | Runs in the terminal            |
| **goal_based_agent_v2.py** | Streamlit | Web-based UI with resume upload |

---

# Project Structure

```
Goal_Based_Agent
│
├── .env
├── .env.example
├── .gitignore
├── goal_based_agent_v1.py
├── goal_based_agent_v2.py
└── README.md
```

---

# Features

## Goal-Based Agent

The agent works toward a specific goal:

```
Collect: name, email, skills
```

The conversation continues until the goal is achieved.

---

## Version 1 – CLI Agent

Runs in the terminal and interacts with the user through text input.

Example:

```
You: my name is Sai
Bot: Name saved. Still need: email, skills
```

---

## Version 2 – Streamlit Web App

Features:

* Chat interface
* Resume upload
* Automatic information extraction from PDF
* Application status tracking
* Download application summary

---

# Installation

### 1. Clone the repository

```
clone the repository
cd Goal_Based_Agent
```

---

### 2. Install dependencies

```
pip install -r requirements.txt
```

If requirements.txt is not available, install manually:

```
pip install streamlit langchain langchain-openai python-dotenv pymupdf
```

---

### 3. Setup Environment Variables

Create a `.env` file:

```
OPENAI_API_KEY=your_openai_api_key
```

Example `.env.example`:

```
OPENAI_API_KEY=your_api_key_here
```

---

# Running the Application

## Run CLI Version

```
python goal_based_agent_v1.py
```

---

## Run Streamlit Version

```
streamlit run goal_based_agent_v2.py
```

Open in browser:

```
http://localhost:8501
```

---

# Example Workflow

1. User enters information in chat
2. Agent extracts name, email, and skills
3. Agent checks if all required data is collected
4. If missing data exists, the agent asks again
5. When complete, the application summary is generated

---

# Technologies Used

* Python
* LangChain
* OpenAI GPT
* Streamlit
* PyMuPDF
* Regex

---

# Future Improvements

Possible enhancements:

* LLM-based information extraction instead of regex
* Database storage for applications
* Multi-agent architecture
* Resume ranking system
* Email notification system
