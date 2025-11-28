---
layout: splash
classes:
  - wide
---

<style>
  /* =================================================================
     WRITING ARCHIVE - Refined Tech Design
     ================================================================= */

  /* Main Container */
  .page__content,
  .archive,
  #main {
    max-width: 1200px !important;
    margin-left: auto !important;
    margin-right: auto !important;
    float: none !important;
    width: 100% !important;
  }

  #main {
    padding: 0 1rem !important;
  }

  /* Page Header */
  .page-header {
    text-align: center;
    padding: 3rem 1rem 2rem;
    background: var(--gradient-hero);
    margin: -2rem -1rem 0;
    position: relative;
  }

  .page-header::before {
    content: '';
    position: absolute;
    inset: 0;
    background-image: radial-gradient(circle at 30% 40%, rgba(30, 58, 95, 0.05) 0%, transparent 50%);
    pointer-events: none;
  }

  .page-header h1 {
    font-family: var(--font-display);
    font-size: 2.5rem;
    font-weight: 800;
    color: var(--color-text);
    margin-bottom: 0.5rem;
    letter-spacing: -0.03em;
    position: relative;
  }

  .page-header p {
    font-size: 1.15rem;
    color: var(--color-text-muted);
    max-width: 600px;
    margin: 0 auto;
    position: relative;
  }

  /* Content Container */
  .content-container {
    margin-top: 1.5rem;
    padding: 2rem;
    background: var(--color-surface);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-lg);
    box-shadow: var(--shadow-md);
  }

  /* Category Navigation - Compact Horizontal Scroll */
  .category-nav {
    display: flex;
    flex-wrap: nowrap;
    gap: 0.4rem;
    margin-bottom: 1.25rem;
    padding-bottom: 0.75rem;
    border-bottom: 1px solid var(--color-border);
    overflow-x: auto;
    -webkit-overflow-scrolling: touch;
    scrollbar-width: thin;
  }

  .category-nav::-webkit-scrollbar {
    height: 3px;
  }

  .category-nav::-webkit-scrollbar-track {
    background: var(--color-surface-elevated);
    border-radius: 2px;
  }

  .category-nav::-webkit-scrollbar-thumb {
    background: var(--color-border);
    border-radius: 2px;
  }

  .category-nav:hover::-webkit-scrollbar-thumb {
    background: var(--color-border-hover);
  }

  .category-button {
    font-family: var(--font-display);
    padding: 0.35rem 0.75rem;
    background: var(--color-surface);
    color: var(--color-text-muted);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-xl);
    text-decoration: none;
    font-size: 0.8rem;
    font-weight: 500;
    transition: all var(--transition-base);
    cursor: pointer;
    flex-shrink: 0;
    white-space: nowrap;
  }

  .category-button:hover {
    border-color: var(--color-primary);
    color: var(--color-primary);
    background: rgba(30, 58, 95, 0.05);
  }

  .category-button.active {
    background: var(--gradient-accent);
    color: white !important;
    border-color: transparent;
    box-shadow: 0 2px 8px rgba(30, 58, 95, 0.25);
  }

  /* Featured Badge */
  .featured-badge {
    background: var(--color-secondary);
    color: var(--color-text);
    padding: 0.15rem 0.5rem;
    border-radius: var(--radius-xl);
    font-size: 0.7rem;
    font-weight: 600;
    margin-left: 0.5rem;
    text-transform: uppercase;
    letter-spacing: 0.02em;
  }

  /* All Posts Section */
  .all-posts {
    display: grid;
    gap: 1rem;
  }

  .post-item {
    background: var(--color-surface);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-md);
    padding: 1.5rem 1.75rem;
    transition: all var(--transition-base);
  }

  .post-item:hover {
    border-color: var(--color-primary);
    box-shadow: var(--shadow-hover);
    transform: translateY(-2px);
  }

  .post-item h3 {
    margin: 0 0 0.5rem 0 !important;
    font-size: 1.15rem !important;
    font-family: var(--font-display);
    font-weight: 600;
    line-height: 1.35;
  }

  .post-item h3 a {
    color: var(--color-text) !important;
    text-decoration: none !important;
    transition: color var(--transition-fast);
  }

  .post-item:hover h3 a {
    color: var(--color-primary) !important;
  }

  .post-meta {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 0.75rem !important;
    font-size: 0.85rem !important;
    color: var(--color-text-muted) !important;
  }

  .post-category {
    display: inline-block;
    background: var(--color-surface-elevated);
    color: var(--color-primary);
    padding: 0.2rem 0.6rem;
    border-radius: var(--radius-xl);
    font-size: 0.75rem;
    font-weight: 500;
  }

  .post-excerpt {
    display: block !important;
    margin: 0 !important;
    font-size: 0.95rem !important;
    color: var(--color-text-muted) !important;
    line-height: 1.6 !important;
  }

  /* Hidden class for filtering */
  .hidden {
    display: none !important;
  }

  /* Responsive */
  @media (max-width: 768px) {
    .page-header {
      padding: 2rem 1rem 1.5rem;
    }

    .page-header h1 {
      font-size: 2rem;
    }

    .content-container {
      padding: 1.5rem;
      margin-top: 1.5rem;
    }

    .post-item {
      padding: 1.25rem;
    }

    .post-item h3 {
      font-size: 1.05rem !important;
    }
  }
</style>

<!-- Page Header -->
<div class="page-header">
  <h1>Writing</h1>
  <p>Practical insights on building AI solutions, software engineering, and strategy.</p>
</div>

<div class="content-container">
  <!-- Category Navigation -->
  <div class="category-nav">
    <button class="category-button active" data-category="all">All Posts</button>
    <button class="category-button" data-category="featured">Featured</button>
    <button class="category-button" data-category="Getting Started with AI">Getting Started with AI</button>
    <button class="category-button" data-category="Building with LLMs">Building with LLMs</button>
    <button class="category-button" data-category="AI Strategy & Leadership">AI Strategy</button>
    <button class="category-button" data-category="Finance & Investing">Finance & Investing</button>
    <button class="category-button" data-category="Product & Strategy">Product & Strategy</button>
    <button class="category-button" data-category="Software Engineering">Software Engineering</button>
    <button class="category-button" data-category="Learning & Books">Learning & Books</button>
    <button class="category-button" data-category="Personal Reflections">Personal</button>
    <button class="category-button" data-category="uncategorized">Other</button>
  </div>

  <!-- All Posts Section -->
  <div class="all-posts">
    {% for post in site.posts %}
    <article class="post-item" data-category="{{ post.category | default: 'uncategorized' }}" data-featured="{{ post.featured | default: false }}">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <div class="post-meta">
        {{ post.date | date: "%B %d, %Y" }}
        <span class="post-category">{{ post.category | default: "Other" }}</span>
        {% if post.featured %}
        <span class="featured-badge">Featured</span>
        {% endif %}
      </div>
      <div class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</div>
    </article>
    {% endfor %}
  </div>
</div>

<script>
let activeCategory = 'all';

document.addEventListener('DOMContentLoaded', function() {
  const categoryButtons = document.querySelectorAll('.category-button');

  categoryButtons.forEach(button => {
    button.addEventListener('click', function(e) {
      e.preventDefault();
      e.stopPropagation();
      this.blur();
      activeCategory = this.getAttribute('data-category');

      categoryButtons.forEach(btn => btn.classList.remove('active'));
      this.classList.add('active');

      filterPosts();
    });
  });
});

function filterPosts() {
  const postItems = document.querySelectorAll('.post-item');

  postItems.forEach(post => {
    const postCategory = post.getAttribute('data-category');
    const postFeatured = post.getAttribute('data-featured') === 'true';

    let categoryMatch = false;
    if (activeCategory === 'all') {
      categoryMatch = true;
    } else if (activeCategory === 'featured') {
      categoryMatch = postFeatured;
    } else {
      categoryMatch = postCategory === activeCategory;
    }

    if (categoryMatch) {
      post.classList.remove('hidden');
    } else {
      post.classList.add('hidden');
    }
  });
}
</script>
