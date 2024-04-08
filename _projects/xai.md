---
layout: page
title: XAI - eXplainable Artificial Intelligence
description: Slicing the blackbox and understanding its outputs.
img: assets/img/publication_preview/XAI.jpg
importance: 6
category: academia
---

This is my capstone project from my undergrad degree. In today's world, computer scientists have found a way to incorporate Artificial Intelligence into practically almost everything. We are always fascinated by how these systems work and how they make our life easy, but have we ever wondered why an AI model predicted the way it did or what made an AI model generate a particular output? In this study, we took one such example of malaria detection from stained blood cells using a Convolutional Neural Network (blackbox), and tried to understand what happened at each of the layers of the model.

<strong>Pipeline and methodology:</strong>
<ul>
    <li>The CNN we used was built with a ResNet-34 backbone with 6 additional fully connected sequential layers and sigmoid activation function. The overall accuracy of this model was 85.32%</li>
    <li>To understand the outputs from this CNN, we designed our own model - A regularied linear regression model (Ridge Regression) that dissects a neural network at any layer and provides information about neuron activation at that layer.</li>
    <li>We break our system into 4 main modules: Feed Input Module, Output Explanation Module, Layer Activation Module and Visualizing Neuron Module</li>
    <li>We will mainly focus on the output of the 4th module</li>
</ul>

<strong>Results:</strong>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/XAI_1.jpg" title="Uninfected and Infected cells" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Uninfected and Infected cells.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/XAI_2.jpg" title="Uninfected and Infected cells" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Neuron activations for innermost layer for infected cell.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/XAI_3.jpg" title="Uninfected and Infected cells" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Neureon activations for outermost layer for uninfected cell.
</div>