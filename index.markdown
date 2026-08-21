---
layout: splash
---

<style>
  .home-shell {
    max-width: 1040px;
    margin: 0 auto;
    padding: 0 1.5rem 4rem;
  }

  .home-hero {
    display: grid;
    grid-template-columns: minmax(0, 1fr) 220px;
    gap: 3.5rem;
    align-items: center;
    padding: 5rem 0 4rem;
    border-bottom: 1px solid var(--color-border);
  }

  .home-eyebrow {
    margin: 0 0 1rem;
    color: var(--color-primary);
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }

  .home-title {
    max-width: 760px;
    margin: 0 0 1.25rem;
    font-family: var(--font-serif);
    font-size: clamp(2.8rem, 6vw, 4.6rem);
    font-weight: 400;
    line-height: 1.02;
    letter-spacing: -0.035em;
  }

  .home-intro {
    max-width: 680px;
    margin: 0;
    color: var(--color-text-muted);
    font-size: 1.18rem;
    line-height: 1.65;
  }

  .home-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
    margin-top: 1.75rem;
  }

  .home-button {
    display: inline-flex;
    align-items: center;
    min-height: 44px;
    padding: 0.7rem 1.1rem;
    border: 1px solid var(--color-primary);
    border-radius: 6px;
    background: var(--color-primary);
    color: #fff !important;
    font-size: 0.95rem;
    font-weight: 650;
    text-decoration: none;
  }

  .page__content a.home-button {
    border-bottom: 1px solid var(--color-primary);
  }

  .home-button.secondary {
    background: transparent;
    color: var(--color-primary) !important;
  }

  .home-button:hover {
    transform: translateY(-1px);
    box-shadow: var(--shadow-md);
  }

  .home-photo {
    width: 220px;
    height: 220px;
    border-radius: 12px;
    object-fit: cover;
    box-shadow: 10px 10px 0 rgba(245, 166, 35, 0.2);
  }

  .home-section {
    padding: 3.75rem 0 0;
  }

  .home-section-header {
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    gap: 1rem;
    margin-bottom: 1.5rem;
  }

  .home-section h2 {
    margin: 0;
    font-family: var(--font-serif);
    font-size: 2.15rem;
    font-weight: 400;
    letter-spacing: -0.02em;
  }

  .home-section-link {
    color: var(--color-primary);
    font-size: 0.92rem;
    font-weight: 650;
    text-decoration: none;
  }

  .home-section-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem 1rem;
    justify-content: flex-end;
  }

  .home-post-list {
    border-top: 1px solid var(--color-border);
  }

  .home-post {
    display: grid;
    grid-template-columns: 120px minmax(0, 1fr);
    gap: 1.25rem;
    padding: 1.35rem 0;
    border-bottom: 1px solid var(--color-border);
  }

  .home-post time {
    color: var(--color-text-light);
    font-size: 0.82rem;
  }

  .home-post h3 {
    margin: 0 0 0.35rem;
    font-size: 1.08rem;
    line-height: 1.35;
  }

  .home-post h3 a {
    color: var(--color-text);
    text-decoration: none;
  }

  .home-post p {
    margin: 0;
    color: var(--color-text-muted);
    font-size: 0.96rem;
    line-height: 1.5;
  }

  .home-x-list {
    border-top: 1px solid var(--color-border);
  }

  .home-x-note {
    display: grid;
    grid-template-columns: 120px minmax(0, 1fr);
    gap: 1.25rem;
    padding: 1.2rem 0;
    border-bottom: 1px solid var(--color-border);
  }

  .home-x-meta {
    color: var(--color-text-light);
    font-size: 0.78rem;
    line-height: 1.5;
  }

  .home-x-theme {
    display: block;
    margin-top: 0.3rem;
    color: var(--color-primary);
    font-size: 0.66rem;
    font-weight: 700;
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }

  .home-x-note h3 {
    margin: 0 0 0.35rem;
    font-size: 1.08rem;
    line-height: 1.35;
  }

  .home-x-note h3 a {
    color: var(--color-text);
    border: 0 !important;
    text-decoration: none;
  }

  .home-x-note p {
    max-width: 720px;
    margin: 0;
    color: var(--color-text-muted);
    font-size: 0.94rem;
    line-height: 1.5;
  }

  .home-feature-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1rem;
  }

  .home-feature {
    display: flex;
    min-height: 210px;
    flex-direction: column;
    padding: 1.4rem;
    border: 1px solid var(--color-border);
    border-top: 3px solid var(--color-primary);
    border-radius: 10px;
    background: var(--color-surface);
  }

  .home-feature:nth-child(2) {
    border-top-color: var(--color-secondary);
  }

  /* An odd number of features leaves the last one alone in a two-up grid, so
     it takes the full width instead. Same move .fig:last-child makes on the
     listening index. Conditional, so the set can change size without this
     needing a second look. */
  .home-feature:last-child:nth-child(odd) {
    grid-column: 1 / -1;
    /* min-height exists to keep two tiles in a row the same height. A card
       with the row to itself has nothing to match, and at twice the width it
       holds its text in one line, so the floor just leaves a hole. */
    min-height: 0;
  }

  .home-feature-label {
    margin-bottom: 0.75rem;
    color: var(--color-text-light);
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  .home-feature h3 {
    margin: 0 0 0.65rem;
    font-size: 1.08rem;
    line-height: 1.35;
  }

  .home-feature p {
    margin: 0 0 1rem;
    color: var(--color-text-muted);
    font-size: 0.94rem;
    line-height: 1.55;
  }

  .home-feature a {
    margin-top: auto;
    color: var(--color-primary);
    font-size: 0.9rem;
    font-weight: 650;
    text-decoration: none;
  }

  .home-note {
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 2rem;
    align-items: center;
    padding: 1.75rem 2rem;
    border-radius: 10px;
    background: var(--color-surface-elevated);
    border-left: 3px solid var(--color-secondary);
  }

  .home-note p {
    margin: 0;
    color: var(--color-text-muted);
    line-height: 1.6;
  }

  @media (max-width: 760px) {
    .home-shell { padding: 0 1rem 3rem; }
    .home-hero {
      grid-template-columns: 1fr;
      gap: 2rem;
      padding: 3rem 0;
    }
    .home-photo {
      width: 150px;
      height: 150px;
      grid-row: 1;
    }
    .home-title { font-size: 2.8rem; }
    .home-feature-grid { grid-template-columns: 1fr; }
    .home-feature { min-height: 0; }
    .home-post { grid-template-columns: 1fr; gap: 0.35rem; }
    .home-x-note { grid-template-columns: 1fr; gap: 0.35rem; }
    .home-x-theme { display: inline; margin-left: 0.5rem; }
    .home-note { grid-template-columns: 1fr; gap: 1rem; padding: 1.5rem; }
    .home-section-header { align-items: flex-end; }
    .home-section-header--stack {
      flex-direction: column;
      align-items: flex-start;
      gap: 0.4rem;
    }
    .home-section-links { justify-content: flex-start; }
  }
</style>

<div class="home-shell">
  <section class="home-hero">
    <div>
      <p class="home-eyebrow">Software engineering, applied AI, and machine learning</p>
      <h1 class="home-title">I build software and write about what I learn.</h1>
      <p class="home-intro">I've spent more than 20 years building software and roughly a decade working in ML and AI. I publish longer pieces here. Most of my day-to-day thinking happens <a href="https://x.com/mstockton">on X</a>, where I share working ideas and practical things I'm trying.</p>
      <div class="home-actions">
        <a class="home-button" href="/writing.html">Read the writing</a>
        <a class="home-button secondary" href="https://pragmanexus.com">Work with me through PragmaNexus</a>
      </div>
    </div>
    <img class="home-photo" src="/docs/assets/images/matt.jpeg" alt="Matt Stockton">
  </section>

  <section class="home-section">
    <div class="home-section-header">
      <h2>Working notes</h2>
      <div class="home-section-links">
        <a class="home-section-link" href="/notes.html">All notes &rarr;</a>
        <a class="home-section-link" href="https://x.com/mstockton">Follow on X &rarr;</a>
      </div>
    </div>
    <div class="home-x-list">
      {% assign featured_notes = site.data.x_notes | where: "featured", true %}
      {% for note in featured_notes %}
      <article class="home-x-note">
        <div class="home-x-meta">
          <time datetime="{{ note.datetime }}">{{ note.date }}</time>
          <span class="home-x-theme">{{ note.theme }}</span>
        </div>
        <div>
          <h3><a href="/notes/{{ note.slug }}/">{{ note.title }}</a></h3>
          <p>{{ note.summary }}</p>
        </div>
      </article>
      {% endfor %}
    </div>
  </section>

  <section class="home-section">
    <div class="home-section-header">
      <h2>Recent writing</h2>
      <a class="home-section-link" href="/writing.html">All posts &rarr;</a>
    </div>
    <div class="home-post-list">
      {% for post in site.posts limit:5 %}
      <article class="home-post">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %-d, %Y" }}</time>
        <div>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          <p>{{ post.excerpt | strip_html | truncatewords: 24 }}</p>
        </div>
      </article>
      {% endfor %}
    </div>
  </section>

  <section class="home-section">
    <div class="home-section-header home-section-header--stack">
      <h2>Experiments and conversations</h2>
      <a class="home-section-link" href="/experiments.html">All experiments &rarr;</a>
    </div>
    <div class="home-feature-grid">
      {% assign featured_experiments = site.data.experiments | where: "featured", true %}
      {% for item in featured_experiments limit:5 %}
      <article class="home-feature">
        <div class="home-feature-label">{{ item.kind }}</div>
        <h3>{{ item.title }}</h3>
        <p>{{ item.short | default: item.summary }}</p>
        <a href="{{ item.url }}"{% if item.external %} rel="noopener noreferrer"{% endif %}>{% if item.cta %}{{ item.cta }}{% if item.external %} &nearr;{% else %} &rarr;{% endif %}{% elsif item.external %}Explore {{ item.title }} &nearr;{% else %}Open the page &rarr;{% endif %}</a>
      </article>
      {% endfor %}
    </div>
  </section>

  <section class="home-section">
    <div class="home-note">
      <p>I do client work through <strong>PragmaNexus</strong>. Its site has services, case studies, and contact information.</p>
      <a class="home-section-link" href="https://pragmanexus.com">Visit PragmaNexus &rarr;</a>
    </div>
  </section>
</div>
