# Simple Reflex Agent Simulation (Python)

This project demonstrates a **Simple Reflex Agent** using Python.
The agent operates inside a **2×2 grid environment** representing rooms that may be **clean or dirty**.

The agent follows a very simple rule:

* If the current room is **Dirty → Clean the room**
* If the current room is **Clean → Move to the next room**

The environment is visualized using **Matplotlib**, showing the agent’s actions step-by-step in a live simulation.

---

# Project Structure

```
Reflex_Agent/
│
├── demo_simple_reflex_agent.py
└── README.md
```

---

# Requirements

This project requires:

* Python 3.x
* matplotlib

The modules `time` and `random` (if used) are part of the **Python standard library** and do not need installation.

---

# Installation

### 1. Check Python installation

```
python --version
```

### 2. Install required library

```
pip install matplotlib
```

or

```
python -m pip install matplotlib
```

If you are using **Anaconda / Conda**:

```
conda install matplotlib
```

---

# How to Run the Project

Navigate to the project folder:

```
cd Reflex_Agent
```

Run the Python script:

```
python demo_simple_reflex_agent.py
```

A visualization window will open showing the simulation.

---

# Environment

The environment contains **four rooms arranged in a 2×2 grid**.

```
Room1 | Room2
--------------
Room3 | Room4
```

Initial configuration in the code:

```
Room1 → Clean
Room2 → Dirty
Room3 → Clean
Room4 → Clean
```

---

# Agent Behavior

This simulation implements a **Simple Reflex Agent**.

The agent makes decisions **only based on the current room state**.
It does **not remember previous states**.

### Reflex Rule

```
If room is Dirty → Clean
If room is Clean → Move to next room
```

The agent continues performing actions for a fixed number of simulation steps.

---

# Visualization

The environment is displayed using **Matplotlib graphics**.

| Element          | Representation                   |
| ---------------- | -------------------------------- |
| Clean Room       | Green square                     |
| Dirty Room       | Red square                       |
| Agent            | Blue circle                      |
| Step Information | Displayed at the top of the grid |

---

# Output (Live Visualization)

When the program runs, a graphical window opens showing the **2×2 grid environment**.

The simulation runs **step-by-step in real time**, updating approximately every second.

Each step shows:

* The **current simulation step**
* The **room where the agent is located**
* The **state of each room (Clean or Dirty)**
* The **agent’s action (Clean or Move)**

### Example Simulation Flow

Step 1
Agent starts in **Room1**.

Step 2
Agent moves to **Room2**.

Step 3
Room2 is **Dirty → Agent cleans the room**.

Step 4
Agent moves to **Room3**.

Step 5+
Agent continues moving between rooms according to the reflex rules.

The visualization updates after every step so you can **observe the agent's behavior live**.

---

# Key Functions

### `reflex_agent(state)`

Determines the action of the agent based on the room’s condition.

```
Dirty → Clean
Clean → Move
```

---

### `draw_environment(env, agent_pos, step)`

Draws the grid environment and shows:

* Room states
* Agent position
* Current simulation step

The visualization updates every second to simulate the agent's actions.

---

# Concepts Demonstrated

This project demonstrates basic **Artificial Intelligence concepts**, including:

* Simple Reflex Agents
* Agent–Environment interaction
* Rule-based decision making
* Environment perception
* AI simulation visualization using Python

---

# Final Output

After completing the simulation steps, the terminal displays:

```
Simulation complete!
```

---

# Learning Purpose

This project is useful for learning:

* Introductory **Artificial Intelligence agent models**
* How **reflex agents work**
* Python visualization with **Matplotlib**
* Basic simulation design