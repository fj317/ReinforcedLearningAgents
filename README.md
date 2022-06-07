# Reinforced Learning Agents in Gridworld
Various agents that implement reinforced learning algorithms in a gridworld environment.

The environment is based on a gridworld environment with two objects being present: a bomb - if hit by the agent, it gives a reward of -10 and terminates the episode; and a goal state - if reached a reward of 10 is given and the episode termiantes. The agent has four possible actions in each state (grid square): west, north, south, and east. The actions are unreliable. They move the agent in the intended direction with probability 0.8, and with probability 0.2, they move the agent in a random other direction. If the direction of movement is blocked, the agent remains in the same grid square. The initial state of the agent is one of the five grid squares at the top, selected randomly. A reward of -1 is given to the agent for each navigational action. 

![gridworld environment](https://github.com/fj317/ReinforcedLearningAgents/blob/main/img/bombs%20and%20gold%20numbers.png)

## Q-Learning.ipynb
The agent uses a Q-Learning algorithm that creates a table if each state-action pair and assigns a Q-value to it. Using these Q-Values the agent can find the best path to the goal from its initial starting square. A learning curve is also plotted, showing the mean total reward the agent collects over each episode. A random agent is also implemented as a comparison tool.

## Value Iteration.ipynb
Using value iteration (and the Bellman optimality equation), the optimal policy is calculated and found. The optimal policy and the state values are outputted. There are two versions of this program - one where the agent is guaranteed to successfully complete the action, and one where the agent has a 20% chance of the action failing to complete.

# Racetrack.ipynb
Various tabular methods are implemented to solve the task of driving a racecar around a short track. The environment's dynamics are described in the notebook as well as each of the different algorithms. 

In short, on-policy first-visit Monte Carlo control, Sarsa and Q-learning algorithms are implemented, as well as a modified Q-learning agent that implements the Sarsa(λ) algorithm to improve the performance of the agent's learning. A comparison of each algorithm is also given in the notebook. The file (and environment) is located in the Racetrack folder.
