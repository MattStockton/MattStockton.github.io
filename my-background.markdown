---
layout: splash
title: My Professional Background
---

<style>
  /* Main container styling */
  .page__content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 2em 1.4em;
  }
  
  /* Background container */
  .background-container {
    padding: 2.5em;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: rgba(0, 0, 0, 0.06) 0px 3px 12px;
    border-top: 3px solid #0A4D68;
  }
  
  /* Page introduction */
  .page-intro {
    margin-bottom: 2.5em;
    border-bottom: 1px solid rgba(10, 77, 104, 0.1);
    padding-bottom: 1.5em;
  }
  
  /* Main heading */
  .page-heading {
    font-size: 2.2em;
    margin-bottom: 0.7em;
    color: #0A4D68;
    position: relative;
    display: inline-block;
  }
  
  .page-heading:after {
    content: "";
    display: block;
    width: 50%;
    height: 3px;
    background-color: #FFD700;
    position: absolute;
    bottom: -8px;
    left: 0;
  }
  
  /* Education section */
  .education-section {
    margin-bottom: 2.5em;
  }
  
  /* Section headings */
  .section-heading {
    font-size: 1.5em;
    margin: 1.8em 0 1em;
    color: #0A4D68;
    display: flex;
    align-items: center;
  }
  
  .section-heading:before {
    content: "";
    display: inline-block;
    width: 6px;
    height: 24px;
    background-color: #FFD700;
    margin-right: 12px;
    border-radius: 3px;
  }
  
  /* Paragraph text with improved readability */
  .section-text {
    font-size: 1.05em;
    line-height: 1.7;
    color: #3a3f45;
    margin-bottom: 1.5em;
    max-width: 90ch;
  }
  
  /* Experience timeline styling */
  .experience-timeline {
    position: relative;
    margin: 2em 0 3em;
    padding-left: 2em;
  }
  
  .experience-timeline:before {
    content: "";
    position: absolute;
    top: 8px;
    bottom: 8px;
    left: 0;
    width: 3px;
    background-color: rgba(10, 77, 104, 0.1);
    border-radius: 3px;
  }
  
  /* Experience item */
  .experience-item {
    position: relative;
    margin-bottom: 2em;
    padding-bottom: 1em;
  }
  
  .experience-item:last-child {
    margin-bottom: 0;
    padding-bottom: 0;
  }
  
  /* Special styling for current company */
  .experience-item.current {
    background-color: rgba(10, 77, 104, 0.03);
    border-radius: 6px;
    padding: 1.5em;
    margin-left: -0.5em;
    margin-bottom: 3em;
    border-left: 3px solid #FFD700;
  }
  
  .experience-item.current:before {
    top: 1.5em;
    left: -2.5em;
    width: 16px;
    height: 16px;
    background-color: #FFD700;
    box-shadow: 0 0 0 3px rgba(255, 215, 0, 0.3);
  }
  
  .experience-item:before {
    content: "";
    position: absolute;
    left: -2em;
    top: 6px;
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background-color: #0A4D68;
    border: 2px solid white;
    box-shadow: 0 0 0 2px rgba(10, 77, 104, 0.3);
  }
  
  /* Job title styling */
  .job-title {
    font-size: 1.15em;
    font-weight: 600;
    color: #0A4D68;
    margin-bottom: 0.4em;
    display: inline-block;
  }
  
  /* Current job title styling */
  .current .job-title {
    font-size: 1.25em;
  }
  
  /* Company styling */
  .company {
    font-weight: 500;
    color: #137a9e;
    margin-left: 0.4em;
  }
  
  /* Current company styling */
  .current .company {
    color: #0A4D68;
    font-weight: 600;
  }
  
  /* Year range styling */
  .years {
    display: inline-block;
    color: #5a6268;
    font-size: 0.9em;
    margin-left: 0.8em;
  }
  
  /* Current year styling */
  .current .years {
    background-color: rgba(255, 215, 0, 0.2);
    padding: 0.2em 0.6em;
    border-radius: 4px;
    color: #0A4D68;
    font-weight: 500;
  }
  
  /* Job description */
  .job-description {
    margin-top: 0.5em;
    line-height: 1.6;
    color: #3a3f45;
  }
  
  /* Current job description */
  .current .job-description {
    margin-top: 0.6em;
  }
  
  /* LLM focus section */
  .llm-focus {
    margin: 3em 0;
    border-radius: 8px;
    background: linear-gradient(to right, rgba(10, 77, 104, 0.06), rgba(10, 77, 104, 0.02));
    padding: 2em;
    position: relative;
    overflow: hidden;
  }
  
  .llm-focus:before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 6px;
    height: 100%;
    background-color: #0A4D68;
  }
  
  .llm-heading {
    color: #0A4D68;
    font-size: 1.5em;
    margin-bottom: 1em;
    position: relative;
  }
  
  /* Focus areas */
  .focus-areas {
    display: flex;
    flex-wrap: wrap;
    gap: 0.8em;
    margin: 1.5em 0;
  }
  
  .focus-tag {
    display: inline-block;
    padding: 0.5em 1em;
    background-color: white;
    border: 1px solid rgba(10, 77, 104, 0.2);
    border-radius: 4px;
    font-size: 0.9em;
    color: #0A4D68;
    font-weight: 500;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  }
  
  /* Philosophy section */
  .philosophy-section {
    background-color: rgba(255, 215, 0, 0.05);
    border-radius: 8px;
    padding: 2em;
    margin: 3em 0;
    position: relative;
  }
  
  .philosophy-section:before {
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    width: 6px;
    height: 100%;
    background-color: #FFD700;
    border-radius: 8px 0 0 8px;
  }
  
  .philosophy-heading {
    color: #0A4D68;
    font-size: 1.5em;
    margin-bottom: 1em;
  }
  
  /* Leadership section */
  .leadership-section {
    background-color: white;
    border: 1px solid rgba(10, 77, 104, 0.1);
    border-radius: 8px;
    padding: 2em;
    margin: 3em 0;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.04);
  }
  
  .leadership-heading {
    color: #0A4D68;
    font-size: 1.4em;
    margin-bottom: 1em;
    display: inline-block;
    position: relative;
  }
  
  .leadership-heading:after {
    content: "";
    position: absolute;
    bottom: -6px;
    left: 0;
    width: 40%;
    height: 2px;
    background-color: #FFD700;
  }
  
  /* Emphasis styling */
  .emphasis {
    color: #0A4D68;
    font-weight: 600;
  }
  
  /* Responsive adjustments */
  @media (max-width: 768px) {
    .background-container {
      padding: 1.8em;
    }
    
    .page-heading {
      font-size: 1.8em;
    }
    
    .section-heading {
      font-size: 1.3em;
    }
    
    .experience-timeline {
      padding-left: 1.5em;
    }
    
    .experience-item:before {
      left: -1.5em;
    }
    
    .experience-item.current {
      margin-left: -1.2em;
      padding: 1.2em;
    }
    
    .experience-item.current:before {
      left: -1.8em;
    }
    
    .llm-focus, .philosophy-section, .leadership-section {
      padding: 1.5em;
    }
  }
</style>

<div class="background-container">
  <div class="page-intro">
    <h1 class="page-heading">My Professional Journey</h1>
    <p class="section-text">With over 20 years of experience building software and leading engineering teams, I've focused my career on solving complex problems with data-driven solutions. Today, I'm channeling that expertise into helping organizations leverage AI technologies effectively through my consulting practice, PragmaNexus.</p>
  </div>

  <div class="education-section">
    <h2 class="section-heading">Education</h2>
    <p class="section-text">I hold a Bachelor of Science in Engineering (Computer Science) from the University of Michigan (2004) and a Master of Science from the University of Illinois (2009), which I completed while working full-time.</p>
  </div>

  <h2 class="section-heading">Professional Experience</h2>
  
  <div class="experience-timeline">
    <div class="experience-item current">
      <span class="job-title">Founder & Principal Consultant</span>
      <span class="company">at PragmaNexus</span>
      <span class="years">(2024-Present)</span>
      <p class="job-description">I founded PragmaNexus to help organizations navigate the AI landscape with practical, results-driven solutions. Drawing on my experience in both traditional machine learning and emerging AI technologies, I provide strategic guidance and implementation support for businesses looking to leverage data and AI effectively.</p>
    </div>
    
    <div class="experience-item">
      <span class="job-title">Director of Engineering</span>
      <span class="company">at <a href="https://www.teamshares.com/">Teamshares</a></span>
      <span class="years">(2021-2024)</span>
      <p class="job-description">Built Teamshares' data strategy and infrastructure from the ground up. Established a software team and technical platform that empowered colleagues across all departments to make data-informed decisions related to acquiring and operating small businesses. Teamshares is backed by QED Investors, Khosla Ventures, Slow Ventures, Union Square Ventures, and other top-tier investors.</p>
    </div>
    
    <div class="experience-item">
      <span class="job-title">Director of Data Science and Engineering</span>
      <span class="company">at <a href="https://raconcapital.com/">Racon Capital Partners</a></span>
      <span class="years">(2020-2021)</span>
      <p class="job-description">Collaborated with the Head of Quantitative Research to develop quantitative investment algorithms and build the software/data infrastructure necessary for backtesting and executing these algorithms at scale.</p>
    </div>
    
    <div class="experience-item">
      <span class="job-title">Director of Engineering</span>
      <span class="company">at <a href="https://circleup.com/">CircleUp</a></span>
      <span class="years">(2014-2020)</span>
      <p class="job-description">Helped build and scale a Data/Machine Learning platform that discovered and analyzed emerging consumer brands across hundreds of data sources. The platform automatically identified and evaluated over 100,000 small consumer businesses, guiding investment decisions and facilitating hundreds of successful equity and debt transactions. CircleUp was backed by Google Ventures, Union Square Ventures, QED Investors, Clayton Christensen's Rose Park Advisors, and other prominent investors.</p>
    </div>
    
    <div class="experience-item">
      <span class="job-title">VP of Engineering</span>
      <span class="company">at <a href="https://www.harqen.com/">Harqen</a></span>
      <span class="years">(2010-2014)</span>
      <p class="job-description">Helped develop one of the first digital interviewing platforms, enabling millions of job applicants to apply for positions through asynchronous audio or video recordings from their smartphones or computers.</p>
    </div>
    
    <div class="experience-item">
      <span class="job-title">Senior Software Engineer</span>
      <span class="company">at Stark Investments</span>
      <span class="years">(2007-2010)</span>
      <p class="job-description">Developed Derivatives/Credit Default Swaps trading software for a multi-billion dollar hedge fund, gaining valuable insights during the 2007-2008 global financial crisis.</p>
    </div>
    
    <div class="experience-item">
      <span class="job-title">Engineering Leadership Program</span>
      <span class="company">at General Electric</span>
      <span class="years">(2004-2007)</span>
    </div>
    
    <div class="experience-item">
      <span class="job-title">iOS Developer</span>
      <span class="years">(Side Projects, Late 2000s)</span>
      <p class="job-description">Built and launched 7 iOS applications as side projects and learning experiences.</p>
    </div>
  </div>

  <div class="llm-focus">
    <h2 class="llm-heading">Current Focus: AI & Large Language Models</h2>
    <p class="section-text">I've invested significant time researching and prototyping with Large Language Models, developing practical applications that deliver real business value. My work blends technical implementation with strategic thinking to help organizations effectively adopt AI technologies.</p>
    
    <div class="focus-areas">
      <span class="focus-tag">Data Infrastructure</span>
      <span class="focus-tag">AI Strategy</span>
      <span class="focus-tag">ML/LLM Integration</span>
      <span class="focus-tag">RAG Systems</span>
      <span class="focus-tag">Evaluation Frameworks</span>
      <span class="focus-tag">Data Engineering</span>
    </div>
    
    <p class="section-text">My approach combines rigorous technical expertise with practical business sense. I help organizations move past the hype to implement AI solutions that solve real problems and deliver measurable results.</p>
  </div>

  <div class="philosophy-section">
    <h2 class="philosophy-heading">My Product-First Approach</h2>
    <p class="section-text">I believe the most critical question isn't "Which AI technology should we use?" but "What business problems are we trying to solve?" This product-first mindset means starting with the real issues affecting your business, users, and bottom line.</p>
    <p class="section-text">Only after clarifying core problems do I consider potential solutions—whether they involve machine learning, LLMs, or simpler approaches. Technologies are tools; what matters is addressing problems that genuinely impact your business outcomes.</p>
    <p class="section-text">This approach consistently leads to focused, practical solutions that deliver real value rather than chasing technology trends. It's about building something that works for your specific context and creates measurable business impact.</p>
  </div>

  <div class="leadership-section">
    <h2 class="leadership-heading">Leadership Philosophy</h2>
    <p class="section-text">I believe effective leadership multiplies a team's impact. Throughout my career, I've prioritized building, coaching, and mentoring engineering teams. Nothing frustrates me more than seeing exceptional talent stifled by inadequate leadership.</p>
    <p class="section-text">My leadership approach centers on empowering teams to do their best work. This means clear communication, thoughtful delegation, and creating an environment where innovation thrives. I take pride in growing future engineering leaders and demonstrating excellence in leadership practices.</p>
  </div>

  <p class="section-text">Above all, I focus on understanding the underlying business strategy and clearly defining the core problems to be solved. While it's important to build things correctly, it's absolutely critical to <span class="emphasis">build the right things</span>.</p>
</div>