---
layout: page
title: Echo Chamber Detection
description: Understanding the spread of misinformation and political polarization in social media.
img: assets/img/MAGA1.jpg
importance: 3
category: academia
---
Created Using: <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">Python</span> <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">PyTorch</span> <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">HuggingFace</span> <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">Gephi</span>

In today's digital world, the widespread use of social media platforms such as Twitter, Instagram, and Facebook has provided individuals with unparalleled access to copius amounts of information and connections. While empowering, this accessibility poses two significant challenges. Firstly, users struggle with information overload, making it challenging to sift through the constant influx of content. Secondly, the prevalence of misinformation and disinformation compounds the problem, as users encounter content with hidden agendas. Additionally, social media's algorithm-driven content delivery often reinforces existing beliefs, creating echo chambers where users are exposed to ideas that mirror their own, perpetuating a cycle of reinforcement.

This project was created to explore the phenomenon of echo chambers on Twitter, specifically focusing on political agendas like MAGA (Make America Great Again). Our objective was to investigate the role of social media platforms in fostering echo chambers by analyzing tweets from around 10,000 users. By categorizing their political affiliations as Democratic or Republican, we examined and dissected the resulting echo chambers. Through this study, we sought to delve into the implications of these digital environments and gain a deeper understanding of the issues surrounding information overload and misinformation prevalent in today's social media realm, as observed through our findings.

To achieve this, we designed a multi-stage pipelin: We used #MAGA (#MakeAmericaGreatAgain), the basis of our study, to generate the retweet network from OSoMe network tool. Then we cleaned the data and generated the largest connected graph. We use some clustering algorithms to generate priliminary echo chambers. Then the users and their tweets are parsed by our network model, which finally yields the similarity weighted echo chambers. The below flowcharts provide a better visualization of the same.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/MODEL.drawio.png" title="Overall Model Pipeline" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Overall Model Pipeline to detect Echo Chambers.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/twitter_scraping.drawio.png" title="Tweet Scraping and Similarity Measure Model Architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Tweet Scraping and Similarity Measure Model Architecture.
</div>

<strong>Results</strong>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/MAGA1.jpg" title="Echo Chambers based on #MAGA" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Weight based Echo Chambers for #MAGA.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/echo_chamber_with_twitter_users.png" title="Echo Chambers with Important Media personalities and organizations" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Echo Chambers with Important Media Personalities and Organizations. This project was from the time when Mr. Donald Trump was banned from Twitter, which is why you cannot see his profile in the network. Some other extremist Republican accounts had also been suspended at the time. 
</div>

<i>This project involves sensitive and private user data which cannot be publicly shared. In compliance with academic integrity rules, we cannot make the source code public either. If you have any questions or would like to learn more about the project and its details, please feel free to contact me at <a href="mailto:hitansh.shah@gmail.com">hitansh.shah@gmail.com</a>.</i>