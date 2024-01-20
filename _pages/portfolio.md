---
title: Portfolio
layout: collection
permalink: /portfolio/
classes: wide
---

{% capture portfolio %}
    {% include documents-collection.html.liquid collection='portfolio' sort_by = 'priority' flag = 'portfolio'%}
{% endcapture %}

{% include colcade-grid.html items = portfolio %}
