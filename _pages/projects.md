---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Carnegie Mellon University, Visual and Tactile SLAM (Group Project)
======
Clarification: There are contents from our project final paper, by Hung-Jui Huang, Anoop Bhat, Jiarui Chang, Xinming Han.

The precise 3D reconstruction of small objects is important since it enables advanced analysis across scientific disciplines. Fields including geology, biology, and archaeology rely on accurate 3D models of items like seeds, artifacts, and microfossils to conduct in-depth research. For example, reconstructing the detailed morphology of a seed facilitates the study of associated plant evolution. Similarly, precise 3D imaging of ancient artifacts allows more comprehensive anthropological and historical investigations of past cultures. Beyond basic science, robotics also stands to benefit from accurate small object reconstruction and pose estimation for complex manipulation tasks like assembly or high-precision insertion.

We leverage a multimodal approach combining RealSense depth images and GelSight images to enable robust 3D reconstruction and pose estimation during sensor rolling motions. Neural networks are trained to process tactile and visual data to output odometry for tracking touch poses over time. Another neural network detects loop closures to refine the pose estimates. These pose estimates are integrated into a pose graph optimization framework using GTSAM to produce optimal touch trajectories. The local 3D reconstructions from the tactile images are then combined according to the estimated poses to generate the full 3D model.

As shown from Fig.13 to Fig.16 predicted and ground truth tactile odometry and visual odometry are used separately to do GTSAM pose optimization. In the tactile odometry result, there is some drift from the ground truth, but the rough pattern of going back and forth can still be seen from it. However, the optimization using visual odometry does not perform as well. From the ground truth, there is a clear pattern of going back and forth. However, by looking at the visual odometry optimization result, it is impossible to tell the original movement pattern. As a side note, in our initial implementation, we used Rodrigues vectors to parameterize the orientation in the optimization. We also tried using yaw-pitch-roll angles, but they yielded a similar result.

GTSAM optimization does not perform well for visual odometry, and that can only be solved by obtaining better visual odometry. For tactile odometry, there is still drift, since we do not have loop closure constraints in the optimization. If we had a well-performing loop closure detection method, by entering the corresponding odometry between two poses that have a loop closure, we could improve the optimization's performance. We expect that after getting better performance out of the visual and tactile odometry individually and by performing loop closure using both sources of data, we can get better results from the pose graph optimization.
![p1f13](/images/Project_1/fig13.png)
![p1f14](/images/Project_1/fig14.png)
![p1f15](/images/Project_1/fig15.png)
![p1f16](/images/Project_1/fig16.png)


Reinforcement Learning Based UAV Collision Avoidance
======
Clarification: This was modified from a proejct that I was responsible for at CERLAB, and later modified and used for 16833 course project. Some contents below are from the final report of that project, written by Xinming Han and Ziyi Zhang and Ye Jin

Nowaday, in a lot of scenarios, UAVs can be used. However, UAVs are very easy to break and vulnerable to collision. Therefore, collision avoidance algorithms are very important. DQN, DDQN, D3QN are some very popular reinforcement learning based algorithms,and can be helpful in learning complex models like collision avoidance.

As shown in Figure 1., the drone is firstly at its respawn location. Its goal is to go along the positive x direction, and avoid any obstacle before reaching the final x plane. If the drone hits an obstacle or reaches the setup x plane, it will be respawned. The reward is proportional to x-displacement in each step. However, if a negative x-displacement happens, there will be an extra small penalty other than the negative reward proportional to the displacement. Similarly, if the x-displacement is positive but too small, a small penalty (a little smaller than the situation when x-displacement is negative) is given. That is to encourage the algorithm to faster learn the best way of acting by penalizing the actions that are not good enough. A very large negative reward will be given if a collision happens. Collision detection range and allowed action space are shown on Figure 2. and Figure 3.

The result on Figure 5. shows a general trend of going farther before collision as the training goes.The result itself does not really converge, but generally DQN has the slowest increasing trend in its performance, its trend is more stable than DDQN and D3QN. DDQN and D3QN training results are very similar. Generally, these algorithms all learnt collision avoidance, though with different performance
![p2f1](/images/Project_2/fig1.png)
![p2f2&3](/images/Project_2/fig2&3.png)
![p2f5](/images/Project_2/fig5.png)

Internal Combustion Engine Laboratory
======
Clarification: This is a course project from a control course at Rutgers University.

![p3](/images/Project_3/Project_3.png)
 
Project 4
======
Clarification: This is a course project from a control course at Rutgers University.

Abstract
	In this project we study a mechanical system which can be modeled as a set of ordinary differential equations. Our goal is to understand the system’s response to a given input. We created a free body diagram of the system, found its transfer function using a laplace transform, and created a Signal Flow Diagram to describe the system more simply. We found that the behavior of the system can be mathematically modeled, and that it is possible to simplify its inner workings down in a clear and concise manner using a signal flow diagram.

Introduction
	To study the behavior of a mechanical system, we can model it as a series of signals and responses. For this project we analyzed a mechanical system of two masses undergoing torque while connected to a system of springs and dampers. To study this system we will create a free body diagram, from which we will extrapolate the differential equations which we can then use to analyze the system. We can then perform a laplace transform and obtain a transfer function to describe mathematically how the system reacts to a given input. This will allow us to solve for A1(s), B1(s), C1(s), and D1(s). We will then use our free body diagrams and our results from the previous section to create a signal flow diagram. From this diagram we can use Mason’s Gain formula to find A2(s), B2(s), C2(s).  

Theory：
	The Mechanical System being studied is shown below, from this we can create our free body diagram. It is important to note for the purposes of our analysis that initial conditions are set to 0, and 1>2:
  ![p4f1](/images/Project_4/fig1.png)

The functions A1(s), B1(s), C1(s), D1(s) can be solved by performing laplace transforms on the differential equations created from the free body diagram and rearranging into the form below:
A1(s), B1(s), C1(s), D1(s):
![p4f2](/images/Project_4/fig2.png)

Additionally, the functions A2(s), B2(s), C2(s), can be solved for by using Mason's Gain formula on our signal flow diagrams, and rearranging into the form shown below:


Mason’s Gain Formula:
![p4f3](/images/Project_4/fig3.png)



A2(s), B2(s), C2(s):
![p4f4](/images/Project_4/fig4.png)



The mathematics and results of this process can be seen in the next section.

Results:
Free body 
![p4f5](/images/Project_4/fig5.png)

Differential equations of two bodies can be obtained from the free body diagrams. ̇̇̈̈̈


Reference
[1] G.F. Franklin, J.D. Powell, and A. Emami-Naeini, Feedback Control of Dynamic Systems, Eighth Edition, Pearson Education, Inc., 2019.


Project 5
======
* 1
* 2
* 3

Project 6
======
* 1
* 2
* 3




<!-- Project 1
======
* 1
* 2
* 3

Project 2
======
* 1
* 2
* 3

Project 3
======
* 1
* 2
* 3

Project 4
======
* 1
* 2
* 3

Project 5
======
* 1
* 2
* 3

Project 6
======
* 1
* 2
* 3 -->
