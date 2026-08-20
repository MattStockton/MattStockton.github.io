---
layout: splash
title: Experiments
permalink: /experiments.html
classes:
  - wide
---

<style>
  .experiments-page {
    max-width: 1040px;
    margin: 0 auto;
    padding: 4.5rem 1.5rem 4rem;
  }

  .experiments-header {
    padding-bottom: 3rem;
    border-bottom: 1px solid var(--color-border);
  }

  .experiments-header h1 {
    margin: 0 0 1rem;
    font-family: var(--font-serif);
    font-size: clamp(3rem, 6vw, 4.5rem);
    font-weight: 400;
    line-height: 1;
    letter-spacing: -0.035em;
  }

  .experiments-header p {
    max-width: 660px;
    margin: 0 !important;
    color: var(--color-text-muted);
    font-size: 1.08rem;
    line-height: 1.6;
  }

  .experiments-header a {
    color: var(--color-primary) !important;
    border-bottom: 1px solid rgba(10, 77, 104, 0.3) !important;
    text-decoration: none !important;
  }

  .experiment-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 2rem;
    padding: 2.75rem 0 0;
  }

  .experiment {
    display: flex;
    flex-direction: column;
    overflow: hidden;
    border: 1px solid var(--color-border);
    border-radius: 10px;
    background: var(--color-surface);
    transition: border-color var(--transition-fast), box-shadow var(--transition-fast);
  }

  .experiment:hover {
    border-color: var(--color-border-hover);
    box-shadow: var(--shadow-md);
  }

  .experiment-thumb {
    display: block;
    border-bottom: 1px solid var(--color-border);
  }

  .experiment-thumb img {
    display: block;
    width: 100%;
    height: auto;
    aspect-ratio: 1200 / 630;
    object-fit: cover;
  }

  .experiment-body {
    display: flex;
    flex: 1;
    flex-direction: column;
    padding: 1.5rem;
  }

  .experiment-meta {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    align-items: baseline;
    margin-bottom: 0.7rem;
    color: var(--color-text-light);
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  .experiment-kind {
    color: var(--color-primary);
  }

  .experiment-meta::before {
    display: none;
  }

  .experiment h2 {
    margin: 0 0 0.6rem !important;
    padding: 0 !important;
    border: 0 !important;
    font-family: var(--font-serif);
    font-size: 1.85rem !important;
    font-weight: 400;
    line-height: 1.1;
    letter-spacing: -0.02em;
  }

  .experiment h2 a {
    color: var(--color-text) !important;
    border: 0 !important;
    text-decoration: none !important;
  }

  .experiment h2 a:hover {
    color: var(--color-primary) !important;
  }

  .experiment-summary {
    margin: 0 0 1.25rem !important;
    color: var(--color-text-muted);
    font-size: 0.95rem;
    line-height: 1.6;
  }

  .experiment-notes {
    margin: 0 0 1.25rem;
    padding: 0.9rem 1rem;
    border-left: 3px solid var(--color-secondary);
    background: var(--color-surface-elevated);
  }

  .experiment-notes p {
    margin: 0 0 0.5rem !important;
    color: var(--color-text-muted);
    font-size: 0.85rem;
    line-height: 1.55;
  }

  .experiment-notes p:last-child {
    margin-bottom: 0 !important;
  }

  .experiment-notes strong {
    color: var(--color-text);
    font-size: 0.68rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  .experiment-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem 1.25rem;
    margin-top: auto;
    padding-top: 0.25rem;
  }

  .experiment-links a {
    color: var(--color-primary) !important;
    border: 0 !important;
    font-size: 0.9rem;
    font-weight: 650;
    text-decoration: none !important;
  }

  .experiment-links a:hover {
    border-bottom: 1px solid var(--color-primary) !important;
  }

  .experiments-elsewhere {
    padding: 3.5rem 0 0;
  }

  .experiments-elsewhere h2 {
    margin: 0 0 1.25rem !important;
    padding: 0 !important;
    border: 0 !important;
    font-family: var(--font-serif);
    font-size: 2.15rem !important;
    font-weight: 400;
    letter-spacing: -0.02em;
  }

  .elsewhere-item {
    display: grid;
    grid-template-columns: 150px minmax(0, 1fr);
    gap: 2rem;
    padding: 1.5rem 0;
    border-top: 1px solid var(--color-border);
  }

  .elsewhere-meta {
    color: var(--color-text-light);
    font-size: 0.76rem;
    line-height: 1.45;
  }

  .elsewhere-kind {
    display: block;
    margin-top: 0.4rem;
    color: var(--color-primary);
    font-size: 0.68rem;
    font-weight: 700;
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }

  .elsewhere-item h3 {
    margin: 0 0 0.35rem !important;
    font-family: var(--font-display);
    font-size: 1.06rem !important;
    font-weight: 650;
    line-height: 1.35;
  }

  .elsewhere-item h3 a {
    color: var(--color-text) !important;
    border: 0 !important;
    text-decoration: none !important;
  }

  .elsewhere-item h3 a:hover {
    color: var(--color-primary) !important;
  }

  .elsewhere-item p {
    margin: 0 !important;
    color: var(--color-text-muted);
    font-size: 0.9rem;
    line-height: 1.55;
  }

  @media (max-width: 820px) {
    .experiments-page { padding: 3rem 1rem; }
    .experiments-header { padding-bottom: 2.25rem; }
    .experiments-header h1 { font-size: 3rem; }
    .experiment-grid { grid-template-columns: 1fr; gap: 1.5rem; }
    .experiment h2 { font-size: 1.6rem !important; }
    .elsewhere-item { grid-template-columns: 1fr; gap: 0.5rem; }
    .elsewhere-kind { display: inline; margin-top: 0; margin-left: 0.5rem; }
  }
</style>

<div class="experiments-page">
  <header class="experiments-header">
    <h1>Experiments</h1>
    <p>Things I built to answer a question I had. Most started as a dataset I wanted to understand or an argument I wanted to see laid out, and each one is a working page you can open and use. I write about how they were built over in <a href="/writing.html">the writing</a>.</p>
  </header>

  <div class="experiment-grid">
    {% assign experiments = site.data.experiments | where_exp: "item", "item.type != 'appearance'" %}
    {% for item in experiments %}
    <article class="experiment" id="{{ item.slug }}">
      {% if item.preview %}
      <a class="experiment-thumb" href="{{ item.url }}"{% if item.external %} rel="noopener noreferrer"{% endif %}>
        <img src="{{ item.preview }}" alt="{{ item.preview_alt | default: item.title }}" loading="lazy" width="1200" height="630">
      </a>
      {% endif %}
      <div class="experiment-body">
        <div class="experiment-meta">
          <span class="experiment-kind">{{ item.kind }}</span>
          <time datetime="{{ item.datetime }}">{{ item.date }}</time>
        </div>
        <h2><a href="{{ item.url }}"{% if item.external %} rel="noopener noreferrer"{% endif %}>{{ item.title }}</a></h2>
        <p class="experiment-summary">{{ item.summary }}</p>

        {% if item.data or item.built_with %}
        <div class="experiment-notes">
          {% if item.data %}<p><strong>Data</strong><br>{{ item.data }}</p>{% endif %}
          {% if item.built_with %}<p><strong>Built with</strong><br>{{ item.built_with }}</p>{% endif %}
        </div>
        {% endif %}

        <div class="experiment-links">
          <a href="{{ item.url }}"{% if item.external %} rel="noopener noreferrer"{% endif %}>{% if item.external %}Open {{ item.title }} &nearr;{% else %}Open the page &rarr;{% endif %}</a>
          {% if item.post_url %}<a href="{{ item.post_url }}">Read the post &rarr;</a>{% endif %}
        </div>
      </div>
    </article>
    {% endfor %}
  </div>

  {% assign appearances = site.data.experiments | where: "type", "appearance" %}
  {% if appearances.size > 0 %}
  <section class="experiments-elsewhere">
    <h2>Elsewhere</h2>
    {% for item in appearances %}
    <article class="elsewhere-item">
      <div class="elsewhere-meta">
        <time datetime="{{ item.datetime }}">{{ item.date }}</time>
        <span class="elsewhere-kind">{{ item.kind }}</span>
      </div>
      <div>
        <h3><a href="{{ item.url }}"{% if item.external %} rel="noopener noreferrer"{% endif %}>{{ item.title }}</a></h3>
        <p>{{ item.summary }}</p>
      </div>
    </article>
    {% endfor %}
  </section>
  {% endif %}
</div>
