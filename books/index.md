---
title: Books
lede: The Arbuthnot Books list.
layout: page
permalink: /books/
---

{% assign authors = site.books | map: "author" | compact | uniq | sort %}
{% assign authors = authors | where_exp: "a", "a != ''" %}

{% if authors.size > 1 %}
  <p class="meta">
    {% for a in authors %}
      <span class="tag">{{ a }}</span>
    {% endfor %}
  </p>
{% endif %}

<ul class="book-list">
  {% assign ordered   = site.books | where_exp: "b", "b.order != nil and b.order != ''" | sort: "order" %}
  {% assign unordered = site.books | where_exp: "b", "b.order == nil or b.order == ''" | sort: "title" %}
  {% assign books = ordered | concat: unordered %}

  {% for b in books %}
    <li class="book-list__item">
      <a href="{{ b.url | relative_url }}">{{ b.title }}</a>

      {% if b.author and b.author != '' %}
        <span class="fine"> by {{ b.author }}</span>
      {% endif %}

      {% if b.lede and b.lede != '' %}
        <div class="fine book-list__lede">
          {{ b.lede }}
        </div>
      {% endif %}
    </li>
  {% endfor %}
</ul>