# Multi-Agent Actor-Critic for Mixed Environment

Implementation of [MADDPG](https://arxiv.org/pdf/1706.02275.pdf) in pytorch to solve Unity's [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md) environment: a two-player game where agents control rackets to hit a ball over the net. The environment is considered solved if the mean reward over 100 episodes of the maximum score of agents over an episode is at least +0.5

__Project contains__:

* __report.pdf__: model architecture details and training choices made to solve the environment.
* __training.ipynd__:  jupyter notebook for training the agent, and watching the agent interact with the environment with pre-trained weights.
* __agent__: folder containing the implementation of MADDPG in an agent class, and actor-critic network classes.
* __actor.pth__: actor network pretrained weights.
* __critic.pth__: critic network pretrained weights.

### Project Details

* __Goal__:  The agents must keep the ball in play.
* __Agent Reward Function__: 
    - +0.1 if an agent hits the ball over the net
    - -0.01 every time the agent lets a ball hit the ground or hits the ball out of bounds
* __Behaviour Parameters__:
    - Observation space: 9 variables corresponding to position, velocity and orientation of ball and racket.
    - Action space: 2 variables corresponding to movement toward net or away from net and jumping

### Getting Started

* __Dependencies__: Project uses [PyTorch](https://pytorch.org/) and [Unity ML-Agents Toolkit](https://github.com/Unity-Technologies/ml-agents). To set up your python environment follow instruction on following link:
https://github.com/udacity/deep-reinforcement-learning

* __Environment__: The environment used in this project can be found here:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here]([click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)
    
### Instructions

To train the agent yourself, run training.ipynb. In the same notebook you can also load the pre-trained weights and watch the agents solve the task.