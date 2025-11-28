---
layout: splash
---

<style>
  /* =================================================================
     HOMEPAGE STYLES - Refined Tech Design
     ================================================================= */

  /* Hero Section */
  .hero-section {
    background: var(--gradient-hero);
    padding: 4rem 1.5rem 3rem;
    margin: -2rem -1.4rem 0;
    position: relative;
  }

  .hero-section::before {
    content: '';
    position: absolute;
    inset: 0;
    background-image: radial-gradient(circle at 20% 30%, rgba(30, 58, 95, 0.06) 0%, transparent 50%),
                      radial-gradient(circle at 80% 70%, rgba(245, 158, 11, 0.04) 0%, transparent 50%);
    pointer-events: none;
  }

  .hero-content {
    max-width: 800px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
  }

  /* Profile Header */
  .profile-header {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  /* Profile Image */
  .profile-image-wrapper {
    position: relative;
    margin-bottom: 2rem;
  }

  .profile-image {
    width: 180px;
    height: 180px;
    border-radius: 50%;
    border: 4px solid var(--color-surface);
    box-shadow: 0 8px 32px rgba(30, 58, 95, 0.15),
                0 0 0 1px var(--color-primary);
    object-fit: cover;
  }

  /* Hero Heading */
  .hero-heading {
    font-family: var(--font-display);
    font-size: 2.75rem;
    font-weight: 800;
    color: var(--color-text);
    margin-bottom: 1rem;
    letter-spacing: -0.03em;
    line-height: 1.1;
  }

  .hero-heading .text-gradient {
    background: var(--gradient-text);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  /* Hero Subheading */
  .hero-subheading {
    font-family: var(--font-body);
    font-size: 1.2rem;
    line-height: 1.7;
    color: var(--color-text-muted);
    margin-bottom: 2rem;
    max-width: 600px;
  }

  /* CTA Section */
  .cta-section {
    display: flex;
    gap: 1rem;
    justify-content: center;
    flex-wrap: wrap;
  }

  .btn-hero-primary {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    padding: 1rem 2rem;
    background: var(--gradient-accent);
    color: white !important;
    text-decoration: none;
    border-radius: var(--radius-md);
    font-family: var(--font-display);
    font-size: 1.1rem;
    font-weight: 600;
    box-shadow: 0 4px 16px rgba(30, 58, 95, 0.3);
    transition: all var(--transition-base);
    border: none;
  }

  .btn-hero-primary:hover {
    box-shadow: 0 6px 24px rgba(30, 58, 95, 0.4);
    transform: translateY(-2px);
    color: white !important;
  }

  .btn-hero-secondary {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    padding: 1rem 2rem;
    background: var(--color-surface);
    color: var(--color-primary) !important;
    text-decoration: none;
    border-radius: var(--radius-md);
    font-family: var(--font-display);
    font-size: 1.1rem;
    font-weight: 600;
    border: 2px solid var(--color-border);
    transition: all var(--transition-base);
  }

  .btn-hero-secondary:hover {
    border-color: var(--color-primary);
    background: rgba(30, 58, 95, 0.05);
    transform: translateY(-2px);
    color: var(--color-primary) !important;
  }

  /* Main Content Container */
  .main-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 3rem 1.5rem;
  }

  /* What I Do Section */
  .what-i-do-section {
    margin-bottom: 4rem;
  }

  .what-i-do-card {
    background: var(--color-surface);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-lg);
    padding: 2.5rem;
    position: relative;
    box-shadow: var(--shadow-md);
    max-width: 800px;
    margin: 0 auto;
  }

  .what-i-do-card::before {
    content: '';
    position: absolute;
    left: 0;
    top: 1.5rem;
    bottom: 1.5rem;
    width: 4px;
    background: var(--gradient-accent);
    border-radius: 2px;
  }

  .what-i-do-intro {
    font-family: var(--font-display);
    font-size: 1.35rem;
    font-weight: 700;
    color: var(--color-text);
    margin-bottom: 1.25rem;
    line-height: 1.4;
  }

  .what-i-do-details {
    font-size: 1.1rem;
    line-height: 1.7;
    color: var(--color-text-muted);
    margin-bottom: 1.25rem;
  }

  .what-i-do-approach {
    font-size: 1.05rem;
    line-height: 1.7;
    color: var(--color-text);
    margin-bottom: 0;
    padding-top: 1rem;
    border-top: 1px solid var(--color-border);
    font-weight: 500;
  }

  /* Section Heading */
  .section-heading {
    font-family: var(--font-display);
    font-size: 1.75rem;
    font-weight: 700;
    color: var(--color-text);
    text-align: center;
    margin-bottom: 2rem;
    letter-spacing: -0.02em;
  }

  /* Recent Writing Section */
  .recent-writing-section {
    margin-bottom: 4rem;
  }

  .recent-posts {
    display: grid;
    gap: 1.25rem;
    max-width: 800px;
    margin: 0 auto 2rem;
  }

  .recent-post {
    background: var(--color-surface);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-md);
    padding: 1.5rem 1.75rem;
    transition: all var(--transition-base);
  }

  .recent-post:hover {
    border-color: var(--color-primary);
    box-shadow: var(--shadow-hover);
    transform: translateY(-2px);
  }

  .recent-post h4 {
    margin: 0 0 0.5rem 0;
  }

  .recent-post h4 a {
    font-family: var(--font-display);
    color: var(--color-text);
    text-decoration: none;
    font-size: 1.1rem;
    font-weight: 600;
    transition: color var(--transition-fast);
  }

  .recent-post:hover h4 a {
    color: var(--color-primary);
  }

  .recent-post p {
    color: var(--color-text-muted);
    font-size: 1rem;
    line-height: 1.5;
    margin: 0;
  }

  /* Browse All Link */
  .writing-link {
    text-align: center;
  }

  .writing-link a {
    font-family: var(--font-display);
    color: var(--color-primary);
    text-decoration: none;
    font-weight: 600;
    font-size: 1rem;
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
    transition: gap var(--transition-fast);
  }

  .writing-link a:hover {
    gap: 0.6rem;
  }

  /* Navigation Cards Section */
  .nav-cards-section {
    padding-top: 2rem;
    border-top: 1px solid var(--color-border);
  }

  .nav-cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
    max-width: 900px;
    margin: 0 auto;
  }

  .nav-card {
    background: var(--color-surface);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-lg);
    padding: 2rem 1.5rem;
    text-align: center;
    text-decoration: none;
    transition: all var(--transition-base);
    display: block;
  }

  .nav-card:hover {
    border-color: var(--color-primary);
    box-shadow: var(--shadow-hover);
    transform: translateY(-3px);
  }

  .nav-card-title {
    font-family: var(--font-display);
    font-size: 1.15rem;
    font-weight: 700;
    color: var(--color-text);
    margin-bottom: 0.5rem;
    transition: color var(--transition-fast);
  }

  .nav-card:hover .nav-card-title {
    color: var(--color-primary);
  }

  .nav-card-description {
    font-size: 0.95rem;
    color: var(--color-text-muted);
    line-height: 1.5;
    margin: 0;
  }

  /* Responsive */
  @media (max-width: 768px) {
    .hero-section {
      padding: 3rem 1rem 2rem;
    }

    .hero-heading {
      font-size: 2rem;
    }

    .hero-subheading {
      font-size: 1.1rem;
    }

    .profile-image {
      width: 140px;
      height: 140px;
    }

    .cta-section {
      flex-direction: column;
      align-items: center;
    }

    .btn-hero-primary,
    .btn-hero-secondary {
      width: 100%;
      max-width: 280px;
      justify-content: center;
    }

    .nav-cards {
      grid-template-columns: 1fr;
    }

    .what-i-do-card {
      padding: 2rem 1.5rem;
    }

    .what-i-do-intro {
      font-size: 1.2rem;
    }
  }
</style>

<!-- Hero Section -->
<div class="hero-section">
  <div class="hero-content">
    <div class="profile-header animate-in">
      <div class="profile-image-wrapper">
        <img src="/docs/assets/images/matt.jpeg" class="profile-image" alt="Matt Stockton"/>
      </div>
      <h1 class="hero-heading">Hello, I'm <span class="text-gradient">Matt</span></h1>
      <p class="hero-subheading">I've spent 20+ years building software and data systems, with the last decade focused on ML and data infrastructure. Today I help teams understand what's actually possible with large language models and build solutions that deliver real results.</p>
      <div class="cta-section">
        <a href="/work-with-me.html" class="btn-hero-primary">Work With Me</a>
        <a href="/writing.html" class="btn-hero-secondary">Read My Writing</a>
      </div>
    </div>
  </div>
</div>

<!-- Main Content -->
<div class="main-content">

  <!-- What I Do Section -->
  <div class="what-i-do-section animate-in delay-1">
    <div class="what-i-do-card">
      <p class="what-i-do-intro">I help teams cut through the AI hype to build systems that actually solve their business problems.</p>
      <p class="what-i-do-details">These tools can solve problems in ways that weren't possible before - processing complex documents, understanding customer intent, generating insights from unstructured data. But the key is starting with your actual business problems, not the technology. I help you figure out what's worth building, then build it alongside your team, and make sure your people can maintain it.</p>
      <p class="what-i-do-approach">My approach is hands-on: I architect and build alongside your team rather than just giving advice. The goal is reliable systems that create real value, not demos.</p>
    </div>
  </div>

  <!-- Recent Writing Section -->
  <div class="recent-writing-section animate-in delay-2">
    <h2 class="section-heading">Recent Writing</h2>
    <div class="recent-posts">
      <div class="recent-post">
        <h4><a href="/2025/07/10/why-successful-llm-products-start-with-spreadsheets.html">Why Successful LLM Products Start with Spreadsheets</a></h4>
        <p>Systematic evaluation is what separates working products from demos.</p>
      </div>
      <div class="recent-post">
        <h4><a href="/2025/06/21/ai-coding-tools-amplify-what-you-already-know.html">AI Coding Tools Amplify What You Already Know</a></h4>
        <p>These tools are productivity multipliers for people who understand the domain.</p>
      </div>
      <div class="recent-post">
        <h4><a href="/2025/04/09/what-matters-when-building-ai-products.html">What Actually Matters When You're Building AI Products</a></h4>
        <p>A few takeaways from Hamel Husain's guide to improving AI products.</p>
      </div>
      <div class="recent-post">
        <h4><a href="/2025/07/13/five-insights-from-andrew-ng-on-building-faster-with-ai.html">Five Insights from Andrew Ng on Building Faster with AI</a></h4>
        <p>Practical advice on shipping AI features quickly and effectively.</p>
      </div>
    </div>
    <p class="writing-link"><a href="/writing.html">Browse all posts →</a></p>
  </div>

  <!-- Navigation Cards -->
  <div class="nav-cards-section animate-in delay-3">
    <div class="nav-cards">
      <a href="/work-with-me.html" class="nav-card">
        <h3 class="nav-card-title">Work With Me</h3>
        <p class="nav-card-description">Strategic consulting for measurable business impact</p>
      </a>
      <a href="/writing.html" class="nav-card">
        <h3 class="nav-card-title">Writing</h3>
        <p class="nav-card-description">Practical insights on building AI solutions that work</p>
      </a>
      <a href="/my-background.html" class="nav-card">
        <h3 class="nav-card-title">Background</h3>
        <p class="nav-card-description">20+ years of building systems that solve real problems</p>
      </a>
    </div>
  </div>

</div>
