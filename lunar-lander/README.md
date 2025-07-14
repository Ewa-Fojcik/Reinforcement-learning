# Deep Reinforcement Learning: Lunar Lander

## Overview

This project implements and analyzes a **Deep Q-Network (DQN)** agent designed to solve the `LunarLander-v2` environment from the Gymnasium library. The core focus is on investigating how different **epsilon decay rates** impact the agent's learning performance and efficiency, specifically examining the critical **exploration-exploitation trade-off** in Deep Reinforcement Learning.

## Key Components

The key components of this project include:

* **Deep Q-Network (DQN) Agent:** Implementation of a DRL agent that leverages neural networks to approximate the Q-function, enabling it to handle high-dimensional state spaces.
* **Gymnasium Environment Integration:** Seamless interaction with the `LunarLander-v2` environment, processing its 8-dimensional continuous state space and executing 4 discrete actions (do nothing, fire left, fire main, fire right engine).
* **Epsilon-Greedy Exploration:** Experimentation with three distinct epsilon decay rates (slow: 0.003, medium: 0.005, fast: 0.01) to analyze their influence on the agent's learning trajectory.
* **Training Algorithm:** A standard DQN algorithm using a neural network with an 8-node input layer, two hidden layers of 64 neurons (ReLU activation), and a 4-node output layer.
* **Hyperparameter Tuning Analysis:** Examination of how varying epsilon decay rates affect the optimal balance between exploration and exploitation.

## Implementation Details

* **Environment:** LunarLander-v2 (Gymnasium library).
* **Agent Architecture:** Deep Q-Network (DQN).
* **Neural Network:** Input (8 nodes), 2 Hidden Layers (64 neurons each, ReLU), Output (4 nodes).
* **Training Episodes:** 1000 episodes for each epsilon decay rate configuration.
* **Hyperparameters:** Discount factor (gamma): 0.99, Initial epsilon: 1.0, Minimum epsilon: 0.01, Learning rate: 0.001, Optimizer: Adam, Loss function: Mean Squared Error (MSE).
* **Exploration Strategies:**
    * Slow decay: 0.003 per episode (decay rate = 0.997)
    * Medium decay: 0.005 per episode (decay rate = 0.995)
    * Fast decay: 0.01 per episode (decay rate = 0.99)
* **Frameworks:** Python with PyTorch

## Key Findings

The experimentation with different epsilon decay rates revealed significant differences in learning efficiency and final agent performance:

* **Learning Speed:** The fast decay rate (0.01) demonstrated the quickest learning, achieving good performance by episode 250 and maintaining it. The medium decay showed good but slower learning, while the slow decay struggled to converge.
* **Stability:** The fast decay exhibited the most stable rewards post-learning, with fewer extreme drops. The medium decay showed good stability after episode 300, while the slow decay remained highly volatile.
* **Loss Patterns:** The fast decay achieved the fastest stabilization of loss values to consistently low levels. The slow decay's erratic loss patterns, including periodic spikes, suggested unstable convergence.
* **Final Performance:** Fast and medium decay rates yielded comparable strong final rewards (approx. 259-260), indicating successful policy convergence. The slow decay resulted in negative final rewards.
* **Exploration-Exploitation Balance:** The results underscore that for environments with clear feedback signals like Lunar Lander, a quicker transition to exploitation (fast decay) can accelerate learning without sacrificing final performance, challenging the assumption that slower exploration is always preferable.

## Experimental Results

The project includes plots of training rewards and loss over 1000 episodes for each decay rate, visually demonstrating the learning progression and stability.
