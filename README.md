<h1>Udacity Deep Reinforcement Learning Nanodegree</h1>
  
<h2>Collaboration and Competition</h2>

<h3>1. Project Description</h3>

The current project attempts to solve a task using a value-based model-free and off-policy deep reinforcement learning algorithm that uses a neural network to decide on which actions to take in its environment.

The task consists of two agents that need to learn how to bounce a ball over a net. The environment provides a reward of +0.1 if an agent is able to hit the ball over the net, and a punishment of -0.01 if an agent lets the ball fall into the ground or hits the ball off the playing field.

The goal of each agent is therefore to cooperate and keep the ball at play during the available time-steps in a given episode so as to maximise the total episodic reward.

<h3>2. Environment</h3>

An adapted version of the Tennis environment available in Unity ML-Agents GitHub page is used in this project. Observation states are composed 3 frames each composed of 8 variables corresponding to the position and velocity of the ball and racket within the environment.

The action space is composed of a vector with 2 continuous variables which correspond to the agent’s movement towards/away from the net and jumping. Each variable is a real number between -1 and 1.

Each episode’s score is obtained by selecting the maximum score from the set total scores of both agents. The task is considered solved when the average score obtained over 100 consecutive episodes is greater than 0.50.

<h3>3. Implementation</h3>

The learning process uses the Multiple Agent Deep Deterministic Policy Gradient (MADDPG) reinforcement learning algorithm (Lowe et al., 2018) which, although not a pure actor-critic algorithm, does use an actor to retrieve actions to use in a given local state and a centralised critic to evaluate such state-action pairs. Both the actor and critic are implemented as neural networks using the Pytorch library. Each agent has an independent actor and critic neural network.

<h3>4. Running the Code</h3>
To run the code simply download the available files to a folder, open the Jupyter Notebook and select "Kernel -> Restart & Run All".

<h3>5. Dependencies</h3>
Python 3.6, Numpy 1.15.1, Pytorch 0.4.0, UnityEnvironment.

<h3>6. Credits</h3>
The baseline implementation of the DDPG algorithm was taken from here https://github.com/higgsfield/RL-Adventure-2. It was so elegantly implemented that we just had to use it :-)
