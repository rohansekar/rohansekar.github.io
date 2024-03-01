---
layout: page
title: A Sequential Quadratic Program Solver using ProxQP
description: Developed an SQP solver and compared its performance on a series of problems, benchmarking different QP solvers
img: assets/img/ocrl.png
importance: 2
category: Research
# related_publications: einstein1956investigations, einstein1950meaning
---

In the realm of optimal control problems, a variety of solvers and symbolic toolboxes are available, each exhibiting distinct performance characteristics contingent on the problem's structure and size. Linear and quadratic problems (QP) benefit from straightforward optimization solutions with numerous existing solvers. However, non-linear problems necessitate more sophisticated solvers such as those employing interior point methods, Augmented Lagrangians, and sequential quadratic programs (SQP). This project aimed to explore these tools, culminating in the development of an SQP solver. The study involved a comprehensive comparison of its performance on various problems, benchmarking different QP solvers. Additionally, the project delved into symbolic math libraries, notably SymForce, for generating Hessians and Jacobians. Future endeavors include integrating these components to establish an end-to-end workflow encompassing problem formulation, code generation, and problem-solving.<br>
**Methods**:<br>
To assess solver performance, we implemented an SQP solver and conducted a thorough comparison with existing QP solvers, particularly focusing on ProxQP and OSQP. The evaluation spanned multiple tests, examining both runtime and convergence metrics. Notably, ProxQP demonstrated superior convergence, requiring fewer iterations for both linear and quadratic problems. Although the runtime performance for simple QPs remained comparable, ProxQP emerged as notably more efficient for solving non-linear problems in terms of both runtime and iteration count. In a specific case involving a simple NLP with an infeasible start, OSQP outperformed ProxQP in terms of iteration count, potentially attributed to optimal parameter tuning for initializing the solver, as suggested in the problem description


<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/ocrl.png"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
     <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/algocrl.png" title="example image" class="img-fluid rounded z-depth-1"  %}
    </div>
</div> 
<div class="caption">
    Step-by-step approach to solve the problem
</div>
<!-- <div class="row">
</div> -->
<!-- <div class="caption">
    This image can also have a caption. It's like magic.
</div> -->

**The quantitative results obtained were as follows**:


<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/result1ocrl.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/result2ocrl.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Comaprison between OSQP and ProxQP
</div>

<br>
**Results:**<br>
The comparative analysis revealed that ProxQP excels in terms of convergence, outperforming other solvers for NLPs. However, OSQP showcased superiority in scenarios involving infeasible starting points, emphasizing the impact of parameter tuning on solver performance. While ProxQP displayed efficiency in terms of iteration count, OSQP's performance in certain scenarios highlights the significance of solver initialization.

Discussion and Future Work:
The findings underscore the importance of considering problem characteristics and tuning solver parameters for optimal performance. Future work aims to integrate the developed SQP solver with symbolic math libraries like SymForce, creating a seamless end-to-end workflow. This integration will facilitate problem formulation, code generation, and efficient solving of non-linear programs, providing a comprehensive and streamlined approach to optimal control problems.
