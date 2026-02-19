---
title: Books
lede: The Arbuthnot Books list.
layout: page
permalink: /books/
---

<ul>
{% assign items = site.books | sort: "order" %}
{% for b in items %}
  <li>
    <a href="{{ b.url }}">{{ b.title }}</a>
    {% if b.lede %}<span class="fine"> — {{ b.lede }}</span>{% endif %}
  </li>
{% endfor %}
</ul>