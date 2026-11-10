---
layout: default
title: Projects
permalink: /experiments.html
description: "Things I built to answer a question I had. Each one is a working page you can open and use."
---

<div class="wrap">
  <header class="page-head">
        <h1>Projects</h1>
    <p class="lead">Things I built to answer a question I had. Most started as a dataset I wanted to understand or an argument I wanted to see laid out, and each one is a working page you can open and use. I write about how they were built in <a href="{{ '/writing.html' | relative_url }}">the writing</a>.</p>
  </header>

  <div class="project-list">
    {% assign projects = site.data.experiments | where_exp: "item", "item.type != 'appearance'" | sort: "datetime" | reverse %}
    {% for item in projects %}
    <article class="project-row" id="{{ item.slug }}">
      {% if item.preview %}
      <a class="project__image" href="{{ item.url }}"{% if item.external %} rel="noopener noreferrer"{% endif %} tabindex="-1" aria-hidden="true">
        <img src="{{ item.preview }}" alt="" loading="lazy" width="1200" height="630">
      </a>
      {% endif %}
      <div>
        <p class="meta">{{ item.kind }} &middot; {{ item.date }}</p>
        <h2><a href="{{ item.url }}"{% if item.external %} rel="noopener noreferrer"{% endif %}>{{ item.title }}</a></h2>
        <p>{{ item.short | default: item.summary }}</p>
        {% if item.built_with %}<p class="meta built">Built with {{ item.built_with }}</p>{% endif %}
        <div class="actions">
          <a class="text-link" href="{{ item.url }}"{% if item.external %} rel="noopener noreferrer"{% endif %}>{% if item.cta %}{{ item.cta }}{% elsif item.external %}Explore {{ item.title }}{% else %}Open the page{% endif %} {% if item.external %}&nearr;{% else %}&rarr;{% endif %}</a>
          {% if item.video_url %}<a class="text-link" href="{{ item.video_url }}" rel="noopener noreferrer">{{ item.video_cta | default: "Watch the film" }} &nearr;</a>{% endif %}
          {% if item.post_url %}<a class="text-link" href="{{ item.post_url }}">Read the post &rarr;</a>{% endif %}
        </div>
      </div>
    </article>
    {% endfor %}
  </div>

  {% assign appearances = site.data.experiments | where: "type", "appearance" %}
  {% if appearances.size > 0 %}
  <section class="elsewhere" aria-labelledby="elsewhere-heading">
    <div class="section-head"><h2 id="elsewhere-heading">Elsewhere</h2></div>
    <ul class="list">
      {% for item in appearances %}
      <li class="list__row">
        <span class="meta">{{ item.kind }} &middot; {{ item.date }}</span>
        <div>
          <a class="list__title" href="{{ item.url }}"{% if item.external %} rel="noopener noreferrer"{% endif %}>{{ item.title }}</a>
          <p>{{ item.short | default: item.summary }}</p>
        </div>
      </li>
      {% endfor %}
    </ul>
  </section>
  {% endif %}
</div>
