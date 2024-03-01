---
layout: page
title: Implicit Neural Representations
description: This is a project on neural implicit representation of a deep network that can be used to memorize an image or even reconstruct it from non-linear measurements.
img: assets/img/INR.png
importance: 2
category: Robotics
---

Implicitly defined signal representations, characterized by their continuity and differentiability and parameterized through neural networks, have emerged as a potent paradigm, presenting numerous potential advantages over traditional representations. This project focused on implementing four distinct variants of Implicit Neural Networks (INNs), exploring their applications in various contexts.

**Methods:**<br>
The implemented INN variants encompassed the following:

* Vanilla image regression with implicit neural representations.<br>
* Image regression with implicit neural representations using a Fourier feature network.<br>
* Reconstruction from the Radon transform.<br>
* Reconstruction from a non-linear Radon transform.<br>


* **Vanilla image regression with implicit neural representations**

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/original_1.png"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
     <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/original_2.png" title="example image" class="img-fluid rounded z-depth-1"  %}
    </div>
</div> 
<div class="caption">
    The original and the reconstructed image
</div>
<!-- <div class="row">
</div> -->
<!-- <div class="caption">
    This image can also have a caption. It's like magic.
</div> -->
* **Image regression with implicit neural representations using a fourier feature network**

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/original_1.png"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
     <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/result_3.png" title="example image" class="img-fluid rounded z-depth-1"  %}
    </div>
</div> 
<div class="caption">
    The original and the reconstructed image
</div>
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/result_4.png"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
     <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/result_5.png" title="example image" class="img-fluid rounded z-depth-1"  %}
    </div>
</div> 
<div class="caption">
    The original and the reconstructed image
</div>


**Results:**<br>
Upon examination, the use of a Fourier feature network in image regression yielded results of superior quality when compared to the vanilla image regression method. This observation suggests that incorporating Fourier features enhances the performance and output quality of implicit neural representations in the context of image regression.

**Discussion:**<br>
The findings underscore the effectiveness of leveraging Fourier features within implicit neural representations for improved results in image regression tasks. This signifies a notable advancement in the application of INNs, demonstrating their adaptability to different signal processing scenarios. The comparison between vanilla image regression and Fourier feature-enhanced regression highlights the importance of feature engineering in optimizing the performance of implicit neural networks.

**Future Work:**<br>
Future work may involve further exploration and refinement of the Fourier feature network's integration within implicit neural representations. Additionally, expanding the study to other signal processing tasks and domains could provide insights into the generalizability and versatility of the proposed approach. The project lays the groundwork for continued research and development in the realm of implicit neural representations and their applications.