# Snake Q-Learning Agent

This project demonstrates a simple **Q-Learning agent** that learns to play a small Snake game using **Pygame**.

The agent moves inside a **5×5 grid** and tries to reach food while avoiding collisions with walls or itself.

During training, you can **visually observe each episode** in the Pygame window while the terminal prints the reward for each episode.

---

## Project Structure

```
Learning_agent/
├── demo_learning_agent.py
└── Readme.md
```

---

## Installation

Install the required libraries:

```
pip install pygame numpy
```

---

## Run the Program

Run the script:

```
python demo_learning_agent.py
```

A **Pygame window will open**, and the snake agent will start training automatically.
Each episode runs visually in the window, and the terminal prints results like:

```
Episode 1 finished with Total Reward: -102
Episode 2 finished with Total Reward: 7
Episode 3 finished with Total Reward: 10
```

---

## Technologies Used

* Python
* Pygame
* NumPy
* Q-Learning (Reinforcement Learning)