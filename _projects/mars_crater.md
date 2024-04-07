---
layout: page
title: Mars Crater Detection
description: Performing semantic segmentation on Martian satellite images to identify craters along with their classes.
img: assets/img/ctx.jpg
importance: 1
category: academia
related_publications: false
github: https://github.com/HitanshShah/mars-crater-detection
---
Created Using: <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">Python</span> <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">TensorFlow</span> <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">Keras</span> <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">OpenCV</span>

I can say that this project has been the highlight of my masters degree. I published a research paper on this project and got to present it at the ACM SIGSPATIAL conference in Hamburg, Germany.

<i>The code for this project is available at: <a href="https://github.com/HitanshShah/mars-crater-detection">github.com/HitanshShah/mars-crater-detection</a>. Reach out to me via <a href="mailto:hitansh.shah@gmail.com">email</a> if you have any queries related to this project.</i>

Crater Detection and Crater Counting have historically been manual and tedious tasks. With the recent advancements in the field of Deep Learning and Computer Vision, and with the availability of higher computation power, it has been possible to automate this process. Almost all of the recent studies have used some or the other variation of a U-Net architecture for this task. We aimed to outperform these former State-of-the-Art methods by using a U2-Net architecture, which in simple words, is a U-Net made up of U-Nets at all of its levels. We were able to achieve our goal, however, this was a binary semantic segmentation, i.e., the output only said if a particular part of the image was a crater or not a crater.

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_crops_edges.jpg" title="Binary Semantic Segmentation with edge masks" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_crops_filled.jpg" title="Binary Semantic Segmentation with filled masks" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Binary Crater Segmentation using Edges of Craters as ground truth annotations. Right: Binary Crater Segmentation using Full Craters as ground truth annotations.
</div>

However, it must be noted that not all craters are of the same nature. Some craters millions and millions of years old, whereas some are relatively new. Some craters, being so old, might even be filled or covered by a fresher layer, which in turn could be from different sources, like volcanic sedimenation, settling of dust, and so on. Some craters might have been formed as a result of ejecta material from another primary impact crater. These factors become relevant when crater counting is used for tasks like Surface Age Estimation. Thus, it is important to not just identify craters, but also get some insights related to the nature of the crater. There had been no research done on this till date and my team and I were the first ones to come up with a proper pipeline for the same. We collaborated with our professors <a href="https://hannah-rae.github.io/">Dr. Hannah Kerner</a> and <a href="https://www.adlerlab.org/home">Dr. Jacob Adler</a> to get more domain specific knowledge and to convert this from a class project to a research project.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/main_diagram_1.jpg" title="Overall Pipeline for Binary and Multi-class Crater Segmentation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Pipeline of Binary and Multi-class semantic segmentation of Martian satellite images.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_crops_edges_mc.jpg" title="Multi-class Crater Segmentation using Edge masks" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Multi-class Segmentation using Edges of Craters as ground truth annotations.
</div>

All of our research and model training was done on the THEMIS dataset. Even though consistent with all other related research, this dataset is relatively old and of lower resolution. The newer CTX dataset provides a much higher resolution (20 times) than THEMIS and should be the base of all future studies. However, since it is such a high quality dataset, it is computationally inefficient (and close to impossible) to train Deep Learning models of similar complexity purely on this dataset at the same scale. To prove that our model, even though trained on a lower quality dataset, was capable of segmenting the higher resolution CTX images, we performed 2 out-of-domain evaluations.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/main_diagram2.jpg" title="Overall Pipeline for out-of-domain evaluation of Binary Crater Segmentation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Pipeline for Out-of-Domain evaluation of Binary Crater Segmentation on CTX and DoMars16k datasets.
</div>

For detailed results, discussions and other information related to project, pls read my paper here.
I am currently working on improving the performance of the multi-class segmentation by using various data augmentation techniques and balanced loss functions catered specifically towards imbalanced datasets.
