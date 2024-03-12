---
layout: page
title: Decentralized and Centralized Behavior Trees for Heterogenous Robotic Systems
description: Deploying decentralized and centralized behavior trees for complex robotic systems to attain increased modularity
img: assets/img/bt_1.png
importance: 1
category: Research
# related_publications: einstein1956investigations, einstein1950meaning
---

Behavior trees are hierarchical structures used in artificial intelligence and robotics to model the behavior of agents in complex environments. Comprising nodes representing actions, conditions, and control flow, behavior trees offer a flexible and intuitive framework for designing reactive and goal-oriented behaviors. In this work, both centralized and decentralized frameworks of the behavior tree were implemented. This was achieved by integrating the BehaviorTree.CPP library with our multi-robot system.

**The centralized behavior tree**:<br>
The centralized behavior tree runs on a base station, commanding individual robots on their tasks according to user input. This behavior tree dynamically incorporates the robots in the system and creates publisher maps for all the features present. In this way, individual commands can be sent to each robot from a remote computer.
<br>
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/bt_1.png"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div> 
<div class="caption">
    The centralized behavior tree structure
</div>

<video controls="" width="320" height="240" muted="" loop="" autoplay="">
<source src="./assets/video/BehaviorTrees.mp4" type="video/mp4">
</video>

<div class="caption">
    Working of the centralized behavior tree in real-time
</div>

**The decentralized behavior tree**:<br>

The decentralized behavior tree runs on the robot,which means that we can have different behavior trees for different types of robots.This also ensures that the computational load on the basestation is reduced.Additionally,this also ensures that any communication delays between the operator and the robot does not come in the way of choosing a mode.
<br>
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/bt_1.png"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div> 
<div class="caption">
    The decentralized behavior architecture
</div>

<video src="assets/video/BehaviorTrees.mp4" width="320" height="240" controls></video>

<div class="caption">
    Working of the centralized behavior tree in real-time
</div>


**References**:<br>

[1]https://www.behaviortree.dev/