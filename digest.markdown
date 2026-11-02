---
layout: default
title: Digest
permalink: /writing/digest/
description: "What I'm writing, trying, reading, and listening to. A regular digest by Matt Stockton."
---

<div class="wrap">
  <header class="page-head">
    <h1>Digest</h1>
    <p class="lead">What I'm writing, trying, reading, and listening to, with a little context on why it caught my attention. Follow it <a href="{{ '/writing/digest/feed.xml' | relative_url }}">via RSS</a>.</p>
  </header>

  {% include writing-nav.html active="digest" %}

  {% assign issues = site.digests | sort: "date" | reverse %}
  {% assign years = issues | group_by_exp: "issue", "issue.date | date: '%Y'" %}
  {% for year in years %}
  <section class="digest-year" aria-labelledby="year-{{ year.name }}">
    <h2 class="meta" id="year-{{ year.name }}">{{ year.name }}</h2>
    <ul class="list">
      {% for issue in year.items %}
      <li class="list__row">
        <a class="list__title" href="{{ issue.url | relative_url }}"><time datetime="{{ issue.date | date_to_xmlschema }}">{{ issue.date | date: "%B %-d" }}</time></a>
        <p>{{ issue.excerpt | strip_html }}</p>
      </li>
      {% endfor %}
    </ul>
  </section>
  {% endfor %}
</div>
