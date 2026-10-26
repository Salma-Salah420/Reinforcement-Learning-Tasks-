# Reinforcement Learning Tasks

## 📌 Overview
This repository contains practical tasks and implementations related to **Reinforcement Learning (RL)**. The tasks focus on understanding how an agent interacts with an environment, learns from rewards, and improves its decisions through experience.

## 🎯 Objectives
- Understand the fundamental concepts of Reinforcement Learning.
- Implement the Q-Learning algorithm.
- Design a custom environment with states, actions, and rewards.
- Train an agent through multiple episodes.
- Evaluate the agent's learned policy.

## 🧠 Task 1: Q-Learning Thermostat

### Description
Develop a simple thermostat control system using Q-Learning. The agent learns to choose appropriate heating or cooling actions based on the current temperature state.

### Environment

**States:**
- `Cold`
- `Comfortable`
- `Hot`

**Actions:**
- `Heat`
- `Cool`
- `Do Nothing`

**Goal:**

Learn a policy that maintains a comfortable temperature while avoiding unnecessary heating or cooling.

### Algorithm: Q-Learning

Q-Learning is a model-free Reinforcement Learning algorithm that updates action values using rewards and estimated future rewards.

The update rule is:

\[
Q(s,a) \leftarrow Q(s,a)+\alpha[r+\gamma\max_{a'}Q(s',a')-Q(s,a)]
\]

Where:
- \(s\): Current state
- \(a\): Selected action
- \(r\): Received reward
- \(s'\): Next state
- \(\alpha\): Learning rate
- \(\gamma\): Discount factor

### Hyperparameters

| Parameter | Value |
|---|---:|
| Learning Rate (\(\alpha\)) | 0.1 |
| Discount Factor (\(\gamma\)) | 0.9 |
| Training Episodes | 500 |
| Environment | Custom Python environment |
| Algorithm | Q-Learning |

### Implementation Steps
1. Define the environment states and available actions.
2. Design the reward function.
3. Initialize the Q-table.
4. Select actions using an exploration strategy such as epsilon-gre
