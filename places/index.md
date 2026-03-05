---
layout: page
title: Places
permalink: /places/
---

<ul class="place-list">
  {% assign ps = site.places | sort: "title" %}
  {% for p in ps %}
    <li><a href="{{ p.url | relative_url }}">{{ p.title }}</a></li>
  {% endfor %}
</ul>