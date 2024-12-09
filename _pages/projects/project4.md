---
layout: archive
title: "Reinforcement Learning (PPO) Based UAV Collision Avoidance and Navigation"
permalink: /projects/project4/
author_profile: false
---

{% include base_path %}


Clarification: This is a C++ course group project. I was responsible for dealing with bouncing when the human character touches an obstacle, and writing the difficulty class that provided other members a difficulty level interface.

Nowadays, there are a lot of Triple A games, which require a powerful GPU. And some of them even run slow when you have a RTX 4090 because of poor optimization. However, C++ based programs can run pretty fast, and we thought that fast, convenient, but still funny game can still atttract a lot of players. Those busy students or people do not have a GPU can be our potential customers.

We used C++ to wrote this program. The goal is to reach a final goal in the map, with as few number of collisions as possible, and try to make the color same as the goal entrance. Scoring system with calculate the score based on these criterias. Player can simply use left and right key to rotate the human. If feet touch wall, human will be bounced to the direction where his head points to. If head touches wall, the reflection angel will be equal to the angle of incidence, like the reflection of light on a flat surface. The visualized game design is explained in the figure below.
<img src="/images/Project_6/fig1.png" alt="Example" style="width:80%; height:auto; display:block; margin:auto;">  

The game run without problem on Ubuntu, Windows, and Mac. It is pretty fast, computationally cheap, funny. We have tested different levels of difficulty, and thought the levels design is reasonable, which meant "Easy" is esay, and "Hard" is challenging. Below is a demo of our game.

<video width="640" height="360" controls>
  <source src="/images/Project_6/demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

Future work will be debugging the game furthurmore, since we still observe some problems when the character hit the wall with a certain angle sometimes.
