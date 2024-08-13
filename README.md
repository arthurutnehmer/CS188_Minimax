---

# Multi-Agent Pacman Project

This repository contains the code for Project 2 of the CS 188 Summer 2024 course, where we implemented various multi-agent search algorithms to control Pacman and his ghostly adversaries. The project includes implementations of Reflex, Minimax, Alpha-Beta Pruning, and Expectimax agents, as well as a custom evaluation function.

## Table of Contents
- [Project Overview](#project-overview)
- [Setup Instructions](#setup-instructions)
- [Project Details](#project-details)
  - [1. Reflex Agent](#1-reflex-agent)
  - [2. Minimax Agent](#2-minimax-agent)
  - [3. Alpha-Beta Pruning](#3-alpha-beta-pruning)
  - [4. Expectimax Agent](#4-expectimax-agent)
  - [5. Evaluation Function](#5-evaluation-function)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

In this project, we design agents for the classic Pacman game, now including ghost adversaries. The tasks involve implementing both minimax and expectimax search algorithms, enhancing the Reflex agent, and designing an evaluation function to optimize Pacman’s gameplay.

## Setup Instructions

To run the code in this repository, ensure you have Python installed. The following Python packages are required:

- `pygame` (for graphical display)
- `numpy` (for numerical computations)

You can install these dependencies using pip:

```bash
pip install pygame numpy
```

## Project Details

### 1. Reflex Agent
The Reflex Agent is a simple agent that selects actions based on a state-action evaluation function. The goal was to improve this agent to play Pacman more effectively by considering both food and ghost positions.

**Files involved**: `multiAgents.py` (ReflexAgent class)

### 2. Minimax Agent
The Minimax Agent implements the minimax search algorithm, accounting for the moves of Pacman and all ghosts. This agent performs adversarial search to maximize Pacman’s score while minimizing potential losses.

**Files involved**: `multiAgents.py` (MinimaxAgent class)

### 3. Alpha-Beta Pruning
The Alpha-Beta Pruning Agent extends the Minimax Agent by incorporating alpha-beta pruning, which reduces the number of game states that need to be evaluated, thus optimizing the decision-making process.

**Files involved**: `multiAgents.py` (AlphaBetaAgent class)

### 4. Expectimax Agent
The Expectimax Agent models the behavior of ghosts probabilistically. Instead of assuming optimal adversarial moves, this agent considers the expected outcomes based on the ghosts’ random behavior.

**Files involved**: `multiAgents.py` (ExpectimaxAgent class)

### 5. Evaluation Function
The final task involved designing a custom evaluation function that evaluates game states, optimizing Pacman’s chances of winning the game. The function considers factors such as distance to food, proximity to ghosts, and other heuristics to guide Pacman’s actions.

**Files involved**: `multiAgents.py` (betterEvaluationFunction)

## Usage

To run the Pacman game with a specific agent, use the following commands:

- Reflex Agent:
  ```bash
  python pacman.py -p ReflexAgent
  ```

- Minimax Agent:
  ```bash
  python pacman.py -p MinimaxAgent -a depth=3
  ```

- Alpha-Beta Pruning Agent:
  ```bash
  python pacman.py -p AlphaBetaAgent -a depth=3
  ```

- Expectimax Agent:
  ```bash
  python pacman.py -p ExpectimaxAgent -a depth=3
  ```

You can also run the autograder to test the correctness of your implementations:

```bash
python autograder.py
```

## Contributing

Contributions are welcome! Feel free to fork the repository, make changes, and submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
