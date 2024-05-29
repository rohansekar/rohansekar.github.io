---
layout: page
title: Master's Thesis:A Trajectory Library-Based Local Planner for Ground Robots in Unstructured Environments
description: A robust local planner to navigate unstructured and complex environments
img: assets/img/path_pc.png
redirect: https://drive.google.com/file/d/1mvF6ClwuVw1otDfKOzk5C149VQME2Mf9/view?usp=drive_link
importance: 1
category: Research
---

Navigating in cluttered environments presents significant challenges for autonomous systems. Although finding the shortest path from a start to a goal location is a well-addressed problem, as robots traverse this path, they encounter numerous unforeseen obstacles that are not accounted for in the initial global plan.  These obstacles are dynamic in nature, making it difficult to establish a reliable path over time. Several works like A* and RRT generate real-time plans for robots as they navigate through an environment but often fail to incorporate the dynamics involved. In this work, we introduce a trajectory-library-based local planner designed for high-speed, non-holonomic autonomous ground robots. This planner not only adeptly navigates the dynamic challenges of the environment but also accounts for the dynamics of the robot.
In this trajectory-library-based local planner, the knowledge of the robot's dynamics is leveraged to generate trajectories at varying speeds. These pre-computed trajectories are then overlaid onto a grid while also considering the robot's footprint. This grid is then convolved with the obstacle map, effectively filtering out any paths that intersect with obstacles. This streamlined collision-checking process is executed in less than two milliseconds, facilitating rapid decision-making. To validate our approach, we tested our methodology both in simulated environments using Gazebo and through practical trials with an RC car in real-world scenarios.
<br>
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/pathplanner.png"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/path_pc.png"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div> 
<div class="caption">
    The trajectory-library navigating through the cluttered environment
</div>
**Path Generation**:<br>
The paths were generated using the kinematic bicycle model(KBM) and are kindoynamically feasible paths.


<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/pathss.png"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div> 
<div class="caption">
    The generated paths using the KBM model
</div>

**Correspondence Generation**:<br>

* The generated paths are overlaid on a grid,which is then convolved with the obstacle map for collision checking.
* The robot’s footprint is accounted for in this step.
* This makes the overall process computationally cheap and can run seamlessly on real robots.

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/corres_green.png"  title="example image" class="rounded mx-auto d-block" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/corres_red.png"  title="example image" class="rounded mx-auto d-block" %}
    </div>
</div> 
<div class="caption">
    The generated grid is overlayed on the obstacle map to cancel out paths
</div>


<br>
**Results and Comparison at Different Speeds :**<br>
The trajectory library outperforms Fast Likelihood-based Collision Avoidance (FALCO)[1] overall in terms of success rate in performance, average directional error, enhancing responsiveness, and average cross-track error.

In terms of success rates,the trajectory library demonstrates superior success rates in executing turns at different speeds compared to FALCO.

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/graph1.png"  title="2m/s" class="rounded mx-auto d-block" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/graph2.png"  title="4m/s" class="rounded mx-auto d-block" %}
    </div>
        <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/graph3.png"  title="6m/s" class="rounded mx-auto d-block" %}
    </div>
</div> 
<div class="caption">
    Trajectory library's success rate while making turns in comparison to FALCO
</div>

At higher speeds, the trajectory library exhibits reduced directional error compared to FALCO.

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/direc_4.png"  title="4m/s" class="rounded mx-auto d-block" %}
    </div>
        <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/direc_6.png"  title="6m/s" class="rounded mx-auto d-block" %}
    </div>
</div> 
<div class="caption">
    Comparison of directional error between the trajectory library and FALCO
</div>

At higher speeds, the iLQR controller excels in tracking the paths provided by the trajectory library over FALCO
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/cte_4.png"  title="4m/s" class="rounded mx-auto d-block" %}
    </div>
        <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/cte_6.png"  title="6m/s" class="rounded mx-auto d-block" %}
    </div>
</div> 
