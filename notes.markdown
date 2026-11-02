---
layout: default
title: Notes
description: "Selected notes from X that I want to keep easier to find."
---

<div class="wrap">
  <header class="page-head">
    <h1>Notes</h1>
    <p class="lead">Most of my shorter writing happens on <a href="{{ site.author.x }}">X</a>. These are selected notes I want to keep easier to find, lightly edited so they make sense outside the original thread. They are dated because the tools change quickly, and so does my thinking.</p>
  </header>

  {% include writing-nav.html active="notes" %}

  <div>
    {% for note in site.data.x_notes %}
    {% unless note.archived %}
    <article class="note" id="{{ note.slug }}">
      <p class="meta"><time datetime="{{ note.datetime }}">{{ note.date }}</time><span>{{ note.theme }}</span></p>
      <div>
        <h2><a href="/notes/{{ note.slug }}/">{{ note.title }}</a></h2>
        <div class="note__body">
          {% for paragraph in note.paragraphs %}<p>{{ paragraph }}</p>{% endfor %}
          {% if note.update %}<p><strong>What I would add now:</strong> {{ note.update }} {% if note.update_url %}<a href="{{ note.update_url }}">Read the newer note on X.</a>{% endif %}</p>{% endif %}
        </div>
        <p class="note__foot"><a href="{{ note.url }}" rel="noopener noreferrer">Read the original and replies on X &nearr;</a></p>
      </div>
    </article>
    {% endunless %}
    {% endfor %}
  </div>
</div>
