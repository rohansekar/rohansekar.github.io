---
layout: page
title: Uncovering hidden patterns:Study on masked autoencoders
description: Exploring masked autoencoders for the purpose of reconstructing an image from a masked input image.
img: assets/img/ae2.png
importance: 3
---

An autoencoder is a type of artificial neural network used to learn efficient codings of unlabeled data (unsupervised learning). An autoencoder learns two functions: an encoding function that transforms the input data, and a decoding function that recreates the input data from the encoded representation.<br>
Masked Autoencoders represent a class of autoencoder neural networks designed to enhance the learning and representation of hidden structures within input data. These models utilize a masking mechanism, which restricts the autoencoder's access to certain input features during training. This constraint encourages the network to learn more robust and informative representations, making masked autoencoders particularly effective in capturing intricate patterns and relationships within the data.<br>
**Methods:**<br>
The types of masked autoencoders that were implemented for this project are:<br>
* Vanilla Autoencoders<br>
* Vision Transformers<br>


**Some notable results obtained were as follows**

* **Reconstruction of an image using Vision Transformers**

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/autoencoders.png"  title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

* **Reconstruction of an image using Vanilla Autoencoders and Adversarial Autoencoders**

<div>
     <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/autoencodersvanilla.png" title="example image" class="img-fluid rounded z-depth-1"  %}
    </div>
</div> 

<div class="caption">
    The original and the reconstructed image
</div>

**Results:**<br>
Masked autoencoders have demonstrated success in various applications, such as image and sequence data processing, where capturing complex dependencies is crucial. By leveraging the masking technique, these autoencoders can uncover intricate patterns and extract meaningful features, leading to improved data representation.<br>

**Discussion:**<br>
The introduction of masking in autoencoders represents an innovative approach to enhance the learning capabilities of neural networks. By selectively concealing input features, masked autoencoders compel the model to focus on the most relevant information, fostering the development of more concise and informative representations. This method stands out as a valuable tool in scenarios where intricate patterns and relationships in the data require careful consideration.<br>

**Future Work:**<br>
Future research endeavors may explore further refinements and adaptations of masked autoencoders for specific domains and applications. Investigating the impact of different masking strategies, exploring architectural modifications, and assessing the generalizability of these models to diverse datasets could contribute to advancing the effectiveness and versatility of masked autoencoders. The ongoing development and exploration of masked autoencoders hold promise for addressing complex learning tasks in various domains.

