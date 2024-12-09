---
layout: archive
title: "Reinforcement Learning Based UAV Collision Avoidance"
permalink: /projects/project2/
author_profile: false
---

{% include base_path %}

Clarification: This was modified from a proejct that I was responsible for at CERLAB, and later modified and used for 16833 course project. Some contents below are from the final report of that project, written by Xinming Han and Ziyi Zhang and Ye Jin

Nowaday, in a lot of scenarios, UAVs can be used. However, UAVs are very easy to break and vulnerable to collision. Therefore, collision avoidance algorithms are very important. DQN, DDQN, D3QN are some very popular reinforcement learning based algorithms,and can be helpful in learning complex models like collision avoidance.

<img src="/images/Project_2/fig1.png" alt="Example" style="width:80%; height:auto; display:block; margin:auto;">
<!-- ![p2f1](/images/Project_2/fig1.png) -->
As shown in Figure 1., the drone is firstly at its respawn location. Its goal is to go along the positive x direction, and avoid any obstacle before reaching the final x plane. If the drone hits an obstacle or reaches the setup x plane, it will be respawned. The reward is proportional to x-displacement in each step. However, if a negative x-displacement happens, there will be an extra small penalty other than the negative reward proportional to the displacement. Similarly, if the x-displacement is positive but too small, a small penalty (a little smaller than the situation when x-displacement is negative) is given. That is to encourage the algorithm to faster learn the best way of acting by penalizing the actions that are not good enough. A very large negative reward will be given if a collision happens. Collision detection range and allowed action space are shown on Figure 2. and Figure 3.
<!-- ![p2f2&3](/images/Project_2/fig2&3.png) -->
<img src="/images/Project_2/fig2&3.png" alt="Example" style="width:80%; height:auto;">

The result on Figure 5. shows a general trend of going farther before collision as the training goes.The result itself does not really converge, but generally DQN has the slowest increasing trend in its performance, its trend is more stable than DDQN and D3QN. DDQN and D3QN training results are very similar. Generally, these algorithms all learnt collision avoidance, though with different performance.
<img src="/images/Project_2/fig5.png" alt="Example" style="width:60%; height:auto;">
<!-- ![p2f5](/images/Project_2/fig5.png) -->