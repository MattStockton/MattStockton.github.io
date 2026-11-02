---
layout: default
title: Matt Stockton
---

<div class="wrap">
  <section class="hero">
    <div>
      <h1>I build software and write about what I learn.</h1>
      <p class="hero__lead">I've spent more than 20 years building software and roughly a decade working in ML and AI. I write longer pieces here, and share what I'm trying, reading, and listening to in a regular <a href="{{ '/writing/digest/' | relative_url }}">digest</a>. You can also find my day-to-day thinking <a href="{{ site.author.x }}">on X</a>.</p>
      <div class="actions">
        <a class="text-link" href="{{ '/writing.html' | relative_url }}">Read the writing &rarr;</a>
        <a class="text-link" href="{{ '/my-background.html' | relative_url }}">About me &rarr;</a>
      </div>
    </div>
    <img class="hero__photo" src="{{ site.author.avatar | relative_url }}" alt="Matt Stockton" width="200" height="240">
  </section>

  <section class="home-section" aria-labelledby="writing-heading">
    <div class="section-head">
      <h2 id="writing-heading">Writing</h2>
      <a class="text-link" href="{{ '/writing.html' | relative_url }}">All essays &rarr;</a>
    </div>
    <ul class="list">
      {% assign latest_digest = site.digests | sort: "date" | last %}
      {% if latest_digest %}
      <li class="list__row list__row--digest">
        <time class="meta" datetime="{{ latest_digest.date | date_to_xmlschema }}">{{ latest_digest.date | date: "%b %-d, %Y" }}</time>
        <div>
          <a class="list__title" href="{{ latest_digest.url | relative_url }}">{{ latest_digest.date | date: "%B %-d" }}</a>
          <p>{{ latest_digest.excerpt | strip_html }}</p>
        </div>
      </li>
      {% endif %}
      {% for post in site.posts limit:5 %}
      <li class="list__row">
        <time class="meta" datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %-d, %Y" }}</time>
        <a class="list__title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </li>
      {% endfor %}
    </ul>
  </section>

  <section class="home-section" aria-labelledby="notes-heading">
    <div class="section-head">
      <h2 id="notes-heading">Notes</h2>
      <a class="text-link" href="{{ '/notes.html' | relative_url }}">All notes &rarr;</a>
    </div>
    <ul class="list">
      {% assign notes = site.data.x_notes | where_exp: "note", "note.archived != true" %}
      {% for note in notes limit:3 %}
      <li class="list__row">
        <time class="meta" datetime="{{ note.datetime }}">{{ note.date }}</time>
        <div>
          <a class="list__title" href="/notes/{{ note.slug }}/">{{ note.title }}</a>
          <p>{{ note.summary }}</p>
        </div>
      </li>
      {% endfor %}
    </ul>
  </section>

  <section class="home-section" id="projects" aria-labelledby="projects-heading">
    <div class="section-head">
      <h2 id="projects-heading">Projects</h2>
      <a class="text-link" href="{{ '/experiments.html' | relative_url }}">All projects &rarr;</a>
    </div>
    <div class="projects">
      {% assign featured = site.data.experiments | where: "featured", true | where_exp: "item", "item.preview" | sort: "datetime" | reverse %}
      {% for item in featured limit:4 %}
      <article class="project">
        <div class="project__image"><img src="{{ item.preview }}" alt="" loading="lazy" width="1200" height="630"></div>
        <p class="meta">{{ item.kind }} &middot; {{ item.date }}</p>
        <h3><a href="{{ item.url }}"{% if item.external %} rel="noopener noreferrer"{% endif %}>{{ item.title }}</a></h3>
        <p>{{ item.short }}</p>
      </article>
      {% endfor %}
    </div>
  </section>

  <p class="aside-note">I do client work through <a href="{{ site.company.url }}">{{ site.company.name }}</a>, mostly applied AI for investment research. <a href="{{ '/work-with-me.html' | relative_url }}">More on that</a>.</p>
</div>
