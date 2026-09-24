---
layout: splash
title: Writing
digest_styles: true
classes:
  - wide
---

<style>
  .writing-page {
    max-width: var(--site-width);
    margin: 0 auto;
    padding: var(--page-top) var(--page-gutter) 3rem;
  }

  .writing-header {
    padding-bottom: 2rem;
    border-bottom: 1px solid var(--color-border);
  }

  .writing-header h1 {
    margin: 0 0 1rem;
    font-family: var(--font-serif);
    font-size: var(--type-title);
    font-weight: 400;
    line-height: 1;
    letter-spacing: -0.035em;
  }

  .writing-header p {
    max-width: 640px;
    margin: 0 !important;
    color: var(--color-text-muted);
    font-size: 1.08rem;
    line-height: 1.6;
  }

  .writing-header a {
    color: var(--color-primary) !important;
    border-bottom: 1px solid rgba(10, 77, 104, 0.3) !important;
    text-decoration: none !important;
  }

  .category-nav {
    display: flex;
    gap: 0.45rem;
    margin: 0;
    padding: 1.5rem 0;
    overflow-x: auto;
    border-bottom: 1px solid var(--color-border);
    -webkit-overflow-scrolling: touch;
    scrollbar-width: thin;
  }

  .category-button {
    flex-shrink: 0;
    padding: 0.42rem 0.72rem;
    border: 1px solid var(--color-border);
    border-radius: 999px;
    background: transparent;
    color: var(--color-text-muted);
    font-family: var(--font-body);
    font-size: 0.73rem;
    font-weight: 600;
    line-height: 1.2;
    white-space: nowrap;
    cursor: pointer;
    transition: border-color var(--transition-fast), color var(--transition-fast), background var(--transition-fast);
  }

  .category-button:hover {
    border-color: var(--color-primary);
    color: var(--color-primary);
  }

  .category-button.active {
    border-color: var(--color-primary);
    background: var(--color-primary);
    color: #fff;
  }

  .all-posts {
    border-top: 0;
  }

  .post-item {
    display: grid;
    grid-template-columns: 150px minmax(0, 1fr);
    gap: 1.75rem;
    padding: 1.6rem 0;
    border-bottom: 1px solid var(--color-border);
  }

  .post-meta {
    color: var(--color-text-light);
    font-size: 0.76rem;
    line-height: 1.45;
  }

  .post-category {
    display: block;
    margin-top: 0.4rem;
    color: var(--color-primary);
    font-size: 0.68rem;
    font-weight: 700;
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }

  .featured-badge {
    display: inline-block;
    margin-top: 0.5rem;
    padding: 0.12rem 0.4rem;
    border-radius: 4px;
    background: rgba(245, 166, 35, 0.18);
    color: var(--color-text);
    font-size: 0.62rem;
    font-weight: 700;
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }

  .post-body h2 {
    margin: 0 0 0.4rem !important;
    padding: 0 !important;
    border: 0 !important;
    font-family: var(--font-display);
    font-size: 1.06rem !important;
    font-weight: 650;
    line-height: 1.35;
  }

  .post-body h2 a {
    color: var(--color-text) !important;
    text-decoration: none !important;
    border: 0 !important;
  }

  .post-body h2 a:hover {
    color: var(--color-primary) !important;
  }

  .post-excerpt {
    margin: 0 !important;
    color: var(--color-text-muted);
    font-size: 0.9rem;
    line-height: 1.55;
  }

  .hidden {
    display: none !important;
  }

  @media (max-width: 700px) {
    .writing-page { padding: var(--page-top) var(--page-gutter) 3rem; }
    .writing-header { padding-bottom: 2.25rem; }
    .writing-header h1 { font-size: var(--type-title); }
    .post-item { grid-template-columns: 1fr; gap: 0.55rem; padding: 1.35rem 0; }
    .post-meta { display: flex; flex-wrap: wrap; gap: 0.5rem; align-items: center; }
    .post-category, .featured-badge { display: inline-block; margin-top: 0; }
  }
</style>

<div class="writing-page">
  <header class="writing-header">
    <h1>Writing</h1>
    <p>Essays on software development, applied AI, and machine learning, plus a regular digest of what I’m trying, reading, and listening to.</p>
  </header>

  {% include writing-nav.html active="essays" %}

  <nav class="category-nav" aria-label="Filter writing by category">
    <button class="category-button active" data-category="recent" aria-pressed="true">Recent</button>
    <button class="category-button" data-category="all" aria-pressed="false">All posts</button>
    <button class="category-button" data-category="featured" aria-pressed="false">Featured</button>
    <button class="category-button" data-category="Getting Started with AI" aria-pressed="false">Getting started</button>
    <button class="category-button" data-category="Building with LLMs" aria-pressed="false">Building with LLMs</button>
    <button class="category-button" data-category="AI Strategy & Leadership" aria-pressed="false">AI strategy</button>
    <button class="category-button" data-category="Finance & Investing" aria-pressed="false">Finance</button>
    <button class="category-button" data-category="Product & Strategy" aria-pressed="false">Product</button>
    <button class="category-button" data-category="Software Engineering" aria-pressed="false">Software engineering</button>
    <button class="category-button" data-category="Learning & Books" aria-pressed="false">Learning and books</button>
    <button class="category-button" data-category="Personal Reflections" aria-pressed="false">Personal</button>
    <button class="category-button" data-category="uncategorized" aria-pressed="false">Other</button>
  </nav>

  <div class="all-posts">
    {% for post in site.posts %}
    <article class="post-item" data-index="{{ forloop.index0 }}" data-category="{{ post.category | default: 'uncategorized' }}" data-featured="{{ post.featured | default: false }}">
      <div class="post-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %-d, %Y" }}</time>
        <span class="post-category">{{ post.category | default: "Other" }}</span>
        {% if post.featured %}<span class="featured-badge">Featured</span>{% endif %}
      </div>
      <div class="post-body">
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      </div>
    </article>
    {% endfor %}
  </div>
</div>

<script>
let activeCategory = 'recent';

document.addEventListener('DOMContentLoaded', function() {
  const categoryButtons = document.querySelectorAll('.category-button');

  categoryButtons.forEach(button => {
    button.addEventListener('click', function(e) {
      e.preventDefault();
      activeCategory = this.getAttribute('data-category');

      categoryButtons.forEach(btn => {
        btn.classList.remove('active');
        btn.setAttribute('aria-pressed', 'false');
      });
      this.classList.add('active');
      this.setAttribute('aria-pressed', 'true');

      filterPosts();
    });
  });

  filterPosts();
});

function filterPosts() {
  document.querySelectorAll('.post-item').forEach(post => {
    const postCategory = post.getAttribute('data-category');
    const postFeatured = post.getAttribute('data-featured') === 'true';
    const postIndex = Number(post.getAttribute('data-index'));
    const showPost = (activeCategory === 'recent' && postIndex < 20) ||
      activeCategory === 'all' ||
      (activeCategory === 'featured' && postFeatured) ||
      postCategory === activeCategory;

    post.classList.toggle('hidden', !showPost);
  });
}
</script>
