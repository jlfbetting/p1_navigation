# Project 1: Navigation
## Project details
P1 of the Udacity Deep Reinforcement Learning course. This repository contains the following files:
* README.md - this file
* Report.md - report, describing the algorithm and implementation
* Navigation.ipynb - Jupyter notebook, containing the code
* checkpoint.pth - trained model

The 'Banana' environment is part of the Unity environment and is made available to the student. Udacity explained the rules as follows:
A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:

* ``0`` - move forward.
* ``1`` - move backward.
* ``2`` - turn left.
* ``3`` - turn right.
The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.

## Getting started
It is not necessary to install Unity for this project, because the environment was built by Udacity. I used the 64-bit Windows version, which is available [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip). The zip file needs to be extracted in the same folder as `Navigation.ipynb`.
Instructions on how to install the other dependencies can be found [here](https://github.com/udacity/deep-reinforcement-learning#dependencies).

## Instructions
The code in the repository can be run by executing the cells of the environment in order. If you want to skip training the agent and just see the trained agent, skip or comment out the cells in section 5.
