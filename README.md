# AEC2023-Non-Static-Environments-with-Autonomous-Drones

Repository of EUCASS-CEAS 2023 Conference Paper

## Title 
**Navigation in Non-Static Environments with Autonomous Drones: A Kalman Filter Reinforcement Learning Approach**

**Conference**: [EUCASS-CEAS 2023](https://eucass-ceas-2023.eu/)

**Date**: 09-13 July 2023

## Introduction
This webpage provides a succinct overview and illustrative representations pertaining to the paper mentioned in the title. View this page as a supplemental resource that complements the original publication.

## Abstract 
Autonomous drone systems have grown in various industries, but their effectiveness in dynamic environments remains challenging. This study addresses the issues faced in path planning and state estimation for drones operating in non-static environments. To tackle these challenges, a solution combining Kalman Filters and Advanced Reinforcement Learning (RL) Algorithms is proposed. Three RL algorithms are compared to evaluate their performance. Combining the Kalman Filter and RL techniques improves path planning and decision-making, resulting in successful navigation in simulated dynamic scenarios. The approach is designed for continuous state-action environments.

## Methodology
Our methodology utilized a 3D simulation environment to recreate realistic drone scenarios and implemented three reinforcement learning algorithms: Deep Deterministic Policy Gradient (DDPG), Soft-Actor Critic (SAC), and Proximal Policy Optimization (PPO). These algorithms were trained and tested on path planning and state estimation within the simulation. Their performance was then analyzed and compared. The integration of the Kalman Filter, a state estimation technique, with these algorithms aimed to enhance drone decision-making and adaptability to dynamic environments.


## Experiment Results
In our research, we employ three main criteria to evaluate the performance of the reinforcement learning algorithms: cumulative score per episode, the count of episodes in which the agent accomplished the objective, and the duration per episode (episode elapsed). These criteria can be further divided into five metrics defined as follows: 

- Cumulative Score Per Episode: The cumulative score per episode directly measures the agent's performance in its assigned task. Superior scores suggest that the agent optimizes its actions to fulfill its objective.
- Count of Episodes to Accomplish the Objective: This criterion assesses the agent's learning proficiency. An agent that reliably accomplishes the objective in fewer episodes proves to be quicker in resolving the task and adaptation to the environment.
- Duration per Episode (episode elapsed): By evaluating the duration spent on each episode, we can gauge the agent's computational efficiency. This becomes crucial when comparing algorithms that garner similar scores, as computational efficiency could be the deciding factor in algorithm choice.
- Average Reward per Action: The average reward per action offers a measure of the quality of the decisions made by the agent. An increased average reward per action indicates that the agent is making superior decisions, leading to higher rewards for each action. This becomes particularly noteworthy in scenarios where the agent has a limit on the number of actions it can execute in an episode or when the objective is to garner the highest reward in the least possible time or number of steps. 
This metric balances the speed (number of steps) and the quality (reward) of the actions, preventing strategies that excessively prioritize one aspect at the detriment of the other.
- Success Rate: This represents the ratio of episodes where the agent accomplishes its objective. A higher success rate indicates that the agent can more reliably complete its task. 

![Alt Text](./images/PPO_3D_70.gif)
<center>PPO Agent Navigation Animation thought gates - Episode 70</center>

![Alt Text](./images/PPO_3D_220.gif)
<center>PPO Agent Navigation Animation thought gates - Episode 220</center>

![Alt Text](./images/SAC_3D_70.gif)
<center>SAC Agent Navigation Animation thought gates - Episode 70</center>

![Alt Text](./images/SAC_3D_220.gif)
<center>SAC Agent Navigation Animation thought gates - Episode 220</center>


In all visualizations, the gates are denoted by red circles. Each gate's movement is indicated by an additional red circle. When the drone, represented by the blue line, passes through a gate, the corresponding gate is marked green.

The animation shows how the PPO is capable of predicting the gate's position and flying directly to the estimated location. On the contrary, the SAC tends to merely follow the gate, resulting in inferior performance.

## Conclusions

Our research provided significant insights into the performance of DDPG, SAC, and PPO algorithms in dynamic environments. DDPG showed limitations, especially regarding its exploration strategy in evolving scenarios. SAC, with its balance between reward maximization and action diversification, displayed rapid learning. PPO, although slower to learn, demonstrated a robust and stable performance. The Kalman filter was effectively utilized for accurate dynamic motion tracking. These findings, however, are based on simulations, and transitioning to hardware testing is a crucial future step. The upcoming research will focus on hardware-in-the-loop testing for better understanding of real-world performance and potential refinements to the algorithms. This will be complemented by efforts to improve our models to manage environmental changes more efficiently, strengthen perception capabilities, and increase system robustness.

