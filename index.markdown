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
  
  /* Main heading */
  .profile-heading {
    font-size: 1.8em;
    margin-bottom: 0.5em;
    color: #0A4D68; /* PragmaNexus primary color */
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
</style>

<div class="profile-container">
  <div class="profile-header">
    <img src="/docs/assets/images/matt.jpeg" width="300" height="300" class="profile-image" alt="Matt Stockton"/>
    <h3 class="profile-heading">Hello, I'm Matt!</h3>
  </div>
  
  <p class="bio-text">I've been building software and leading software teams professionally for 20+ years, mostly at small VC-backed startup companies. My core areas of focus are Data Engineering and Machine Learning. My current technical interests are around emerging AI capabilities, specifically Large Language Models. I'm also interested in family, running, reading, meditation, investing, coffee, history, and happiness.</p>
  
  <ul class="links-list">
    <li><a href="/work-with-me.html" class="highlight-link">Work With Me</a> - I offer <a href="/work-with-me.html">AI and Data Consulting Services</a></li>
    <li><a href="/writing.html" class="highlight-link">Writing and Learning</a> - I <a href="/writing.html">write about things</a> I find interesting in the world, mainly around technology</li>
    <li><a href="/my-background.html" class="highlight-link">My Professional Background</a> - A <a href="/my-background.html">few more details</a> on where I've been and what I've done</li>
  </ul>
  
  <div class="contact-section">
    <a href="mailto:mattstockton@gmail.com" class="contact-link">
      <i class="fas fa-envelope contact-icon"></i> Email
    </a>
    <a href="https://twitter.com/mstockton" class="contact-link">
      <i class="fab fa-twitter contact-icon"></i> Twitter
    </a>
    <a href="https://www.linkedin.com/in/mattstockton/" class="contact-link">
      <i class="fab fa-linkedin contact-icon"></i> LinkedIn
    </a>
  </div>
</div>