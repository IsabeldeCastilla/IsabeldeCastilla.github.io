---
layout: archive
title: "C++ Game"
permalink: /projects/project4/
author_profile: false
---

{% include base_path %}


Clarification: This is a C++ course group project. I was responsible for dealing with bouncing when the human character touches an obstacle, and writing the difficulty class that provided other members a difficulty level interface.

## Introduction
Nowadays, there are a lot of Triple A games, which require a powerful GPU. And some of them even run slow when you have a RTX 4090 because of poor optimization. However, C++ based programs can run pretty fast, and we thought that fast, convenient, but still entertaining game can still attract a lot of players. Those busy students or people do not have a GPU can be our potential customers.

## Methods
We used C++ and OpengGL to write this program. The goal is to reach a final goal in the map, with as few number of collisions as possible, and try to make the color same as the goal entrance. Scoring system with calculate the score based on these criteria. Player can simply use left and right key to rotate the human. If feet touch wall, human will be bounced to the direction where his head points to. If head touches wall, the reflection angel will be equal to the angle of incidence, like the reflection of light on a flat surface. The visualized game design is explained in the figure below.
<img src="/images/Project_4/fig1.png" alt="Example" style="width:80%; height:auto; display:block; margin:auto;">  

## Results
The game run without problem on Ubuntu, Windows, and Mac. It is fast, computationally efficient, and entertaining. We have tested different levels of difficulty, and thought the levels design is reasonable, which meant "Easy" is esay, and "Hard" is challenging. Below is a demo of our game.

<video width="640" height="360" controls>
  <source src="/images/Project_4/demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

## Discussion
Future work will be debugging the game furthermore, since we still observe some problems when the character hit the wall with a certain angle sometimes.
