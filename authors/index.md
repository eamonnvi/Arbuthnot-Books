---
layout: page
title: Authors
permalink: /authors/
---

<ul>
  {% for pair in site.data.authors %}
    {% assign id = pair[0] %}
    {% assign a = pair[1] %}
    <li>
	
      <a href="{{ '/authors/' | append: id | append: '/' | relative_url }}">{{ a.name }}</a>
      {% if a.photo %}
		<img class="author-photo"
	       src="{{ a.photo | relative_url }}"
	       alt="{{ a.name }}">
	{% endif %}
    </li>
  {% endfor %}
</ul>
