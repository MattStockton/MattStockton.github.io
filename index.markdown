---
layout: splash
---

<style>
  /* Main container styling */
  .page__content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 2em 1.4em;
  }
  
  /* Profile container */
  .profile-container {
    padding: 2em;
    background-color: #fff;
    border-radius: 6px;
    box-shadow: rgba(0, 0, 0, 0.04) 0px 3px 8px;
  }
  
  /* Profile section with image and heading */
  .profile-header {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    margin-bottom: 2em;
  }
  
  /* Profile image styling */
  .profile-image {
    border-radius: 50%;
    margin-bottom: 1.5em;
    border: 3px solid #0A4D68; /* PragmaNexus primary color */
  }
  
  /* Hero heading */
  .hero-heading {
    font-size: 1.8em;
    margin-bottom: 0.8em;
    color: #0A4D68;
    font-weight: 600;
    text-align: center;
  }
  
  /* Hero subheading */
  .hero-subheading {
    font-size: 1.05em;
    line-height: 1.5;
    color: #212529;
    margin-bottom: 1.5em;
    text-align: center;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
  }
  
  /* CTA section */
  .cta-section {
    display: flex;
    gap: 1em;
    justify-content: center;
    margin-bottom: 2em;
    flex-wrap: wrap;
  }
  
  /* Primary CTA button */
  .primary-cta {
    display: inline-block;
    padding: 0.8em 1.8em;
    background-color: #0A4D68;
    color: white !important;
    text-decoration: none;
    border-radius: 4px;
    font-size: 1.1em;
    font-weight: 600;
    transition: all 0.3s ease;
    border: 2px solid #0A4D68;
  }
  
  .primary-cta:hover {
    background-color: white;
    color: #0A4D68 !important;
    box-shadow: 0 4px 12px rgba(10, 77, 104, 0.2);
    transform: translateY(-1px);
  }
  
  /* Secondary CTA button */
  .secondary-cta {
    display: inline-block;
    padding: 0.8em 1.8em;
    background-color: white;
    color: #0A4D68 !important;
    text-decoration: none;
    border-radius: 4px;
    font-size: 1.1em;
    font-weight: 600;
    transition: all 0.3s ease;
    border: 2px solid #0A4D68;
  }
  
  .secondary-cta:hover {
    background-color: #0A4D68;
    color: white !important;
    transform: translateY(-1px);
  }
  
  /* Bio text - now left aligned */
  .bio-text {
    font-size: 1.05em;
    line-height: 1.6;
    color: #212529; /* PragmaNexus text color */
    margin-bottom: 1.5em;
    text-align: left;
  }
  
  /* Links list - now left aligned */
  .links-list {
    margin: 1.5em 0;
    padding: 0;
    list-style-type: none;
    text-align: left;
  }
  
  .links-list li {
    margin-bottom: 0.7em;
    font-size: 1.05em;
  }
  
  .links-list a {
    color: #0A4D68; /* PragmaNexus primary color */
    text-decoration: none;
    transition: color 0.2s ease;
  }
  
  .links-list a:hover {
    color: #137a9e; /* Lighter shade of primary for hover */
    text-decoration: underline;
  }
  
  /* Highlight text - now made clickable */
  .highlight-link {
    color: #0A4D68; /* PragmaNexus primary color */
    font-weight: 600;
    border-bottom: 2px solid #FFD700; /* PragmaNexus secondary color */
    text-decoration: none;
    transition: color 0.2s ease;
  }
  
  .highlight-link:hover {
    color: #137a9e; /* Lighter shade of primary for hover */
    text-decoration: none;
  }
  
  /* Contact section styling */
  .contact-section {
    display: flex;
    flex-wrap: wrap;
    gap: 1.5em;
    margin-top: 2em;
  }
  
  .contact-link {
    display: flex;
    align-items: center;
    color: #0A4D68;
    text-decoration: none;
    transition: transform 0.2s ease, color 0.2s ease;
    font-size: 1em;
  }
  
  .contact-link:hover {
    color: #137a9e;
    transform: translateY(-2px);
  }
  
  .contact-icon {
    margin-right: 0.5em;
    font-size: 1.2em;
  }
  
  /* What I Do section */
  .what-i-do-section {
    margin: 2em 0;
    padding: 2em 0;
    border-top: 1px solid rgba(10, 77, 104, 0.1);
    border-bottom: 1px solid rgba(10, 77, 104, 0.1);
  }
  
  .what-i-do-highlight {
    background-color: rgba(10, 77, 104, 0.03);
    border-left: 4px solid #0A4D68;
    border-radius: 8px;
    padding: 2em;
    max-width: 700px;
    margin: 0 auto;
    text-align: left;
  }
  
  .what-i-do-intro {
    font-size: 1.2em;
    font-weight: 600;
    color: #0A4D68;
    margin-bottom: 1em;
    line-height: 1.4;
  }
  
  .what-i-do-details {
    font-size: 1.05em;
    line-height: 1.6;
    color: #212529;
    margin-bottom: 1em;
  }
  
  .what-i-do-approach {
    font-size: 1.05em;
    line-height: 1.6;
    color: #212529;
    margin-bottom: 0;
    font-style: italic;
  }
  
  .section-heading {
    font-size: 1.4em;
    color: #0A4D68;
    text-align: center;
    margin-bottom: 1.5em;
    font-weight: 600;
  }
  
  /* Recent Writing section */
  .recent-writing-section {
    margin: 2em 0;
    padding: 1.5em 0;
  }
  
  .recent-posts {
    max-width: 700px;
    margin: 0 auto 1.5em;
  }
  
  .recent-post {
    margin-bottom: 1.2em;
    padding-bottom: 1em;
    border-bottom: 1px solid rgba(10, 77, 104, 0.1);
  }
  
  .recent-post:last-child {
    border-bottom: none;
  }
  
  .recent-post h4 {
    margin-bottom: 0.4em;
  }
  
  .recent-post h4 a {
    color: #0A4D68;
    text-decoration: none;
    font-size: 1.05em;
    font-weight: 600;
  }
  
  .recent-post h4 a:hover {
    color: #137a9e;
    text-decoration: underline;
  }
  
  .recent-post p {
    color: #212529;
    font-size: 0.95em;
    line-height: 1.4;
    margin: 0;
  }
  
  .writing-link {
    text-align: center;
    margin-top: 1em;
  }
  
  .writing-link a {
    color: #0A4D68;
    text-decoration: none;
    font-weight: 500;
  }
  
  .writing-link a:hover {
    text-decoration: underline;
  }
  
  /* Simple navigation section */
  .simple-nav-section {
    margin: 2em 0;
    padding: 1.5em 0;
    border-top: 1px solid rgba(10, 77, 104, 0.1);
  }
  
  .simple-nav-links {
    display: flex;
    justify-content: center;
    gap: 2em;
    max-width: 800px;
    margin: 0 auto;
    flex-wrap: wrap;
  }
  
  .nav-link-item {
    text-align: center;
    flex: 1;
    min-width: 200px;
    max-width: 250px;
  }
  
  .nav-link-item h3 {
    margin-bottom: 0.3em;
  }
  
  .nav-link-item h3 a {
    color: #0A4D68;
    text-decoration: none;
    font-size: 1.1em;
    font-weight: 600;
  }
  
  .nav-link-item h3 a:hover {
    color: #137a9e;
    text-decoration: underline;
  }
  
  .nav-link-item p {
    color: #6c757d;
    font-size: 0.9em;
    line-height: 1.4;
    margin: 0;
  }
</style>

<div class="profile-container">
  <div class="profile-header">
    <img src="/docs/assets/images/matt.jpeg" width="300" height="300" class="profile-image" alt="Matt Stockton"/>
    <h1 class="hero-heading">Hello, I'm Matt!</h1>
    <p class="hero-subheading">I've spent 20+ years building software and data systems, with the last decade focused on ML and data infrastructure. Today I help teams understand what's actually possible with large language models and build solutions that deliver real results.</p>
    <div class="cta-section">
      <a href="/work-with-me.html" class="primary-cta">Work With Me</a>
      <a href="/writing.html" class="secondary-cta">Read My Writing</a>
    </div>
  </div>
  
  <!-- What I Do Section -->
  <div class="what-i-do-section">
    <div class="what-i-do-highlight">
      <p class="what-i-do-intro">I help teams cut through the AI hype to build systems that actually solve their business problems.</p>
      <p class="what-i-do-details">These tools can solve problems in ways that weren't possible before - processing complex documents, understanding customer intent, generating insights from unstructured data. But the key is starting with your actual business problems, not the technology. I help you figure out what's worth building, then build it alongside your team, and make sure your people can maintain it.</p>
      <p class="what-i-do-approach">My approach is hands-on: I architect and build alongside your team rather than just giving advice. The goal is reliable systems that create real value, not demos.</p>
    </div>
  </div>
  
  
  <!-- Recent Writing Section -->
  <div class="recent-writing-section">
    <h2 class="section-heading">Recent Writing</h2>
    <div class="recent-posts">
      <div class="recent-post">
        <h4><a href="/2025/07/10/why-successful-llm-products-start-with-spreadsheets/">Why Successful LLM Products Start with Spreadsheets</a></h4>
        <p>Systematic evaluation is what separates working products from demos.</p>
      </div>
      <div class="recent-post">
        <h4><a href="/2025/06/21/ai-coding-tools-amplify-what-you-already-know/">AI Coding Tools Amplify What You Already Know</a></h4>
        <p>These tools are productivity multipliers for people who understand the domain.</p>
      </div>
      <div class="recent-post">
        <h4><a href="/2025/04/09/what-matters-when-building-ai-products/">What Actually Matters When You're Building AI Products</a></h4>
        <p>A few takeaways from Hamel Husain's guide to improving AI products.</p>
      </div>
      <div class="recent-post">
        <h4><a href="/2025/07/13/five-insights-from-andrew-ng-on-building-faster-with-ai/">Five Insights from Andrew Ng on Building Faster with AI</a></h4>
        <p>Practical advice on shipping AI features quickly and effectively.</p>
      </div>
    </div>
    <p class="writing-link"><a href="/writing.html">Browse all posts →</a></p>
  </div>
  
  <!-- Simple Navigation -->
  <div class="simple-nav-section">
    <div class="simple-nav-links">
      <div class="nav-link-item">
        <h3><a href="/work-with-me.html">Work With Me</a></h3>
        <p>Strategic consulting for measurable business impact</p>
      </div>
      <div class="nav-link-item">
        <h3><a href="/writing.html">Writing</a></h3>
        <p>Practical insights on building AI solutions that work</p>
      </div>
      <div class="nav-link-item">
        <h3><a href="/my-background.html">Background</a></h3>
        <p>20+ years of building systems that solve real problems</p>
      </div>
    </div>
  </div>
  
</div>