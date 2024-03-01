---
layout: page
title: Controlling a wheeled double pendulum robot
description: Devising control strategies for a wheeled double pendulum robot
img: assets/img/wheeled.png
importance: 6
---

<div class="row justify-content-sm-center">
     <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Figure_1.png" title="example image" class="img-fluid rounded z-depth-1"  %}
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