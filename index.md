---
layout: collection
title: 
classes: wide
---

<h1 class = "fancy-text"> Hello✌ </h1>


<p style="text-align: center; margin: 60px 0 25px 0; font-size: 34px;">
I'm <span style="font-weight: bold">Anton,</span> an Unreal Engine <span style="font-weight: bold">UI Developer.</span> <br>
I like programming, video games and pretty UIs.
</p>


<div style="display: flex; column-gap: 20px; row-gap: 10px; justify-content: center; flex-wrap: wrap; margin-bottom: 60px">
    <a href="/about" class="secondary-button button"> More about me </a>
    <a href="/portfolio" class="primary-button button"> Portfolio </a>
    <a href="/projects" class="secondary-button button"> All projects </a>
</div>


<h1 class="h-landing">
    My experience
</h1>
 
{% assign jobs = site.data.resume.jobs %}
{% include timeline.html entries = jobs %}

<h1 class="h-landing" style="margin-bottom: 40px"> 
    Best projects
</h1>

{% capture portfolio %}
    {% include documents-collection.html.liquid collection='portfolio' sort_by = 'priority' flag = 'portfolio'%}
{% endcapture %}

{% include h-scroll-box.liquid items = portfolio %}

<div style="display: flex; justify-content: center; margin-top: 40px">
    <a href="/projects" class="primary-button button">All projects ></a>
</div>
