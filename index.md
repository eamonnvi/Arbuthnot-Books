---
title: Arbuthnot Books
layout: default
description: Arbuthnot Books — fiction and ideas.
---
<section class="grid home-grid">
  <article class="card">
    <h2>A Deathly Silence</h2>
    <p class="lede">
      When the agents start dying, the clues are all in the books.
    </p>

    <p class="meta">
      <span class="tag">London  · 2026</span>
      <span class="tag">Literary · Satire</span>
      <span class="tag">Crime · Celebrity · Publishing</span>
    </p>

    <p class="fine">
      Literary agents are dying, and the deaths have an unnerving habit of resembling scenes from books. DI Jake Kowalczyk is the first to see the pattern. His investigation takes him through the agencies, parties, lunches and literary festivals of London publishing — a world Christina Koning regards with a distinctly satirical eye.
    </p>

    <p class="fine">
      A Deathly Silence is a dryly funny police procedural about books, ambition, rejection and the people who decide which stories get heard.
    </p>

    <p class="fine">Forthcoming</p>

    <p class="links">
      <a class="btn" href="{{ '/assets/pdfs/ADS-sample.pdf' | relative_url }}" target="_blank" rel="noopener">
        Read a sample (PDF)
      </a>
    </p>
  </article>

  <aside class="card home-cover">
    <h2>A Deathly Silence</h2>
    <p class="meta"><span class="tag">Front cover</span></p>
    <a href="{{ '/books/a-deathly-silence/' | relative_url }}" aria-label="About A Deathly Silence">
      <img src="{{ '/assets/a-deathly-silence-cover.jpg' | relative_url }}"
           alt="A Deathly Silence — front cover"
           style="width:100%; border:1px solid var(--line); border-radius:14px;"
           loading="lazy" />
    </a>
    <p class="fine">Murder, manuscripts and the London literary world</p>
  </aside>

  <div class="card home-notes">
    <h2>Latest from Notes</h2>
    <p class="fine">Occasional essays and workshop reflections.</p>

    <ul class="notes-latest">
      {% assign latest = site.posts | slice: 0, 3 %}
      {% for post in latest %}
        <li>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <span class="fine">
            — {{ post.date | date: "%-d %B %Y" }}
            {% if post.author %}
              {% assign author_key = post.author | downcase %}
              {% assign author = site.data.authors[author_key] %}
              · {{ author.name | default: post.author }}
            {% endif %}
          </span>
        </li>
      {% endfor %}
    </ul>

    <p style="margin:12px 0 0">
      <a class="pill" href="{{ '/notes/' | relative_url }}">All Notes →</a>
    </p>
  </div>
</section>
