# RL

# Introduction 

This task is about the following:

Your goal is to train a reinforcement learning (RL) agent to perform a specific task using the deep Q-learning (DQN) algorithm. The project will be in groups of 3.

## Details:

Choose an environment (eg. game, robot, ..., etc.).
Load the environment in gym.
Perform the necessary modification to the environment using gym wrappers.
Implement the DQN algorithm from scratch.
Train your agent using your DQN implementation.
Evaluate the performance of your agent.
Deliverables:
Colab Notebook.
Project Documentation within the notebook, including a detailed description of the environment (eg. observation space, action space, reward, ..., etc.), the task the agent needs to learn, your detailed implemented algorithm, and your results (training reward, evaluation mean reward and std, and a video preview of the agent after training).

## Notes:

The environment must be different from the examples shown in the lectures. It should be complex enough to justify using DQN instead of a simple Q-learning algorithm.
You can import an already implemented env or implement your own from scratch using gym custom environments.
Pay attention to your choice of network architecture and justify it in your documentation.
Train several agents and show their variance.

## Extra Credits:
Train your agent using another RL algorithm and compare it with DQN.

# Ms Pacman

![image](https://user-images.githubusercontent.com/101316217/211210252-a1c83cd9-4318-44cc-bc13-d128ec71490a.png)

This environment is part of the https://www.gymlibrary.ml/environments/atari/. Please read that page first for general information.

Action Space Discrete(18)

Observation Space (210, 160, 3)

Observation High 255

Observation Low 0

Import gym.make("ALE/MsPacman-v5")

## Description

Your goal is to collect all of the pellets on the screen while avoiding the ghosts.

## Actions

By default, all actions that can be performed on an Atari 2600 are available in this environment. However, if you use v0 or v4 or specify full_action_space=False during initialization, only a reduced number of actions (those that are meaningful in this game) are available. The reduced action space may depend on the flavor of the environment (the combination of mode and difficulty). The reduced action space for the default flavor looks like this:

Num Action

0 NOOP

1 UP

2 RIGHT

3 LEFT

4 DOWN

5 UPRIGHT

6 UPLEFT

7 DOWNRIGHT

8 DOWNLEFT

## Observations

By default, the environment returns the RGB image that is displayed to human players as an observation. However, it is possible to observe

The 128 Bytes of RAM of the console

A grayscale image

instead. The respective observation spaces are

Box([0 ... 0], [255 ... 255], (128,), uint8)

Box([[0 ... 0] ... [0 ... 0]], [[255 ... 255] ... [255 ... 255]], (250, 160), uint8)

respectively. The general article on Atari environments outlines different ways to instantiate corresponding environments via gym.make.

## Arguments
env = gym.make("ALE/MsPacman-v5") The various ways to configure the environment are described in detail in the article on Atari environments.

## Environment

Valid Modes

Valid Difficulties

Default Mode

MsPacman

[0, ..., 3]

[0]

0

You may use the suffix “-ram” to switch to the RAM observation space. In v0 and v4, the suffixes “Deterministic” and “Noframeskip” are available. These are no longer supported in v5. In order to obtain equivalent behavior, pass keyword arguments to gym.make as outlined in the general article on Atari environments. The versions v0 and v4 are not contained in the “ALE” namespace. I.e. they are instantiated via gym.make("MsPacman-v0")

## Version History


A thorough discussion of the intricate differences between the versions and configurations can be found in the general article on Atari environments.

v5: Stickiness was added back and stochastic frameskipping was removed. The entire action space is used by default. The environments are now in the “ALE” namespace.

v4: Stickiness of actions was removed

v0: Initial versions release (1.0.0)


## Deep Q-network

python implementation of Deep Q Networks using Keras and OpenAI gym. This program learns to play MsPacman. With very little change it could be made to learn just about any other Atari game.

The Q-networks has 3 convolutional layers and fully connected layers .

The agent learns to play the MsPacman-v0 Gym environment.
