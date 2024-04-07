---
layout: page
title: Covid-19 Vaccine Stance Detection
description: Exploring contrasting and varied opinions on Covid-19 Vaccines on Twitter.
img: assets/img/Covid19.png
importance: 5
category: academia
github: https://github.com/HitanshShah/covid-19-twitter
---
Created Using: <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">Python</span> <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">Tweepy</span> <span class="badge" style="background-color: var(--global-theme-color); border-color: var(--global-theme-color) !important">NetworkX</span>

<i>The code for this project is available at: <a href="https://github.com/HitanshShah/covid-19-twitter">github.com/HitanshShah/covid-19-twitter</a>. Reach out to me via <a href="mailto:hitansh.shah@gmail.com">email</a> if you have any queries related to this project.</i>

Social media provides users with not just a huge source of information, but also the freedom to post their own views and opinions related to certain subjects. Each individual is entitled to their own thoughts or opinions. One such subject matter was the Covid-19 pandemic and the vaccines developed to fight the virus. On one hand, there was the thought the vaccines are going to put an end to the global suffering, whereas on the other, people thought vaccines were ploys set by the government and medical institutions. This project analyzes the sentiments around Covid-19 vaccines on Twitter by analyzing tweets from both, Pro and Anti, vaccine campaigns.

The first step was to scrape data from Twitter using the <strong>Twitter Developer API</strong> and <strong>Tweepy</strong> library. I scraped this data on the basis of popular hashtags like <strong>#WearAMask</strong>, <strong>#GetVaccinated</strong>, <strong>#MaskUp</strong>, <strong>#NoVaccinMandate</strong>, <strong>#NoVaccineForMe</strong>. I chose these hashtags because they were not the most common or famous ones, which made it easier to get precise insights. For instance, I found a number of tweets which were neither pro nor anti, but more of a general discussion starter, for hashtags like <strong>VaccineIsPoison</strong> or <strong>VaccinesWork</strong>, which otherwise sound like having strong opinions.

For each of these hashtags, I used the following approach:
<ul>
    <li>Extract 200 tweets using the hashtag as the keyword. Here, I excluded retweets, because popular tweets could have many many retweets and that would skew the results significantly.</li>
    <li>From all of these tweets, generate a set of Unique Hashtags. Most users on the internet tend to use more than one hashtags in their tweets or posts. Thus, it would be interesting to see how many unique hashtags there would be associated with our hashtags and if we could observe any patterns.</li>
    <li>Create a co-occurrence matrix for all of these keywords, and normalize the values.</li>
    <li>Using this co-occurence matrix and the count of occurrences of individual hashtags, create a circular layout network graph, in which the hashtags with a higher occurrence are displayed in the central region of the network.</li>
    <li>Plot the connected components of these graphs to analyze sparsity or density.</li>
    <li>Plot the degree rank and degree distribution of these networks for statistical comparisons.</li>
</ul>

<strong>Results</strong>

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Covid19.jpg" title="#WearAMask" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/covid_2.jpg" title="#NoVaccinesMandate" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Network graph for #WearAMask. Right: Network graph for #NoVaccinesMandate.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/covid_3.jpg" title="#WearAMask" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/covid_4.jpg" title="#NoVaccinesMandate" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: #WearAMask. Right: #NoVaccinesMandate.
</div>

From the above visualizations, we can make the following conclusions:
<ul>
    <li>Generally, for positive or pro-vaccine campaign hashtags, the network graphs are dense with higher degree distribution. It is quite the opposite for negative or anti-vaccine campaign hashtags.</li>
    <li>There are more central thoughts for pro-vaccine, whereas the anti-vaccine tweets originate from fewer central thoughts, and usually revolve around the same train of thought.</li>
</ul>
