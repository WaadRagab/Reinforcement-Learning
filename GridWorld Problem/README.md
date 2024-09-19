# GridWorld with Value Iteration
## Project Overview
This project implements a GridWorld environment in which an agent uses the Value Iteration algorithm to navigate a grid, avoiding obstacles and maximizing rewards. The environment is modeled as a Markov Decision Process (MDP), with rewards placed on specific grid cells and obstacles acting as walls. The goal is for the agent to learn the optimal policy that dictates the best action to take in each state to achieve the highest cumulative reward.

## Environment
The grid is a 3x4 grid with the following features:
* Rewards:
  * A reward of +1 at position (0, 3)
  * A reward of -1 at position (1, 3)
* Walls:An obstacle located at position (1, 1) that blocks movement.
* Actions: The agent can move in four possible directions: up, down, left, or right.

## Methodology
* Grid Initialization: The environment is initialized with the specified number of rows, columns, rewards, and obstacles.
* Value Iteration: At each iteration, the agent updates the value of each state based on its current value, rewards, and transition probabilities. After multiple iterations, the values converge, leading to the extraction of an optimal policy.
* Policy Extraction: After the values converge, the optimal policy is extracted, dictating the best action for the agent to take in each state.

## Results
* Convergence: The values of the states converge after several iterations, and the agent learns an optimal policy that maximizes its cumulative rewards.
* Policy Visualization: The agent's learned policy is visualized as directional arrows on the grid, showing the optimal movement from each state.

## Conclusion
This project demonstrates the effectiveness of the Value Iteration algorithm in solving grid-based MDP problems. The agent learns to navigate the grid while avoiding obstacles and maximizing rewards. Value Iteration is a powerful technique for finding the optimal policy in environments with deterministic or stochastic transitions.
