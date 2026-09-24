---
layout: splash
title: Digest
permalink: /writing/digest/
description: "What I'm writing, trying, reading, and listening to. A regular digest by Matt Stockton."
digest_styles: true
---

<div class="digest-archive">
  <header class="digest-archive__header">
    <p class="digest-eyebrow">Writing</p>
    <h1>Digest</h1>
    <p>What I’m writing, trying, reading, and listening to, with a little context on why it caught my attention.</p>
  </header>

  {% include writing-nav.html active="digest" %}

  {% assign issues = site.digests | sort: "date" | reverse %}
  {% assign years = issues | group_by_exp: "issue", "issue.date | date: '%Y'" %}
  {% for year in years %}
  <section class="digest-year" aria-labelledby="year-{{ year.name }}">
    <h2 id="year-{{ year.name }}">{{ year.name }}</h2>
    <div>
      {% for issue in year.items %}
      <article class="digest-archive__issue">
        <h3><a href="{{ issue.url | relative_url }}"><time datetime="{{ issue.date | date_to_xmlschema }}">{{ issue.date | date: "%B %-d" }}</time></a></h3>
        <p>{{ issue.excerpt | strip_html }}</p>
        <a class="digest-read" href="{{ issue.url | relative_url }}" aria-label="Read the {{ issue.date | date: '%B %-d, %Y' }} digest">Read this issue <span aria-hidden="true">&rarr;</span></a>
      </article>
      {% endfor %}
    </div>
  </section>
  {% endfor %}

  <footer class="digest-archive__footer">
    <a href="{{ '/writing/digest/feed.xml' | relative_url }}">Follow the digest via RSS <span aria-hidden="true">&rarr;</span></a>
    <span>Looking for a longer read? <a href="{{ '/writing.html' | relative_url }}">Browse the essays.</a></span>
  </footer>
</div>
