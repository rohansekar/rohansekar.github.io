---
layout: page
title: A move-out-of-the-way algorithm for a heterogeneous multi-robot system
description: A robust multi-agent planning algorithm to avoid collisions between robots.
img: assets/img/robots.jpg
importance: 4
category: Research
# related_publications: einstein1956investigations, einstein1950meaning
---

The primary objective of this task was to develop a robust algorithm to move a stationary robot out of the way to stand close to the nearest obstacle when an approaching robot is detected. This ensures that there are no deadlocks or collisions between the robots and allows the approaching robot to maintain its speed without having to slow down for the stationary robot, ensuring uninterrupted movement.

This is achieved by broadcasting the positions of all robots in the system, giving each robot access to the locations of all other robots. If the distance between two robots is less than 0.5 meters, the robot with the lower speed moves out of the way, opposite to the approaching direction, and stands close to the nearest obstacle in that direction. The robots used for this task were RC cars and Spot by Boston Dynamics.

<br>
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/robots.jpg"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div> 
<div class="caption">
    The robots used to demonstate move out of the way.
</div>
