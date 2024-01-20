---
layout: collection
title: 
permalink: /projects/
classes: wide
---


{% capture all %}
    {% include documents-collection.html.liquid collection='portfolio' sort_order='reverse' sort_by = 'year'%}
{% endcapture %}

{% capture games %}
    {% include documents-collection.html.liquid collection='portfolio' sort_order='reverse' sort_by = 'date' type = 'Game'%}
{% endcapture %}

{% capture plugins %}
    {% include documents-collection.html.liquid collection='portfolio' sort_order='reverse' sort_by = 'date' type = 'Plugin'%}
{% endcapture %}

{% capture demos %}
    {% include documents-collection.html.liquid collection='portfolio' sort_order='reverse' sort_by = 'date' type = 'Demo'%}
{% endcapture %}

{% include colcade-grid.html items = all %}

{% comment %}# Games 🎮

{% include test-grid.html items = games %}

---
# Plugins 🔌

{% include test-grid.html items = plugins %}

---
# Demos ⚙

{% include test-grid.html items = demos %}{% endcomment %}
