---
title: Notes
lede: Occasional essays and workshop reflections.
layout: page
permalink: /notes/
---

<ul class="notes-list">
{% assign items = site.posts | sort: "date" | reverse %}
{% for post in items %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="fine"> — {{ post.date | date: "%-d %B %Y" }}</span>
    {% if post.author %}<span class="fine"> · {{ post.author }}</span>{% endif %}
  </li>
{% endfor %}
</ul>