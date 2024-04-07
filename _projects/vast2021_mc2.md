---
layout: page
title: VAST 2021 Mini Challenge 2
description: Solving the mystery behind the disappearance of employees by visualizing employee data.
img: assets/img/DV_cover.png
importance: 4
category: academia
github: https://github.com/HitanshShah/vast-2021-mini-challenge-2
---
Created Using: <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">HTML</span> <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">CSS</span> <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">D3.js</span> <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">Python</span>

This project was our solution to the <a href="https://vast-challenge.github.io/2021/MC2.html">VAST 2021 Mini Challenge 2</a>. A live demo of this project can be found <a href = "https://hitanshshah.github.io/vast-2021-mini-challenge-2/">here</a>! The code for this project is available at: <a href="https://github.com/HitanshShah/vast-2021-mini-challenge-2">github.com/HitanshShah/vast-2021-mini-challenge-2</a>. Reach out to me via <a href="mailto:hitansh.shah@gmail.com">email</a> if you have any queries related to this project.

This challenge is about the disappearance of certain employees of a natural gas production company, GASTech, right before its initial public offering. We have been provided with the following data and the main objective is to visualize this data, observe trends, patterns, or anomalies in the behavior of these employees and understand who was behind the kidnapping of employees:
<uL>
    <li>GPS tracking data of each vehicle</li>
    <li>Vehicle to employee mapping</li>
    <li>Credit card and Loyalty card transaction information</li>
    <li>ESRI shapefiles of Abila and Kronos, the city of this company</li>
</ul>

To visualize this data, we created the following visualizations:
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/DV_image3.png" title="Radial Bar Plot and Radial Scatter Plot" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Radial Bar plot and Radial Scatter Plot.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/DV_image1.png" title="Car tracking using the GPS data on a map created using the shapefiles" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Car tracking using the GPS data on a map created using the shapefiles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/DV_image4.png" title="Scattered Boxplot" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: (flowing through 3 images) A Sankey chart showing the number of occurrences a car and a credit/loyalty card were spotted together according to our algorithm. Right: Scattered Boxplot showing spending trends at each of the locations.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/DV_image2.png" title="Network Plot between employees and locations" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Mapping of credit/loyalty card and employees. Right: Network Plot between employees and locationst.
</div>

Please watch the following short video in which I demonstrate the working and functionalities of the overall solution:
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/DV_video_1.mp4" title="Demo Video" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
