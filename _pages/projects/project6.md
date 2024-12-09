---
layout: archive
title: "Dynamic System Analysis"
permalink: /projects/project6/
author_profile: false
---

{% include base_path %}

Clarification: This is a course project from a control course at Rutgers University.

Abstract:
	In this project we study a mechanical system which can be modeled as a set of ordinary differential equations. Our goal is to understand the system’s response to a given input. We created a free body diagram of the system, found its transfer function using a laplace transform, and created a Signal Flow Diagram to describe the system more simply. We found that the behavior of the system can be mathematically modeled, and that it is possible to simplify its inner workings down in a clear and concise manner using a signal flow diagram.

Introduction:
	To study the behavior of a mechanical system, we can model it as a series of signals and responses. For this project we analyzed a mechanical system of two masses undergoing torque while connected to a system of springs and dampers. To study this system we will create a free body diagram, from which we will extrapolate the differential equations which we can then use to analyze the system. We can then perform a laplace transform and obtain a transfer function to describe mathematically how the system reacts to a given input. This will allow us to solve for A1(s), B1(s), C1(s), and D1(s). We will then use our free body diagrams and our results from the previous section to create a signal flow diagram. From this diagram we can use Mason’s Gain formula to find A2(s), B2(s), C2(s).  

Theory:
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

Differential equations of two bodies can be obtained from the free body diagrams.

Reference:
[1] G.F. Franklin, J.D. Powell, and A. Emami-Naeini, Feedback Control of Dynamic Systems, Eighth Edition, Pearson Education, Inc., 2019.