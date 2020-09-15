# Report

## Learning Algorithm
The algorithm uses Deep Q-learning to train an agent to take actions in the given environment, optimizing the rewards. The experiences tuples (s, a, r, s', done) are saved in a buffer, and every `update_every` episodes, a sample of `batch_size` experiences is taken to train the agent. The size of the buffer is constrained to `buffer_size` experiences. Learning happens with a discount factor of `gamma`, and the update model uses an interpolation parameter of `tau`. Learning happens with a learning rate of `lr`. The Q-network consists of 2 hidden layers, fc1 and fc2, with the number of units per layer defined by the parameters `fc1_units` and `fc2_units`.

The values for the hyperparameters were determined experimentally, using a grid search. The following values worked well:
* `update_every` = 6
* `batch_size` = 50
* `buffer_size` = 100000000000
* `gamma` = 0.9999
* `tau` = 0.001
* `lr` = 0.0005
* `fc1_units` = 100
* `fc2_units` = 100

The maximum number of episodes was set at 1000, and the environment was considered 'solved' if the average score over 100 episodes was equal to or higher than 13.5 (the rubic gives +13 as the number of average reward for the environment to be considered 'solved', but it turned out it was easy to obtain 13.5 by training for a few more episodes). With these parameters, it took 728 episodes to solve the environment.

## Plot of Rewards
The following figure shows the score per episode during the training process, and the average score over the past 100 episodes. At 728 episodes, the average score exceeded the value of 13.5, solving the environment.
![Plot of the rewards](https://github.com/jlfbetting/p1_navigation/blob/master/AvgScores.png)

## Ideas for future work
* We could increase the number of layers in the Q-network, or use a different architecture than MLP.
* We could implement techniques such as Prioritized Experience Replay, or Dueling DQN (which were discussed in the course)

