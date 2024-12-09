---
layout: archive
title: "Visual and Tactile SLAM"
permalink: /projects/project1/
author_profile: false
---

{% include base_path %}

Clarification: There are contents from our project final paper, by Hung-Jui Huang, Anoop Bhat, Jiarui Chang, Xinming Han.

<!-- The precise 3D reconstruction of small objects is important since it enables advanced analysis across scientific disciplines. Fields including geology, biology, and archaeology rely on accurate 3D models of items like seeds, artifacts, and microfossils to conduct in-depth research. For example, reconstructing the detailed morphology of a seed facilitates the study of associated plant evolution. Similarly, precise 3D imaging of ancient artifacts allows more comprehensive anthropological and historical investigations of past cultures. Beyond basic science, robotics also stands to benefit from accurate small object reconstruction and pose estimation for complex manipulation tasks like assembly or high-precision insertion. -->

We leverage a multimodal approach combining RealSense depth images and GelSight images to enable robust 3D reconstruction and pose estimation during sensor rolling motions. Neural networks are trained to process tactile and visual data to output odometry for tracking touch poses over time. Another neural network detects loop closures to refine the pose estimates. These pose estimates are integrated into a pose graph optimization framework using GTSAM to produce optimal touch trajectories. The local 3D reconstructions from the tactile images are then combined according to the estimated poses to generate the full 3D model.

As shown from Fig.13 to Fig.16 predicted and ground truth tactile odometry and visual odometry are used separately to do GTSAM pose optimization. In the tactile odometry result, there is some drift from the ground truth, but the rough pattern of going back and forth can still be seen from it. However, the optimization using visual odometry does not perform as well. From the ground truth, there is a clear pattern of going back and forth. However, by looking at the visual odometry optimization result, it is impossible to tell the original movement pattern. As a side note, in our initial implementation, we used Rodrigues vectors to parameterize the orientation in the optimization. We also tried using yaw-pitch-roll angles, but they yielded a similar result.

GTSAM optimization does not perform well for visual odometry, and that can only be solved by obtaining better visual odometry. For tactile odometry, there is still drift, since we do not have loop closure constraints in the optimization. If we had a well-performing loop closure detection method, by entering the corresponding odometry between two poses that have a loop closure, we could improve the optimization's performance. We expect that after getting better performance out of the visual and tactile odometry individually and by performing loop closure using both sources of data, we can get better results from the pose graph optimization.  
<img src="/images/Project_1/fig13.png" alt="Example" style="width:40%; height:auto;">
<img src="/images/Project_1/fig14.png" alt="Example" style="width:40%; height:auto;">
<img src="/images/Project_1/fig15.png" alt="Example" style="width:40%; height:auto;">
<img src="/images/Project_1/fig16.png" alt="Example" style="width:40%; height:auto;">  
<!-- ![p1f13](/images/Project_1/fig13.png) -->
<!-- ![p1f14](/images/Project_1/fig14.png)
![p1f15](/images/Project_1/fig15.png)
![p1f16](/images/Project_1/fig16.png) -->