---
title: Arbuthnot Books
layout: default
description: Arbuthnot Books — fiction and ideas.
---
<section class="grid home-grid">
  <article class="card">
    <h2>The Parallax View</h2>
    <p class="lede">
      A Cold War novel set in London and Cambridge in 1976: archives, doubleness, and the gap between what is said and what is meant.
    </p>

    <p class="meta">
      <span class="tag">London &amp; Cambridge · 1976</span>
      <span class="tag">Espionage · Literary</span>
      <span class="tag">Identity · Betrayal · Desire</span>
    </p>

    <p class="fine">
		Eamonn Vincent's The Parallax View is the third book in The Thieves of Time series. It was preceded by Event/Horizon and Palace of Tears.  
	</p>

    <p class="links">
      <a href="https://www.amazon.co.uk/Parallax-View-Thieves-Time-Book-ebook/dp/B0FYY7SDYM/" target="_blank" rel="noopener">
        Buy / Retailers →
      </a>
    </p>

    <p class="links">
      <a class="btn" href="{{ '/assets/pdfs/TPV-17nov25-sample.pdf' | relative_url }}" target="_blank" rel="noopener">
        Read a sample (PDF)
      </a>
    </p>

    <p class="links">
      <a href="https://www.amazon.co.uk/dp/B0FG3BGSG3?binding=paperback&ref=dbs_m_mng_rwt_sft_tpbk_tkin" target="_blank" rel="noopener">
        Steve Percival sequence →
      </a>
    </p>
  </article>

  <aside class="card home-cover">
    <h2>The Parallax View</h2>
    <p class="meta"><span class="tag">Front cover</span></p>
    <img src="{{ '/assets/tpv-cover.jpg' | relative_url }}"
         alt="The Parallax View — front cover"
         style="width:100%; border:1px solid var(--line); border-radius:14px;"
         loading="lazy" />
    <p class="fine">"The truth is what one is not allowed to say -M."</p>
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