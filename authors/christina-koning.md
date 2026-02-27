---
layout: page
title: Christina Koning
permalink: /authors/christina-koning/
---

<ul>
  {% assign books = site.books | sort: "order" %}
  {% for b in books %}
    {% if b.author == "Christina Koning" %}
      <li><a href="{{ b.url | relative_url }}">{{ b.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>