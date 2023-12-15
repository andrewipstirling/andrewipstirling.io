---
layout: default
title: Reinforcement Learning for Inverted Pendulum Control
---

Control theory, is centered around the behaviour of dynamic systems, and how as
engineers we can force it to behave in a certain way. In the context of Mechanical Engineering, these systems could vary from robotics, to automotive systems, to aerospace and HVAC applications. A large portion of Control design is spent modelling the system or "plant". This requires a good grasp of the system's mechanics, understanding all variables that may influence its behaviour. For complex systems, these dynamics are highly non-linear, while exhibiting large degrees of freedom. In such applications, traditional control techniques may struggle to produce reliable and accurate behaviour. Moreover, we may not even be able to model the system, making any form of controller design impossible. 

In these cases, we can make use of Reinforcement Learning (RL) for controlling such complex systems. RL operates in a model-free fashion, meaning we are not required to have an explicit model of a system's behaviour given various inputs. Using RL, we can effectively sidestep all the disadvantages of model-based controller design. RL generally consists of an agent who, through interacting with an environment, can learn to map various situations to actions. Specifically, the environment provides responses to each a agent's action, using these responses and rewards dependent on various states of the agent, we can condition the agent's decisions towards optimal states. In class, the problems we solved required the action and/or the state to be discretizable. However, for continuous systems, this may not be possible or if it is, it raises the question to what resolution we look to discretize the space or actions. The Soft Actor-Critic architecture is a form of RL that looks to solve this problem. 

In this project, we look to investigate RL's applications and performance in control settings. Specifically, we look to investigate the Soft Actor-Critic (SAC) architecture's ability to control a continuous system, consisting of an inverted pendulum on a cart. With random controll inputs, we can see the Pendulum falls nearly immediately, and we must seek to how keep it upright using Reinforcement Learning.

<video width="640" height="360" controls>
  <source src="assets/no_control.mp4" type="video/quicktime">
  Your browser does not support the video tag.
</video>

### Project

This project implements the SAC framework from https://github.com/openai/spinningup, for the inverted pendulum in the gymnasium environment found at https://github.com/Farama-Foundation/Gymnasium. The final presentation can be found in the *soft_actor_critic.ipynb* notebook of my repository at https://github.com/andrewipstirling/sac_inverted_pendulum, with all code in the relevant files. Upon completion, I was able to obtain succesful control of the pendulum, as can be seen below. 

<video width="640" height="360" controls>
  <source src="assets/trained_alpha02.mp4" type="video/quicktime">
  Your browser does not support the video tag.
</video>
