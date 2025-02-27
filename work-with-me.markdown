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
</style>

<div class="work-container">
  <h1 class="page-heading">AI and Data Consulting Services</h1>

  <div class="company-logo-container">
    <a href="https://pragmanexus.com" class="company-logo">
      <img src="/docs/assets/images/pragma_nexus_logo.png" width="400" height="400" alt="PragmaNexus Logo"/>
    </a>
  </div>
  
  <div class="content-container">
    <p class="description-text">After 20+ years building data systems and leading engineering teams, I founded PragmaNexus to help organizations make practical use of their data. My experience spans <span class="highlight accent">both traditional machine learning and newer large language models</span>, allowing me to recommend the right approach for each specific business problem.</p>
    
    <h3 class="section-heading">Practical Experience with Both Approaches</h3>
    
    <p class="description-text">What guides my work is a straightforward principle: use the right tool for the job. Sometimes that's a traditional ML model with clear, interpretable outputs. Other times it's an LLM that can process unstructured data or natural language. Often, it's a combination of both approaches working together to solve different parts of a complex problem.</p>
    
    <div class="expertise-grid">
      <div class="expertise-column">
        <div class="expertise-box">
          <div class="expertise-title">Traditional Data & ML</div>
          <p>I've built production machine learning systems for predictive modeling, classification, and recommendation engines. My experience includes designing data pipelines, feature engineering, and developing models that deliver reliable, transparent results at scale.</p>
        </div>
      </div>
      
      <div class="expertise-column">
        <div class="expertise-box">
          <div class="expertise-title">LLM Implementation</div>
          <p>I build effective LLM systems that integrate with existing infrastructure, focus on accuracy, and deliver reliable results. My implementations address common challenges like data security, reducing hallucinations, and optimizing for both performance and cost.</p>
        </div>
      </div>
    </div>
    
    <h3 class="section-heading">Services I Offer</h3>
    
    <ul class="services-list">
      <li><span class="highlight">Practical AI Strategy</span> — Developing roadmaps that use both traditional ML and LLMs to address your specific business challenges</li>
      <li><span class="highlight">LLM Engineering</span> — Building reliable AI systems that deliver accurate results, integrate with your existing tools, and address practical concerns like security and cost</li>
      <li><span class="highlight">Data Infrastructure</span> — Building scalable data platforms that provide the foundation for both analytics and AI applications</li>
      <li><span class="highlight">Technical Evaluation</span> — Assessing which approaches will work best for your specific requirements and constraints</li>
      <li><span class="highlight">Team Development</span> — Helping your team build the skills to maintain and extend these systems</li>
    </ul>
    
    <p class="description-text">My background spans different industries—from quantitative finance to consumer analytics to small business operations. This breadth of experience helps me quickly understand your domain and business objectives when designing technical solutions.</p>
    
    <div class="product-first-box">
      <div class="product-first-heading">My Product-First Approach</div>
      <p>I believe the most important question isn't "Which AI technology should we use?" but rather "What actual business problems are we trying to solve?" This product-first mindset means I start by understanding the real issues affecting your business, your users, and your bottom line.</p>
      <p>Only after clarifying the core problems do we discuss potential solutions—whether that involves machine learning, LLMs, or simpler approaches. The technologies are just tools; what matters is addressing the problems that genuinely impact your business outcomes.</p>
      <p>This approach has consistently led to more focused, practical solutions that deliver real value rather than chasing the latest technology trends. It's about building something that works for your specific context, solves actual problems, and creates measurable business impact.</p>
    </div>
    
    <div class="cta-container">
      <a href="https://pragmanexus.com" class="cta-link">Learn More About PragmaNexus</a>
    </div>
  </div>
</div>