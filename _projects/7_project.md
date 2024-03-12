---
layout: page
title: Optimized Path Planning for Ground Robots:A Trajectory Library based Local Planner for Unstructured Environments
description: A robust local planner to navigate unstructured and complex environments
img: assets/img/pathplanner.png
importance: 1
category: Research
# related_publications: einstein1956investigations, einstein1950meaning
---

Navigating in cluttered environments presents significant challenges for autonomous systems due to the complex and dynamic nature of the surroundings.In this work, we implement a trajectory-library-based local planner specifically designed for high-speed, non-holonomic autonomous ground robots. Leveraging pre-generated motion primitives derived from the kinematic bicycle model (KBM), our planner is able to adeptly navigate through cluttered environments .
Within our methodology, pre-generated paths are overlaid onto a grid, which is then convolved with the obstacle map to remove paths that run through obstacles.The planner evaluates and scores the remaining trajectories, selecting the optimal path with minimal cost. This approach enables obstacle avoidance and trajectory selection within a timeframe of under 11 milliseconds. 
To validate our approach,we conducted thorough experiments, testing our methodology in simulations using Gazebo and in real-world scenarios with an RC car, to confirm its effectiveness.
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
    <div class="col-sm mt-3 mt-md-3">
        {% include figure.html path="assets/img/corres_green.png"  title="example image" class="rounded mx-auto d-block" %}
    </div>
    <div class="col-sm mt-3 mt-md-3">
        {% include figure.html path="assets/img/corres_red.png"  title="example image" class="rounded mx-auto d-block" %}
    </div>
</div> 
<div class="caption">
    The generated grid is overlayed on the obstacle map to cancel out paths
</div>


<br>
**Results and Comparison at Different Speeds :**<br>
The trajectory library outperforms Fast Likelihood-based Collision Avoidance (FALCO) overall in terms of success rate in performance, average directional error, enhancing responsiveness, and average cross-track error.

In terms of success rates,the trajectory library demonstrates superior success rates in executing turns at different speeds compared to FALCO.

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/graph1.png"  title="2m/s" class="rounded mx-auto d-block" %}
    </div>
    <div class="col-sm mt-3 mt-md-3">
        {% include figure.html path="assets/img/graph2.png"  title="4m/s" class="rounded mx-auto d-block" %}
    </div>
        <div class="col-sm mt-3 mt-md-6">
        {% include figure.html path="assets/img/graph3.png"  title="6m/s" class="rounded mx-auto d-block" %}
    </div>
</div> 
<div class="caption">
    Trajectory library's success rate while making turns in comparison to FALCO
</div>

At higher speeds, the trajectory library exhibits reduced directional error compared to FALCO.

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-3">
        {% include figure.html path="assets/img/direc_4.png"  title="4m/s" class="rounded mx-auto d-block" %}
    </div>
        <div class="col-sm mt-3 mt-md-6">
        {% include figure.html path="assets/img/direc_6.png"  title="6m/s" class="rounded mx-auto d-block" %}
    </div>
</div> 
<div class="caption">
    Comparison of directional error between the trajectory library and FALCO
</div>

At higher speeds, the iLQR controller excels in tracking the paths provided by the trajectory library over FALCO
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-3">
        {% include figure.html path="assets/img/cte_4.png"  title="4m/s" class="rounded mx-auto d-block" %}
    </div>
        <div class="col-sm mt-3 mt-md-6">
        {% include figure.html path="assets/img/cte_6.png"  title="6m/s" class="rounded mx-auto d-block" %}
    </div>
</div> 
<div class="caption">
    Comparing the cross track error of the iLQR controller while tracking paths generated by the trajectory library and FALCO
</div>