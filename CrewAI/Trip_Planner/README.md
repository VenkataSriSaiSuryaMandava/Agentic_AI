# AI Trip Planner (CrewAI + Streamlit)

An AI-powered **multi-agent travel planning application** built using **CrewAI, Streamlit, and Ollama**.
The system uses specialized AI agents to research destinations, suggest activities, and generate a personalized travel itinerary based on user preferences.

The application can run in two ways:

* **Interactive Web App** using Streamlit
* **Jupyter Notebook workflow** for experimentation and development

---

# Features

* Multi-agent travel planning using **CrewAI**
* Web search integration using **DuckDuckGo**
* Personalized itineraries based on user interests
* Streamlit web interface
* Downloadable travel plan
* Works locally using **Ollama (Llama models)** — no external API required
* Markdown report generation

---

# System Architecture

The system is composed of **three AI agents** working together.

### 1. Location Expert

Responsible for logistics and destination research:

* Accommodation suggestions
* Transportation options
* Local weather
* Visa requirements
* Local events and practical travel information

### 2. Guide Expert

Focuses on experiences and exploration:

* Tourist attractions
* Food recommendations
* Cultural activities
* Interest-based suggestions

### 3. Planner Expert

Combines research from the previous agents and generates a **complete travel itinerary**.

The workflow runs **sequentially**, meaning each agent builds on the previous agent’s results.

---

# Project Structure

```
Trip_Planner/
│
├── streamlit_trip_advisor_app/
│   │
│   ├── my_app_2.py          # Streamlit application
│   ├── TravelAgents.py      # AI agent definitions
│   ├── TravelTasks.py       # Task definitions for agents
│   ├── TravelTools.py       # Web search tools
│
├── trip_planner.ipynb       # Jupyter Notebook version
│
├── city_report.md           # Generated research output
├── guide_report.md          # Generated guide output
├── travel_plan.md           # Final itinerary output
│
├── requirements.txt
└── README.md
```

---

# Installation

### 1. Clone the repository

```
git clone the repo
cd ai-trip-planner
```

### 2. Install dependencies

```
pip install -r requirements.txt
```

---

# Setup Ollama (Local LLM)

Install Ollama from:

https://ollama.com

Pull the required model:

```
ollama pull llama3.2
```

Start the Ollama server:

```
ollama serve
```

The app connects to:

```
http://localhost:11434
```

---

# Running the Streamlit App

Navigate to the Streamlit app folder and run:

```
streamlit run streamlit_trip_advisor_app/my_app_2.py
```

Then open the browser URL shown in the terminal (usually):

```
http://localhost:8501
```

---

# Using the Application

1. Enter your **departure city**
2. Enter your **destination**
3. Select **departure and return dates**
4. Provide your **travel interests** (food, museums, nature, nightlife, etc.)
5. Click **Generate Travel Plan**

The system will:

1. Research destination logistics
2. Generate attraction and activity suggestions
3. Build a complete itinerary

You can also **download the generated travel plan**.

---

# Running the Notebook Version

Open the notebook:

```
trip_planner.ipynb
```

Run the cells to:

* create agents
* define tasks
* run the crew workflow
* generate the travel itinerary

---

# Example Output

The system generates three markdown reports:

```
city_report.md
guide_report.md
travel_plan.md
```

Example sections in the final itinerary:

* Travel overview
* Accommodation suggestions
* Local attractions
* Food recommendations
* Daily itinerary
* Travel tips

---

# Technologies Used

* **CrewAI** – Multi-agent orchestration
* **LangChain** – LLM integrations
* **Streamlit** – Web interface
* **Ollama** – Local LLM inference
* **DuckDuckGo Search** – Web research
* **Python**

---

# Future Improvements

Potential enhancements:

* Integrate flight and hotel APIs
* Add maps and route visualization
* Include budget planning
* Add travel time optimization
* Integrate real-time weather APIs
* Deploy the app to cloud platforms