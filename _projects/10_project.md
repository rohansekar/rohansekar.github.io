---
layout: page
title: A move-out-of-the-way algorihtm for a heterogeneous multi-robot system
description: 
img: assets/img/robots.png
importance: 1
category: Research
# related_publications: einstein1956investigations, einstein1950meaning
---

The main objective of this task was to develop a robust algorithm to move a stationary robot out of the way to stand close to the closest obstacle when a robot in motion is approaching it. This makes sure that there are no deadlocks or collisions that are caused between the robots and this also makes sure that the approaching robot's speed does not reduce to accomodate for the stationary robot and the approaching robot can continue to move without any hindrance.
The way this is done is that the positions of all the robots in the system is broadcasted and all the robot have access to all the robots present in the system. If the distance between two robots is less than 0.5m,the robot with the lower speed moves out of the way opposite to the approaching direcion to give space to the other robot and stands close to the closest obstalce in that direction. The robots that were used for this task were RC cars and Spot by Boston Dynamics.
<br>
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/robots.png"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div> 
<div class="caption">
    The robots used to demonstate move out of the way.
</div>
