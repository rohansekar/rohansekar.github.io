---
layout: page
title: Real-time Lattice Based A* Planning for RC Cars
description: Deploying an A*star based local planner
img: assets/img/astar2.png
importance: 2
category: Robotics
---


The primary focus of this project centers on the development of a local planner for an RC car.A planner has been constructed to generate kino-dynamically feasible paths, utilizing a kinematic bicycle model (KBM).The generated paths form a graph, and an A* algorithm is employed for graph search, with the euclidean distance serving as the heuristic to navigate towards the goal.Paths intersecting with obstacles are eliminated from consideration, and obstacle detection is carried out using a simulated Velodyne lidar.The selected path is executed using an iLQR (Iterative Linear Quadratic Regulator) controller.The entire implementation is tested within a simulated Gazebo world.
<div class="row justify-content-sm-center">
     <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/path.png" title="example image" class="img-fluid rounded z-depth-1"  %}
    </div>
</div> 
<div class="caption">
    The generated paths
</div>


**Results:**<br>

<div class="row justify-content-sm-center">
     <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/astar2.png" title="example image" class="img-fluid rounded z-depth-1"  %}
    </div>
</div> 
<div class="caption">
    Visualizing the A star algorithm running in real-time
</div>

The planner is tested by using an occupancy grid of the environment to check if the right path is chosen.Since the total number of paths are 50 and every path consists of 100 points, doing a large number of expansions will make the planner slow and will hinder the performance as we want the planner to run at 10Hz at all times.So in this project,we do 5 expansions and choose the best path from that.THis makes sure that the path with the least cost is chosen using A start whilst running the planner constantly at 10Hz.<br>
**Conclusion:**<br>
In conclusion, the project's successful implementation of  a lattice based A star local planner proves that best-first search algorithms can be deployed for real-time planning as long as the number of paths to evaluate is reasonable.