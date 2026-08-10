---
layout: splash
title: Notes
permalink: /notes.html
classes:
  - wide
---

<style>
  .notes-page {
    max-width: 1040px;
    margin: 0 auto;
    padding: 4.5rem 1.5rem 4rem;
  }

  .notes-header {
    display: grid;
    grid-template-columns: minmax(0, 1fr) auto;
    gap: 2rem;
    align-items: end;
    padding-bottom: 3rem;
    border-bottom: 1px solid var(--color-border);
  }

  .notes-header h1 {
    margin: 0 0 1rem;
    font-family: var(--font-serif);
    font-size: clamp(3rem, 6vw, 4.5rem);
    font-weight: 400;
    line-height: 1;
    letter-spacing: -0.035em;
  }

  .notes-header p {
    max-width: 680px;
    margin: 0 !important;
    color: var(--color-text-muted);
    font-size: 1.08rem;
    line-height: 1.6;
  }

  .notes-follow {
    display: inline-flex;
    min-height: 44px;
    align-items: center;
    padding: 0.7rem 1rem;
    border: 1px solid var(--color-primary) !important;
    border-radius: 6px;
    color: var(--color-primary) !important;
    font-size: 0.92rem;
    font-weight: 650;
    text-decoration: none !important;
    white-space: nowrap;
  }

  .notes-list {
    border-top: 0;
  }

  .x-note {
    display: grid;
    grid-template-columns: 150px minmax(0, 1fr);
    gap: 2rem;
    padding: 1.75rem 0;
    border-bottom: 1px solid var(--color-border);
  }

  .x-note-meta {
    color: var(--color-text-light);
    font-size: 0.78rem;
    line-height: 1.5;
  }

  .x-note-theme {
    display: block;
    margin-top: 0.45rem;
    color: var(--color-primary);
    font-size: 0.68rem;
    font-weight: 700;
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }

  .x-note-body {
    max-width: 720px;
  }

  .x-note h2 {
    margin: 0 0 1rem !important;
    padding: 0 !important;
    border: 0 !important;
    font-family: var(--font-serif);
    font-size: 1.6rem !important;
    font-weight: 400;
    letter-spacing: -0.02em;
    line-height: 1.15;
  }

  .x-note h2 a {
    color: inherit;
    border-bottom: 0;
  }

  .x-note h2 a:hover {
    color: var(--color-primary);
  }

  .x-note-text p {
    margin: 0 0 0.9rem !important;
    color: var(--color-text);
    font-size: 0.92rem;
    line-height: 1.62;
  }

  .x-note-update {
    margin: 1.1rem 0 !important;
    padding: 0.9rem 1rem;
    border-left: 3px solid var(--color-secondary);
    background: var(--color-surface-elevated);
    color: var(--color-text-muted);
    font-size: 0.9rem;
    line-height: 1.55;
  }

  .x-note-link {
    display: inline-block;
    margin-top: 0.35rem;
    color: var(--color-primary) !important;
    border-bottom: 1px solid rgba(10, 77, 104, 0.3) !important;
    font-size: 0.9rem;
    font-weight: 650;
    text-decoration: none !important;
  }

  @media (max-width: 720px) {
    .notes-page { padding: 3rem 1rem; }
    .notes-header { grid-template-columns: 1fr; gap: 1.5rem; padding-bottom: 2.25rem; }
    .notes-header h1 { font-size: 3rem; }
    .notes-follow { justify-self: start; }
    .x-note { grid-template-columns: 1fr; gap: 0.75rem; padding: 1.75rem 0; }
    .x-note-theme { display: inline; margin-left: 0.5rem; }
    .x-note h2 { font-size: 1.6rem !important; }
  }
</style>

<div class="notes-page">
  <header class="notes-header">
    <div>
      <h1>Notes</h1>
      <p>Most of my shorter writing happens on X. These are selected notes I want to keep easier to find. I have lightly edited them so they make sense outside the original thread. They are dated because the tools change quickly, and so does my thinking.</p>
    </div>
    <a class="notes-follow" href="https://x.com/mstockton">Follow @mstockton on X &rarr;</a>
  </header>

  <div class="notes-list">
    {% for note in site.data.x_notes %}
    <article class="x-note" id="{{ note.slug }}">
      <div class="x-note-meta">
        <time datetime="{{ note.datetime }}">{{ note.date }}</time>
        <span class="x-note-theme">{{ note.theme }}</span>
      </div>
      <div class="x-note-body">
        <h2><a href="/notes/{{ note.slug }}/">{{ note.title }}</a></h2>
        <div class="x-note-text">
          {% for paragraph in note.paragraphs %}
          <p>{{ paragraph }}</p>
          {% endfor %}
        </div>
        {% if note.update %}
        <p class="x-note-update"><strong>Update:</strong> {{ note.update }} <a href="{{ note.update_url }}">Read the newer note on X.</a></p>
        {% endif %}
        <a class="x-note-link" href="{{ note.url }}">Read the original and replies on X &rarr;</a>
      </div>
    </article>
    {% endfor %}
  </div>
</div>
