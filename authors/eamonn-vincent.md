---
layout: page
title: Eamonn Vincent
permalink: /authors/eamonn-vincent/
---

<ul>
  {% assign books = site.books | sort: "order" %}
  {% for b in books %}
    {% if b.author == "Eamonn Vincent" %}
      <li><a href="{{ b.url | relative_url }}">{{ b.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>