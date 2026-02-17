# Sequential Decision Making: Chomp Implementation

## Abstract
This repository contains the source code and technical documentation for the "Sequential Decision Making" project at Kühne Logistics University (KLU). The objective of this project is to model the impartial game "Chomp" as a Markov Decision Process (MDP) and solve it using Reinforcement Learning.

The project is implemented in Python using the Gymnasium API. It compares the performance of a Reinforcement Learning agent (SARSA) against a Heuristic (rule-based) agent and a Random baseline.

**Course:** Management Science & Operations Research
**Module:** Sequential Decision Making
**Instructor:** Prof. Dr. Arne Heinold

---
## Project Description
### The Game: Chomp
Chomp is a two-player game played on a rectangular grid (representing a chocolate bar).
* **State Space:** The configuration of the remaining chocolate squares.
* **Action Space:** A player selects a square $(r, c)$, removing that square and all squares below and to the right of it.
* **Terminal State:** The game ends when a player is forced to select the top-left square $(0,0)$, which is designated as "poisoned."

### Implementation Details
The problem is modeled as a Markov Decision Process (MDP) with the following specifications:
* **Environment:** A custom environment built upon the Gymnasium standard.
* **State Representation:** To optimize memory usage, the board state is represented as a tuple of row lengths rather than a binary matrix.
* **Rewards:** A sparse reward signal is used (+1 for winning, -1 for losing).

---

## Methodology

This project implements and compares two distinct solution approaches as required by the assignment guidelines:

### 1. Reinforcement Learning (SARSA)
An On-Policy Temporal Difference (TD) learning algorithm is implemented to estimate the optimal action-value function $Q(s, a)$.
* **Variant:** SARSA with backward pass.
* **Update Mechanism:** State-values are updated at the end of each episode (game) by propagating the reward signal backward from the terminal state to the initial state. This approach is selected to address the sparse reward structure

---
# Disclaimer and License

##License: MIT License
Academic Disclaimer:
This repository represents student work submitted for grading in the Management Science & Operations Research course at KLU. It is intended solely for educational purposes.
