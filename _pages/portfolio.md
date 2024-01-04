---
title: Portfolio
layout: collection
permalink: /portfolio/
classes: wide
---

{% capture portfolio %}
    {% include documents-collection.html.liquid collection='portfolio' sort_order='reverse' sort_by = 'date' flag = 'portfolio'%}
{% endcapture %}

{% include test-grid.html items = portfolio %}
