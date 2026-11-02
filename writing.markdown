---
layout: default
title: Writing
description: "Essays on software development, applied AI, and machine learning, plus a regular digest."
---

<div class="wrap">
  <header class="page-head">
    <h1>Writing</h1>
    <p class="lead">Essays on software development, applied AI, and machine learning, plus a regular digest of what I'm trying, reading, and listening to.</p>
  </header>

  {% include writing-nav.html active="essays" %}

  <nav class="filters" aria-label="Filter by topic">
    <button data-category="recent" aria-pressed="true">Recent</button>
    <button data-category="featured" aria-pressed="false">Featured</button>
    <button data-category="Building with LLMs" aria-pressed="false">Building with LLMs</button>
    <button data-category="AI Strategy & Leadership" aria-pressed="false">AI strategy</button>
    <button data-category="Finance & Investing" aria-pressed="false">Finance</button>
    <button data-category="Getting Started with AI" aria-pressed="false">Getting started</button>
    <button data-category="Software Engineering" aria-pressed="false">Software engineering</button>
    <button data-category="Product & Strategy" aria-pressed="false">Product</button>
    <button data-category="Learning & Books" aria-pressed="false">Learning and books</button>
    <button data-category="Personal Reflections" aria-pressed="false">Personal</button>
    <button data-category="uncategorized" aria-pressed="false">Other</button>
    <button data-category="all" aria-pressed="false">All posts</button>
  </nav>

  <ul class="list list--writing">
    {% for post in site.posts %}
    <li class="list__row" data-index="{{ forloop.index0 }}" data-category="{{ post.category | default: 'uncategorized' }}" data-featured="{{ post.featured | default: false }}">
      <time class="meta" datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %-d, %Y" }}</time>
      <div>
        <a class="list__title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <p>{{ post.excerpt | strip_html | truncatewords: 22 }}</p>
      </div>
    </li>
    {% endfor %}
  </ul>
  <p class="show-all"><button type="button" data-show-all>Showing the 20 most recent of {{ site.posts.size }} posts. Show all</button></p>
</div>

<script>
(function () {
  var buttons = document.querySelectorAll('.filters button');
  var rows = document.querySelectorAll('.list--writing .list__row');
  function apply(category) {
    rows.forEach(function (row) {
      var show = category === 'all' ||
        (category === 'recent' && Number(row.dataset.index) < 20) ||
        (category === 'featured' && row.dataset.featured === 'true') ||
        row.dataset.category === category;
      row.classList.toggle('is-hidden', !show);
    });
  }
  var showAll = document.querySelector('[data-show-all]');
  function select(button) {
    buttons.forEach(function (b) { b.setAttribute('aria-pressed', String(b === button)); });
    apply(button.dataset.category);
    showAll.parentNode.hidden = button.dataset.category !== 'recent';
  }
  buttons.forEach(function (button) {
    button.addEventListener('click', function () { select(button); });
  });
  showAll.addEventListener('click', function () {
    select(document.querySelector('.filters [data-category="all"]'));
  });
  select(buttons[0]);
})();
</script>
