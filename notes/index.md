---
title: Notes
lede: Occasional essays and workshop notes. No schedule.
layout: page
---

<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="fine"> — {{ post.date | date: "%Y-%m-%d" }}</span>
  </li>
{% endfor %}
</ul>
