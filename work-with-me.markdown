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
  
  /* Section styling */
  .work-container {
    padding: 2.5em;
    background-color: #fff;
    border-radius: 6px;
    box-shadow: rgba(0, 0, 0, 0.04) 0px 3px 12px;
    border-top: 3px solid #0A4D68; /* PragmaNexus primary color */
  }
  
  /* Main heading */
  .page-heading {
    font-size: 2em;
    margin-bottom: 0.8em;
    color: #0A4D68; /* PragmaNexus primary color */
    text-align: center;
  }
  
  /* Company logo styling */
  .company-logo-container {
    text-align: center;
    margin: 1.5em 0 2.5em;
  }
  
  .company-logo {
    transition: transform 0.3s ease;
    display: inline-block;
    border-radius: 8px;
    padding: 8px;
    box-shadow: 0 4px 15px rgba(10, 77, 104, 0.08); /* Very light primary shadow */
  }
  
  .company-logo:hover {
    transform: scale(1.02);
  }
  
  /* Content container */
  .content-container {
    max-width: 800px;
    margin: 0 auto;
  }
  
  /* Section heading */
  .section-heading {
    font-size: 1.4em;
    margin: 1.5em 0 0.8em;
    color: #0A4D68; /* PragmaNexus primary color */
  }
  
  /* Description text */
  .description-text {
    font-size: 1.05em;
    line-height: 1.6;
    color: #212529; /* PragmaNexus text color */
    margin-bottom: 1.2em;
  }
  
  /* Highlight key phrases */
  .highlight {
    color: #0A4D68; /* PragmaNexus primary color */
    font-weight: 500;
  }
  
  /* Gold accent for important words */
  .accent {
    border-bottom: 2px solid #FFD700;
    padding-bottom: 2px;
  }
  
  /* Services list */
  .services-list {
    padding-left: 1.2em;
    margin: 1.5em 0;
  }
  
  .services-list li {
    margin-bottom: 0.8em;
    font-size: 1.05em;
    line-height: 1.5;
  }
  
  /* Expertise section */
  .expertise-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 1.5em;
    margin: 1.5em 0;
  }
  
  .expertise-column {
    flex: 1;
    min-width: 280px;
  }
  
  .expertise-box {
    background-color: rgba(10, 77, 104, 0.03);
    border-left: 3px solid #0A4D68;
    padding: 1.2em;
    margin-bottom: 1em;
    border-radius: 4px;
  }
  
  .expertise-title {
    font-weight: 600;
    margin-bottom: 0.5em;
    font-size: 1.1em;
    color: #0A4D68;
  }
  
  /* Product-first callout */
  .product-first-box {
    background-color: rgba(10, 77, 104, 0.05);
    border: 1px solid rgba(10, 77, 104, 0.1);
    border-left: 4px solid #0A4D68;
    padding: 1.5em;
    border-radius: 4px;
    margin: 2em 0;
  }
  
  .product-first-heading {
    font-size: 1.2em;
    color: #0A4D68;
    margin-bottom: 0.7em;
    font-weight: 600;
  }
  
  /* CTA section */
  .cta-container {
    text-align: center;
    margin-top: 2.5em;
  }
  
  /* CTA button */
  .cta-link {
    display: inline-block;
    padding: 0.8em 1.8em;
    background-color: #0A4D68; /* PragmaNexus primary color */
    color: white !important; /* Ensuring white text color */
    text-decoration: none;
    border-radius: 4px;
    font-size: 1.1em;
    font-weight: 500;
    transition: all 0.3s ease;
    border: 2px solid #0A4D68; /* PragmaNexus primary color */
  }
  
  /* Button hover effect */
  .cta-link:hover {
    background-color: white;
    color: #0A4D68 !important; /* Ensuring teal text on hover */
    text-decoration: none;
    box-shadow: 0 4px 8px rgba(10, 77, 104, 0.15); /* Primary color shadow */
  }
  
  /* Closing statement styling */
  .closing-statement {
    text-align: center;
    margin: 2em 0 1.5em;
    max-width: 500px;
    margin-left: auto;
    margin-right: auto;
  }
  
  .closing-statement p {
    font-size: 1.1em;
    color: #0A4D68;
    font-weight: 500;
    margin: 0;
    font-style: italic;
  }
</style>

<div class="work-container">
  <h1 class="page-heading">Building AI Systems That Work</h1>

  <div class="company-logo-container">
    <a href="https://pragmanexus.com" class="company-logo">
      <img src="/docs/assets/images/pragma_nexus_logo.png" width="400" height="400" alt="PragmaNexus Logo"/>
    </a>
  </div>
  
  <div class="content-container">
    <p class="description-text">I help organizations understand what's actually possible with large language models and build solutions that work. After 20+ years building data systems and leading teams, I founded PragmaNexus to provide <span class="highlight accent">strategy, implementation, and training</span> that helps teams cut through the AI hype and solve real problems.</p>
    
    <h3 class="section-heading">My Approach</h3>
    
    <p class="description-text">I start with your actual business problems, not the technology. These tools can solve problems in ways that weren't possible before, but the key is figuring out what's worth building. Not every problem needs AI, but when it fits, it can open up new possibilities.</p>
    
    <p class="description-text">I've worked across <span class="highlight">quantitative finance</span> (trading algorithms and investment research), <span class="highlight">consumer brands</span> (ML platforms analyzing 100,000+ businesses), <span class="highlight">small business software</span> (data infrastructure from the ground up), <span class="highlight">logistics</span>, and <span class="highlight">healthcare</span>. While I know these sectors well, I'm drawn to interesting problems in any industry.</p>
    
    <div class="expertise-grid">
      <div class="expertise-column">
        <div class="expertise-box">
          <div class="expertise-title">LLM Applications</div>
          <p>I build production LLM systems that solve problems you couldn't tackle before - from processing complex documents to generating insights from unstructured data. My focus is on creating real value and leveraging these tools where they make the biggest impact.</p>
        </div>
      </div>
      
      <div class="expertise-column">
        <div class="expertise-box">
          <div class="expertise-title">Traditional ML & Data</div>
          <p>When you need predictable, interpretable results, I build traditional ML models and data pipelines. A decade of experience means I can quickly identify the right approach for your constraints.</p>
        </div>
      </div>
    </div>
    
    <h3 class="section-heading">Services I Offer</h3>
    
    <ul class="services-list">
      <li><span class="highlight">Strategy & Evaluation</span> — Figure out what's actually worth building and which approach will work for your specific situation</li>
      <li><span class="highlight">Implementation</span> — Build production systems alongside your team, whether that's LLM applications, ML models, or data pipelines</li>
      <li><span class="highlight">Training & Workshops</span> — Help your team understand and apply these technologies through hands-on sessions and practical examples</li>
      <li><span class="highlight">Ongoing Support</span> — Stay available to help your team evolve and improve the systems we've built</li>
    </ul>
    
    <div class="closing-statement">
      <p>Let's figure out what's actually worth building for your business.</p>
    </div>
    
    <div class="cta-container">
      <a href="https://pragmanexus.com" class="cta-link">Learn More About PragmaNexus</a>
    </div>
  </div>
</div>