# Cart-Pole-problem

## Project Overview
This project demonstrates the use of Reinforcement Learning (RL) techniques to solve the classic CartPole-v1 environment using Monte Carlo, Q-Learning and SARSA algorithms. The objective is to train an agent to balance a pole on a moving cart by taking actions based on the current state of the environment.

## Methodology
### Data Preprocessing
The continuous state space of the environment is discretized into bins for ease of use with Q-learning, SARSA, and Monte Carlo methods. Discretization maps continuous values into discrete bins, allowing the agent to approximate the state-action value function.

### 1. Q-Learning Algorithm
Q-Learning is an off-policy, model-free RL algorithm.
The Q-values are updated based on the maximum possible future rewards, using the Bellman equation.
Epsilon-Greedy Policy is used for action selection, where the agent explores the environment with probability epsilon and exploits the learned Q-values with probability 1-epsilon.
### 2. SARSA Algorithm
SARSA is an on-policy RL algorithm.
The Q-values are updated based on the actual action taken by the agent in the next step, rather than the action with the highest estimated reward.
SARSA also uses the epsilon-greedy policy for action selection.
### 3. Monte Carlo (MC) Method
Monte Carlo is a model-free RL algorithm that updates the Q-values based on the average return of a complete episode.
The Q-values are updated after every episode by using the rewards accumulated over the episode.
This approach uses a first-visit Monte Carlo method, where only the first occurrence of each state-action pair in the episode is used to update Q-values.

## Results
All three algorithms were tested across 50,000 episodes to evaluate their performance in learning the optimal policy for balancing the pole.

### 1. Q-Learning:
The agent successfully solved the environment in less than 10,000 episodes, achieving an average reward greater than 195.
As the epsilon value decayed, the agent increasingly exploited the learned Q-values, leading to more consistent balancing.

### 2. SARSA:
Similar performance to Q-Learning, but updates Q-values based on the actual next action taken by the agent, following an on-policy approach.
Solved the environment within a comparable number of episodes, with slightly different learning behavior due to its more conservative nature compared to Q-Learning.

### 3. Monte Carlo:
The Monte Carlo method, which updates the Q-values only after each episode, showed slower initial learning compared to Q-Learning and SARSA but was able to reach a stable policy within 15,000 episodes.
As the Monte Carlo method relies on the entire episode's rewards, it provides a more stable update at the cost of slower convergence.

## Conclusion
This project demonstrates the successful application of three reinforcement learning algorithms—Q-Learning, SARSA, and Monte Carlo—to the CartPole-v1 environment. While all three methods are effective in solving the task, Q-Learning and SARSA tend to converge faster than Monte Carlo due to their per-step updates.
