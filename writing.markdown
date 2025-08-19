---
layout: splash
classes: 
  - wide
---

<style>
  /* Force full width container without indentation */
  .page__content,
  .archive,
  #main {
    max-width: 1200px !important;
    margin-left: auto !important;
    margin-right: auto !important;
    float: none !important;
    width: 100% !important;
  }

  /* Remove any right-side shifting */
  #main {
    padding-left: 1em !important;
    padding-right: 1em !important;
  }
  
  /* Container for better spacing */
  .content-container {
    margin-top: 1.5em;
    padding: 1.5em 1.4em;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: rgba(0, 0, 0, 0.06) 0px 3px 12px;
    border-top: 3px solid #0A4D68;
  }


  /* Featured badge for posts */
  .featured-badge {
    background-color: #FFD700;
    color: #0A4D68;
    padding: 0.2em 0.6em;
    border-radius: 12px;
    font-size: 0.75em;
    margin-left: 0.5em;
    font-weight: 600;
  }

  /* Category navigation */
  .category-nav {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4em;
    margin-bottom: 1.5em;
    justify-content: center;
    padding-bottom: 1em;
    border-bottom: 1px solid #e9ecef;
  }

  .category-button {
    padding: 0.4em 0.8em;
    background-color: #fff;
    color: #0A4D68;
    border: 1px solid #0A4D68;
    border-radius: 16px;
    text-decoration: none;
    font-size: 0.8em;
    font-weight: 500;
    transition: all 0.3s ease;
    cursor: pointer;
    white-space: nowrap;
  }

  .category-button:hover, .category-button.active {
    background-color: #0A4D68;
    color: white !important;
  }

  /* All posts section */
  .all-posts {
    margin-top: 1.5em;
  }

  .post-item {
    padding: 1.2em 1.5em;
    margin-bottom: 1.2em;
    background-color: #f8f9fa;
    border-radius: 6px;
    border-top: 3px solid #0A4D68;
    transition: all 0.2s ease-out;
  }

  .post-item:hover {
    background-color: #fff;
    box-shadow: rgba(0, 0, 0, 0.08) 0px 4px 12px;
  }

  .post-item h3 {
    margin-top: 0.1em !important;
    margin-bottom: 0.4em !important;
    font-size: 1.2em !important;
  }

  .post-item h3 a {
    color: #0A4D68 !important;
    text-decoration: none !important;
  }

  .post-item h3 a:hover {
    color: #137a9e !important;
  }

  .post-meta {
    margin-bottom: 0.5em !important;
    font-size: 0.85em !important;
    color: #6c757d !important;
  }

  .post-excerpt {
    display: block !important;
    margin-top: 0.6em !important;
    margin-bottom: 0.6em !important;
    font-size: 0.92em !important;
    color: #212529 !important;
    line-height: 1.55 !important;
  }

  /* Category badges */
  .post-category {
    display: inline-block;
    background-color: #e9ecef;
    color: #0A4D68;
    padding: 0.2em 0.6em;
    border-radius: 12px;
    font-size: 0.75em;
    margin-left: 0.5em;
    font-weight: 500;
  }

  /* Hidden class for filtering */
  .hidden {
    display: none !important;
  }

  /* Tag section styles */
  .tag-section {
    text-align: center;
    margin: 0.5em 0;
    padding-top: 0.3em;
  }

  .tag-toggle {
    background: none;
    border: none;
    color: #6c757d;
    font-size: 0.75em;
    cursor: pointer;
    padding: 0.2em 0.4em;
    border-radius: 8px;
    transition: all 0.3s ease;
    opacity: 0.7;
  }

  .tag-toggle:hover {
    background-color: #f8f9fa;
    color: #0A4D68;
    opacity: 1;
  }

  .tag-cloud {
    display: none;
    margin-top: 0.8em;
    padding: 0.8em;
    background-color: #fafbfc;
    border: 1px solid #e9ecef;
    border-radius: 6px;
    max-height: 180px;
    overflow-y: auto;
  }

  .tag-cloud.show {
    display: block;
  }

  .tag-item {
    display: inline-block;
    margin: 0.2em 0.3em;
    padding: 0.3em 0.6em;
    background-color: #fff;
    color: #0A4D68;
    border: 1px solid #dee2e6;
    border-radius: 12px;
    font-size: 0.75em;
    cursor: pointer;
    transition: all 0.3s ease;
    text-decoration: none;
  }

  .tag-item:hover {
    background-color: #0A4D68;
    color: white;
  }

  .tag-item.active {
    background-color: #0A4D68;
    color: white;
    font-weight: 600;
  }

  /* Tag size variations based on frequency */
  .tag-item.size-large { font-size: 0.9em; font-weight: 600; }
  .tag-item.size-medium { font-size: 0.8em; font-weight: 500; }
  .tag-item.size-small { font-size: 0.7em; }

  /* Section divider */
  .section-divider {
    margin: 3em 0 2em 0;
    border-bottom: 2px solid #e9ecef;
    position: relative;
  }

  .section-divider::after {
    content: '';
    position: absolute;
    bottom: -2px;
    left: 50%;
    transform: translateX(-50%);
    width: 100px;
    height: 2px;
    background-color: #0A4D68;
  }

  /* Responsive design */
  @media (max-width: 768px) {
    .featured-posts {
      grid-template-columns: 1fr;
    }
    
    .category-nav {
      justify-content: flex-start;
    }
    
    .featured-meta {
      flex-direction: column;
      align-items: flex-start;
      gap: 0.5em;
    }

    .page-title {
      font-size: 2em;
    }
  }
</style>

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

  <!-- Tag Section -->
  <div class="tag-section">
    <button class="tag-toggle" onclick="toggleTagCloud()">
      Browse by Topic <span id="tag-arrow">▼</span>
    </button>
    <div class="tag-cloud" id="tagCloud">
      <!-- Tags will be populated by JavaScript -->
    </div>
  </div>

  <!-- All Posts Section -->
  <div class="all-posts">
    {% for post in site.posts %}
    <article class="post-item" data-category="{{ post.category | default: 'uncategorized' }}" data-featured="{{ post.featured | default: false }}" data-tags="{% if post.tags %}{{ post.tags | join: ', ' }}{% endif %}">
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
let activeTag = null;

document.addEventListener('DOMContentLoaded', function() {
  const categoryButtons = document.querySelectorAll('.category-button');
  const postItems = document.querySelectorAll('.post-item');
  
  // Initialize tag cloud
  initializeTagCloud();
  
  categoryButtons.forEach(button => {
    button.addEventListener('click', function(e) {
      e.preventDefault();
      e.stopPropagation();
      this.blur(); // Remove focus to prevent any focus-related scrolling
      activeCategory = this.getAttribute('data-category');
      
      // Clear active tag when switching categories
      activeTag = null;
      document.querySelectorAll('.tag-item').forEach(tag => tag.classList.remove('active'));
      
      // Update active button
      categoryButtons.forEach(btn => btn.classList.remove('active'));
      this.classList.add('active');
      
      // Filter posts
      filterPosts();
    });
  });
});

function initializeTagCloud() {
  const tagCloud = document.getElementById('tagCloud');
  const postItems = document.querySelectorAll('.post-item');
  const tagCounts = {};
  
  // Count tag frequencies
  postItems.forEach(post => {
    const tags = post.getAttribute('data-tags');
    if (tags) {
      tags.split(',').forEach(tag => {
        const trimmedTag = tag.trim();
        if (trimmedTag) {
          tagCounts[trimmedTag] = (tagCounts[trimmedTag] || 0) + 1;
        }
      });
    }
  });
  
  // Sort tags by frequency and take top 20
  const sortedTags = Object.entries(tagCounts)
    .sort((a, b) => b[1] - a[1])
    .slice(0, 20);
  
  // Create tag elements
  tagCloud.innerHTML = '';
  sortedTags.forEach(([tag, count]) => {
    const tagElement = document.createElement('span');
    tagElement.className = 'tag-item';
    tagElement.textContent = tag;
    tagElement.setAttribute('data-tag', tag);
    
    // Add size class based on frequency
    if (count >= 8) {
      tagElement.classList.add('size-large');
    } else if (count >= 4) {
      tagElement.classList.add('size-medium');
    } else {
      tagElement.classList.add('size-small');
    }
    
    tagElement.addEventListener('click', function() {
      if (activeTag === tag) {
        // Deselect tag
        activeTag = null;
        this.classList.remove('active');
      } else {
        // Select new tag
        activeTag = tag;
        document.querySelectorAll('.tag-item').forEach(t => t.classList.remove('active'));
        this.classList.add('active');
      }
      filterPosts();
    });
    
    tagCloud.appendChild(tagElement);
  });
}

function toggleTagCloud() {
  const tagCloud = document.getElementById('tagCloud');
  const arrow = document.getElementById('tag-arrow');
  
  if (tagCloud.classList.contains('show')) {
    tagCloud.classList.remove('show');
    arrow.textContent = '▼';
  } else {
    tagCloud.classList.add('show');
    arrow.textContent = '▲';
  }
}

function filterPosts() {
  const postItems = document.querySelectorAll('.post-item');
  
  postItems.forEach(post => {
    const postCategory = post.getAttribute('data-category');
    const postFeatured = post.getAttribute('data-featured') === 'true';
    const postTags = post.getAttribute('data-tags') || '';
    
    let categoryMatch = false;
    if (activeCategory === 'all') {
      categoryMatch = true;
    } else if (activeCategory === 'featured') {
      categoryMatch = postFeatured;
    } else {
      categoryMatch = postCategory === activeCategory;
    }
    
    let tagMatch = !activeTag || postTags.includes(activeTag);
    
    if (categoryMatch && tagMatch) {
      post.classList.remove('hidden');
    } else {
      post.classList.add('hidden');
    }
  });
}
</script>