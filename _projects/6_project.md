---
layout: page
title: Controlling a wheeled double pendulum robot
description: Devising control strategies for a wheeled double pendulum robot
img: assets/img/wheeled.png
importance: 1
category: Robotics
---

Wheeled pendulum systems can be found across society, such as in transportation systems like the Segway and in self-balancing robots. As these types of technologies become more commonplace in our daily lives, it is important to find control strategies that maintain their stability under disturbances to ensure the safety of human operators and bystanders. Although researchers have previously modeled wheeled inverted pendulum systems, there is little work explaining wheeled double pendulum systems, which could represent a human carrying a payload while on a Segway. This report discusses several control strategies -- including PID, LQR, and input shaping -- to stabilize a wheeled double pendulum and prevent oscillations in the upper pendulum. After modeling the system using Lagrangian mechanics, controllers and an observer were designed in MATLAB and simulated in both Simulink and Simscape to compare performance in tracking point-to-point trajectories. Additionally, an Elegoo Tumbller self-balancing robot was modified to include a second pendulum to test these controllers on hardware. While the PID and LQR controllers were able to stabilize the system, prevent oscillations, and follow trajectories both in simulation and hardware, the upper pendulum minimally oscillated due to friction on its pivot point in the physical system. 

Some of the results that were got with the PID and LQR controllers are:

<div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/wheeled11.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
</div>

<div class="caption">
    Following the minimum jerk trajectory with LQR
</div>

<div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/wheeled2.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
</div>

<div class="caption">
    PID following a sine wave
</div>

For more information,read our report:<br>
https://drive.google.com/file/d/1EzeNNdNugV0EUZQofzTWvP74nE7-yNlV/view?usp=drive_link