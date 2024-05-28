---
layout: page
title: A CI/CD pipeline for a full-scale robotic system
description: Writing test cases and setting up a CI/CD pipeline for a complex and a full-scale robotic system
img: assets/img/cicd.png
importance: 5
category: Research
# related_publications: einstein1956investigations, einstein1950meaning
---

Large systems consist of many moving parts and require meticulous maintenance, particularly in terms of software engineering practices. To ensure consistency and reliability, a Continuous Integration/Continuous Deployment (CI/CD) pipeline has been implemented for all repositories associated with the project.

The CI/CD pipeline is managed using a self-hosted runner on GitHub. A common repository has been created that contains the necessary YAML files to execute commands upon push or pull requests to the master branch of any repository. This centralized approach ensures that pipeline configurations are standardized across all repositories.

The pipeline includes comprehensive test cases tailored to each repository. For code written in C++, `gtest` is utilized, while for Python code, `unittest` is used. These tests are crucial for verifying the correctness and functionality of the code before it is merged into the master branch.

Additionally, `rostest` has been integrated to facilitate the testing of ROS-based components. This integration allows for the running and verification of ROS nodes and systems as part of the CI/CD pipeline, ensuring that all aspects of the software are thoroughly tested.

By employing these practices, high code quality and system reliability are maintained, enabling efficient and effective development and deployment processes.

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/cicd1.png"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/cicd2.png"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div> 
<div class="caption">
    The CI/CD pipeline.
</div>