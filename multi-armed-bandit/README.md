# Bioinspired Machine Learning: Multi-Armed Bandit
## Overview
This project implements a multi-armed bandit algorithm using the ε-greedy strategy, exploring the exploration-exploitation trade-off in reinforcement learning. The focus is on evaluating how different exploration rates (ε = 0, ε = 0.01, ε = 0.1) impact the agent's performance in a 10-armed bandit environment with stationary reward distributions.

## The key components of this project include:

- Multi-Armed Bandit Algorithm: Implementing the ε-greedy approach to solve the 10-armed bandit problem.

- Exploration and Exploitation: Analyzing the trade-off between exploring new actions and exploiting known ones.

- Action-Value Methods: Estimating the value of actions using methods like the sample-average method.

## Group Members
Ewa Fojcik 

Pantelis Kasioulis 

Gabriel Thomas Newton

Zoi Kallinaki

## Project Structure
- Colab Notebook: https://colab.research.google.com/drive/1_gEJhe49eia0NQqvJZJWNPz_KPwKpjZK?usp=sharing 

- Code File: Python code for the implementation of the multi-armed bandit algorithm is available in the .ipynb format.

## Implementation Details
- Multi-Armed Bandit Problem: The environment consists of 10 arms, each with a true value sampled from a normal distribution. The ε-greedy algorithm is used for action selection, balancing exploration and exploitation.

- Exploration-Exploitation Trade-Off: Analyzing how the exploration rate affects the agent's ability to optimize its rewards.

- Action-Value Estimation: Using the sample-average method to estimate action values and guide decision-making.

## Key Findings
- Greedy Algorithm (ε = 0): Performed suboptimally due to lack of exploration.

- ε = 0.01: Steady improvement over time with balanced exploration.

- ε = 0.1: Showed faster exploration, leading to better results in the short term.

## Experimental Results
- Average Rewards Over Time: A comparison of performance for different ε values.

- Percentage of Optimal Action Selections: Tracking how often the agent selects the optimal action.

- Cumulative Regret: Measuring the opportunity cost of choosing suboptimal actions.
