## Udacity Deep Reinforcement Learning Nanodegree 
## Project 1: Navigation

### Learning Algorithym

In this project the environment is solve by using the DQN Reinforcement Learning Algorithym. The DQN takes the state as input and generates the action value as per the current policy. 
Then the agent receives the 

1. The agent receives a state vector from the environment
1. 

#### Learning Algorithms



#### Agent Hyperparameters

##### All Deep Q-Networks

- `epsilon` controls the degree of exploration vs exploitation of the agent in selecting its actions. `epsilon = 0` implies that the agent is greedy with respect to the Q-network (pure exploitation) and `epsilon = 1` implies that the agent selects actions completely randomly (pure exploration). In this project, `epsilon` was initially annealed from 1.0 to 0.1 in steps of 0.001 after each episode, and remained fixed at 0.1 therafter. This was subsequently adapted to decay exponentially by a factor of 0.995 per episode from 1.0 to 0.01
- `GAMMA = 0.99` is the discount factor that controls how far-sighted the agent is with respect to rewards. `GAMMA = 0` implies that only the immediate reward is important and `GAMMA = 1.0` implies that all rewards are equally important, irrespective whether they are realised soon and much later
- `TAU = 0.001` controls the degree to which the target Q-network parameters are adjusted toward those of the local Q-network. `TAU = 0` implies no adjustment (the target Q-network does not ever learn) and `TAU = 1` implies that the target Q-network parameters are completelty replaced with the local Q-network parameters
- `LR = 0.0005` is the learning rate for the gradient descent update of the local Q-network weights
- `UPDATE_EVERY = 4` determines the number of sampling steps between rounds of learning (Q-network parameter updates)
- `BUFFER_SIZE = 10000` is the number of experience tuples `(state, action, reward, next_state, done)` that are stored in the replay buffer and avaiable for learning
- `BATCH_SIZE = 64` is the number of tuples that are sampled from the replay buffer for learning

##### Prioritised Experience Replay

- `e_priority = 0.01` is added to the absolute value of the TD error to ensure that none of the priorities are exactly zero. This ensures that all tuples in the replay buffer have a non-zero probability of being selected for training
- `a_priority` controls the extent to which the TD error influences the probability of selecting a tuple for training. `a_priority=0` implies that all tuples in the buffer have equal probability of selection, while `a_priority=1` implies pure priority (TD error-based) sampling. We set `a_priority = 0.6` as in [this paper](https://arxiv.org/pdf/1511.05952.pdf)
- `b_priority` controls the extent to which the biased sampling from the replay buffer is corrected in the gradient descent update. `b_priority 
