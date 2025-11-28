---
layout: splash
---

<style>
  /* =================================================================
     WORK WITH ME PAGE - Refined Tech Design
     ================================================================= */

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
    background-image: radial-gradient(circle at 70% 30%, rgba(30, 58, 95, 0.05) 0%, transparent 50%);
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

  /* Work Container */
  .work-container {
    max-width: 900px;
    margin: 2rem auto;
    padding: 0 1rem;
  }


  /* Content Card */
  .content-card {
    background: var(--color-surface);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-lg);
    padding: 2.5rem;
    box-shadow: var(--shadow-md);
  }

  /* Section Heading */
  .section-heading {
    font-family: var(--font-display);
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--color-text);
    margin: 2rem 0 1rem;
    letter-spacing: -0.02em;
  }

  .section-heading:first-of-type {
    margin-top: 0;
  }

  /* Description Text */
  .description-text {
    font-size: 1.1rem;
    line-height: 1.75;
    color: var(--color-text);
    margin-bottom: 1.25rem;
  }

  .highlight {
    color: var(--color-primary);
    font-weight: 600;
  }

  .accent {
    background: linear-gradient(to top, rgba(245, 158, 11, 0.25) 40%, transparent 40%);
    padding: 0 2px;
  }

  /* Expertise Grid */
  .expertise-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.25rem;
    margin: 1.5rem 0;
  }

  .expertise-box {
    background: var(--color-surface-elevated);
    border: 1px solid var(--color-border);
    border-left: 4px solid var(--color-primary);
    border-radius: var(--radius-md);
    padding: 1.5rem;
    transition: all var(--transition-base);
  }

  .expertise-box:hover {
    border-color: var(--color-primary);
    box-shadow: var(--shadow-md);
  }

  .expertise-title {
    font-family: var(--font-display);
    font-weight: 700;
    font-size: 1.1rem;
    color: var(--color-text);
    margin-bottom: 0.75rem;
  }

  .expertise-box p {
    font-size: 0.95rem;
    line-height: 1.6;
    color: var(--color-text-muted);
    margin: 0;
  }

  /* Services List */
  .services-list {
    padding-left: 0;
    margin: 1.5rem 0;
    list-style: none;
  }

  .services-list li {
    position: relative;
    padding: 1rem 1.25rem 1rem 1.5rem;
    margin-bottom: 0.75rem;
    background: var(--color-surface-elevated);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-md);
    font-size: 1rem;
    line-height: 1.6;
    transition: all var(--transition-base);
  }

  .services-list li:hover {
    border-color: var(--color-primary);
    box-shadow: var(--shadow-sm);
  }

  .services-list li::before {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    width: 3px;
    background: var(--gradient-accent);
    border-radius: 3px 0 0 3px;
  }

  /* Closing Statement */
  .closing-statement {
    text-align: center;
    margin: 2.5rem 0 2rem;
    padding: 1.5rem;
    background: var(--color-bg-warm);
    border-radius: var(--radius-md);
  }

  .closing-statement p {
    font-family: var(--font-display);
    font-size: 1.2rem;
    font-weight: 600;
    color: var(--color-text);
    margin: 0;
  }

  /* Intro with Logo */
  .intro-section {
    display: flex;
    align-items: flex-start;
    gap: 2rem;
  }

  .intro-text {
    flex: 1;
  }

  .intro-logo {
    flex-shrink: 0;
  }

  .intro-logo img {
    height: 90px;
    width: auto;
    opacity: 0.9;
    transition: opacity var(--transition-fast);
  }

  .intro-logo:hover img {
    opacity: 1;
  }

  /* CTA Container */
  .cta-container {
    text-align: center;
  }

  .cta-link {
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
  }

  .cta-link:hover {
    box-shadow: 0 6px 24px rgba(30, 58, 95, 0.4);
    transform: translateY(-2px);
    color: white !important;
  }

  /* Responsive */
  @media (max-width: 768px) {
    .page-header {
      padding: 2rem 1rem 1.5rem;
    }

    .page-header h1 {
      font-size: 2rem;
    }

    .content-card {
      padding: 2rem 1.5rem;
    }

    .expertise-grid {
      grid-template-columns: 1fr;
    }

    .intro-section {
      flex-direction: column;
      gap: 1rem;
    }

    .intro-logo {
      order: -1;
    }

    .intro-logo img {
      height: 60px;
    }

    .section-heading {
      font-size: 1.35rem;
    }

    .description-text {
      font-size: 1.05rem;
    }
  }
</style>

<!-- Page Header -->
<div class="page-header">
  <h1>Building AI Systems That Work</h1>
  <p>Strategy, implementation, and training that helps teams cut through the AI hype.</p>
</div>

<div class="work-container">
  <div class="content-card">
    <div class="intro-section">
      <p class="intro-text description-text">I help organizations understand what's actually possible with large language models and build solutions that work. After 20+ years building data systems and leading teams, I founded PragmaNexus to provide <span class="highlight accent">strategy, implementation, and training</span> that helps teams cut through the AI hype and solve real problems.</p>
      <a href="https://pragmanexus.com" class="intro-logo">
        <img src="/docs/assets/images/pragma_nexus_logo.png" alt="PragmaNexus"/>
      </a>
    </div>

    <h3 class="section-heading">My Approach</h3>

    <p class="description-text">I start with your actual business problems, not the technology. These tools can solve problems in ways that weren't possible before, but the key is figuring out what's worth building. Not every problem needs AI, but when it fits, it can open up new possibilities.</p>

    <p class="description-text">I've worked across <span class="highlight">quantitative finance</span> (trading algorithms and investment research), <span class="highlight">consumer brands</span> (ML platforms analyzing 100,000+ businesses), <span class="highlight">small business software</span> (data infrastructure from the ground up), <span class="highlight">logistics</span>, and <span class="highlight">healthcare</span>. While I know these sectors well, I'm drawn to interesting problems in any industry.</p>

    <div class="expertise-grid">
      <div class="expertise-box">
        <div class="expertise-title">LLM Applications</div>
        <p>I build production LLM systems that solve problems you couldn't tackle before - from processing complex documents to generating insights from unstructured data. My focus is on creating real value and leveraging these tools where they make the biggest impact.</p>
      </div>
      <div class="expertise-box">
        <div class="expertise-title">Traditional ML & Data</div>
        <p>When you need predictable, interpretable results, I build traditional ML models and data pipelines. A decade of experience means I can quickly identify the right approach for your constraints.</p>
      </div>
    </div>

    <h3 class="section-heading">Services I Offer</h3>

    <ul class="services-list">
      <li><span class="highlight">Strategy & Evaluation</span> - Figure out what's actually worth building and which approach will work for your specific situation</li>
      <li><span class="highlight">Implementation</span> - Build production systems alongside your team, whether that's LLM applications, ML models, or data pipelines</li>
      <li><span class="highlight">Training & Workshops</span> - Help your team understand and apply these technologies through hands-on sessions and practical examples</li>
      <li><span class="highlight">Ongoing Support</span> - Stay available to help your team evolve and improve the systems we've built</li>
    </ul>

    <div class="closing-statement">
      <p>Let's figure out what's actually worth building for your business.</p>
    </div>

    <div class="cta-container">
      <a href="https://pragmanexus.com" class="cta-link">Learn More About PragmaNexus</a>
    </div>
  </div>
</div>
