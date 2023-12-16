---
layout: single
title: Personal products
permalink: /projects/
---
These are my personal self-distributed projects

{% capture games %}
    {% include documents-collection.html collection='portfolio' sort_order='reverse' sort_by = 'date' type = 'Game'%}
{% endcapture %}

{% capture plugins %}
    {% include documents-collection.html collection='portfolio' sort_order='reverse' sort_by = 'date' type = 'Plugin'%}
{% endcapture %}

{% capture demos %}
    {% include documents-collection.html collection='portfolio' sort_order='reverse' sort_by = 'date' type = 'Demo'%}
{% endcapture %}

---
# Games

{% include colcade-grid.html items = games %}

---
# Plugins

{% include colcade-grid.html items = plugins %}

---
# Demos

{% include colcade-grid.html items = demos %}
