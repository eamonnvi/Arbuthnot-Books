---
layout: page
title: Authors
permalink: /authors/
---

<ul>
  {% assign books = site.books | sort: "order" %}
  {% assign authors = books | map: "author" | compact | where_exp: "x", "x != ''" | uniq | sort %}
  {% for a in authors %}
    <li>
      <a href="{{ '/authors/' | append: a | slugify | append: '/' | relative_url }}">{{ a }}</a>
    </li>
  {% endfor %}
</ul>