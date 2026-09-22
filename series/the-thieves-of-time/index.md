---
layout: page
title: The Thieves of Time
lede: A sequence of novels by Eamonn Vincent.
series_id: the-thieves-of-time
permalink: /series/the-thieves-of-time/
---

From Cambridge in 1974 to divided Berlin and the London of the mid-seventies,
*The Thieves of Time* follows Steve Percival through a world of poetry, music,
artistic ambition and Cold War intrigue. Friends, artists and academics recur
across the novels, their lives connected by love, loyalty and the search for a
place in a changing world.

## Reading order

Begin with *Event/Horizon*, then continue with *Palace of Tears* and
*The Parallax View*. Each book's page offers a sample, purchase links, and
Notes, Places and People to explore.

{% assign sequence_books = site.books | where: 'series', page.series_id | sort: 'order' %}
<ol class="sequence-books">
{% for book in sequence_books %}
  <li class="sequence-book">
    {% if book.cover %}
      <a class="sequence-book__cover" href="{{ book.url | relative_url }}"><img src="{{ book.cover | relative_url }}" alt="{{ book.title | escape }} — cover" loading="lazy" /></a>
    {% endif %}
    <div>
      <p class="fine">Book {{ book.order }}</p>
      <h3><a href="{{ book.url | relative_url }}">{{ book.title }}</a></h3>
      {% if book.lede %}<p>{{ book.lede }}</p>{% endif %}
      <p><a href="{{ book.url | relative_url }}">Explore the book →</a></p>
    </div>
  </li>
{% endfor %}
</ol>

## Forthcoming

**Book Four: Double Exposure** will continue *The Thieves of Time* sequence.
Further details will appear here when available.
