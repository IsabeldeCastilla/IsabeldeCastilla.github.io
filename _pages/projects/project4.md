---
layout: archive
title: "Reinforcement Learning (PPO) Based UAV Collision Avoidance and Navigation"
permalink: /projects/project3/
author_profile: false
---

{% include base_path %}


Clarification: This is from my research project. I was responsible for training in Isaac Sim simulator, finetuning the model and reward functions, designing training environments for dynamic obstacle avoidance, and performing experiments. Some contents are from our paper written by Zhefan Xu, Xinming Han, Haoyu Shen, Hanyu Jin, and Kenji Shimada.

Nowadays, in a lot of scenarios, UAVs can be used. For example, disaster response, construction site monitoring, and bridge maintenance can all be made much easier by using UAV. However, UAVs are very easy to break and vulnerable to collision. Therefore, collision avoidance algorithms are very important. In recently years, applying reinforcement learning in robotics shows a great potential, and PPO is a very popular and efficient reinforcement learning algorithm. Our framework aims to enhance UAV safety, making them more reliable for different tasks.

Our navigation framework is described in Fig. 2. The obstacle perception system processes RGB-D images and robot states to generate representations for both static and dynamic obstacles. Obstacle representations are then converted into network input states, along with the definitions of robot actions and training rewards. During training, we employ the PPO algorithm with an actor-critic network structure to train the policy and value networks. For deployment, a safety shield is applied to the RL policy network’s action outputs to ensure safety. We also applied a parallel training pipeline in Isaac Sim to speed up the training.
<img src="/images/Project_5/fig2.png" alt="Example" style="width:80%; height:auto; display:block; margin:auto;">  

Results from simulation and physical experiments verify the effectiveness of our approach in achieving safe navigation within dynamic environments. The video below is our physical experiments, which show that our algorithm perform quite well in real deployment.

<iframe width="560" height="315" src="https://youtu.be/fhRxS--Rhkc?si=XKpAqg7QXRvD259P" 
title="UAV Collision Avoidance Experiments" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Future work will focus on improving and adapting this framework for deployment across various robotic platforms. Currently, we found that it can be helpful to improve the frequency of this framework. This might be done by reducing the computation or using a more powerful computer.
