# My-DRL-Project-1
[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# Project 1: Navigation

### Introduction

For this project, I will train an agent to navigate (and collect bananas!) in a large, square world.  

![Trained Agent][image1]

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, the trained agent must get an average score of +13 over 100 consecutive episodes.

### Instructions

I made this project in the workspace provided by Udacity. The Unity Environment was already installed in the workspace. So it is sufficient to copy all files to the workspace and open the files Navigation.ipynb and run the code cells. 

The resulting training weights will be saved as a file named My_Weights.pth under the same path. 

### File Descriptions

- My_Model.py defines the DQN model architecture
- My_DQN_Agent.py defines how the agent takes actions based on the policy and learns based on feedback from the environment
- Navigation.ipynb runs the environemt and trains the agent. This is the main code to solve the environment
- My_Weights.pth contains the weights for the final DQN
