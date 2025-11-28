---
layout: splash
title: My Professional Background
---

<style>
  /* =================================================================
     MY BACKGROUND PAGE - Refined Tech Design
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
    background-image: radial-gradient(circle at 25% 60%, rgba(30, 58, 95, 0.05) 0%, transparent 50%);
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
    max-width: 700px;
    margin: 0 auto;
    position: relative;
    line-height: 1.6;
  }

  /* Background Container */
  .background-container {
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
    margin-bottom: 1.5rem;
  }

  /* Section Heading */
  .section-heading {
    font-family: var(--font-display);
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--color-text);
    margin: 0 0 1.5rem 0;
    letter-spacing: -0.02em;
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }

  .section-heading::before {
    content: '';
    width: 4px;
    height: 24px;
    background: var(--gradient-accent);
    border-radius: 2px;
  }

  /* Section Text */
  .section-text {
    font-size: 1.05rem;
    line-height: 1.75;
    color: var(--color-text-muted);
    margin-bottom: 1.25rem;
  }

  /* Experience Timeline */
  .experience-timeline {
    position: relative;
    padding-left: 2rem;
  }

  .experience-timeline::before {
    content: '';
    position: absolute;
    left: 0;
    top: 0.5rem;
    bottom: 0.5rem;
    width: 2px;
    background: var(--color-border);
    border-radius: 1px;
  }

  /* Experience Item */
  .experience-item {
    position: relative;
    padding: 1.25rem 1.5rem;
    margin-bottom: 1rem;
    background: var(--color-surface);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-md);
    transition: all var(--transition-base);
  }

  .experience-item:hover {
    border-color: var(--color-primary);
    box-shadow: var(--shadow-md);
  }

  .experience-item::before {
    content: '';
    position: absolute;
    left: -2rem;
    top: 1.5rem;
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: var(--color-primary);
    border: 2px solid var(--color-surface);
    box-shadow: 0 0 0 2px var(--color-primary);
  }

  /* Current Job Styling */
  .experience-item.current {
    background: linear-gradient(135deg, rgba(30, 58, 95, 0.03) 0%, rgba(245, 158, 11, 0.02) 100%);
    border-left: 4px solid var(--color-secondary);
    padding: 1.5rem;
  }

  .experience-item.current::before {
    width: 14px;
    height: 14px;
    background: var(--color-secondary);
    box-shadow: 0 0 0 3px rgba(245, 158, 11, 0.3);
    left: calc(-2rem - 2px);
  }

  .job-title {
    font-family: var(--font-display);
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--color-text);
  }

  .current .job-title {
    font-size: 1.2rem;
  }

  .company {
    font-weight: 500;
    color: var(--color-primary);
  }

  .company a {
    color: var(--color-primary);
    text-decoration: none;
    border-bottom: 1px solid transparent;
    transition: border-color var(--transition-fast);
  }

  .company a:hover {
    border-bottom-color: var(--color-primary);
  }

  .years {
    display: inline-block;
    font-size: 0.85rem;
    color: var(--color-text-muted);
    margin-left: 0.75rem;
  }

  .current .years {
    background: rgba(245, 158, 11, 0.15);
    color: var(--color-text);
    padding: 0.2rem 0.6rem;
    border-radius: var(--radius-sm);
    font-weight: 500;
  }

  .job-description {
    margin-top: 0.75rem;
    font-size: 0.95rem;
    line-height: 1.6;
    color: var(--color-text-muted);
  }

  /* Focus Section */
  .focus-section {
    background: linear-gradient(135deg, rgba(30, 58, 95, 0.05) 0%, rgba(30, 58, 95, 0.02) 100%);
    border-left: 4px solid var(--color-primary);
    border-radius: var(--radius-md);
    padding: 1.75rem;
  }

  .focus-heading {
    font-family: var(--font-display);
    font-size: 1.35rem;
    font-weight: 700;
    color: var(--color-text);
    margin-bottom: 1rem;
  }

  /* Philosophy Section */
  .philosophy-section {
    background: var(--color-bg-warm);
    border-left: 4px solid var(--color-secondary);
    border-radius: var(--radius-md);
    padding: 1.75rem;
  }

  .philosophy-heading {
    font-family: var(--font-display);
    font-size: 1.35rem;
    font-weight: 700;
    color: var(--color-text);
    margin-bottom: 1rem;
  }

  /* Leadership Section */
  .leadership-section {
    background: var(--color-surface);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-md);
    padding: 1.75rem;
  }

  .leadership-heading {
    font-family: var(--font-display);
    font-size: 1.35rem;
    font-weight: 700;
    color: var(--color-text);
    margin-bottom: 1rem;
    position: relative;
    display: inline-block;
  }

  .leadership-heading::after {
    content: '';
    position: absolute;
    bottom: -4px;
    left: 0;
    width: 40%;
    height: 3px;
    background: var(--gradient-accent);
    border-radius: 2px;
  }

  .emphasis {
    color: var(--color-primary);
    font-weight: 600;
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

    .experience-timeline {
      padding-left: 1.5rem;
    }

    .experience-item::before {
      left: -1.5rem;
    }

    .experience-item.current::before {
      left: calc(-1.5rem - 2px);
    }

    .section-heading {
      font-size: 1.35rem;
    }

    .focus-section,
    .philosophy-section,
    .leadership-section {
      padding: 1.5rem;
    }

    .job-title {
      display: block;
      margin-bottom: 0.25rem;
    }

    .years {
      margin-left: 0;
      display: block;
      margin-top: 0.25rem;
    }
  }
</style>

<!-- Page Header -->
<div class="page-header">
  <h1>My Professional Journey</h1>
  <p>20+ years building software and leading engineering teams. I help organizations cut through the AI hype to build systems that actually work.</p>
</div>

<div class="background-container">
  <!-- Experience Section -->
  <div class="content-card">
    <h2 class="section-heading">Professional Experience</h2>

    <div class="experience-timeline">
      <div class="experience-item current">
        <span class="job-title">Founder & Principal Consultant</span>
        <span class="company">at PragmaNexus</span>
        <span class="years">(2024-Present)</span>
        <p class="job-description">I founded PragmaNexus to help teams cut through the AI hype and build systems that actually work. I focus on figuring out what's worth building first, then provide strategy, implementation, and training to make it happen.</p>
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
  </div>

  <!-- Current Focus Section -->
  <div class="content-card">
    <div class="focus-section">
      <h2 class="focus-heading">Current Focus: Large Language Models</h2>
      <p class="section-text">I'm building production systems in the large language model ecosystem - the kind that process real documents, handle actual customer data, and solve problems that weren't solvable before these tools existed. My work spans strategy, implementation, and training, helping teams figure out what's worth building and then building it right.</p>
    </div>
  </div>

  <!-- Philosophy Section -->
  <div class="content-card">
    <div class="philosophy-section">
      <h2 class="philosophy-heading">My Product-First Approach</h2>
      <p class="section-text">I believe the most important question isn't "Which technology should we use?" but "What business problems are we trying to solve?" I start with understanding your actual problems, then figure out what's worth building - whether that's an LLM application, traditional ML model, or simpler solution.</p>
      <p class="section-text" style="margin-bottom: 0;">This approach leads to focused solutions that solve real problems rather than chase technology trends. It's about using the right tool for the job and building something that works for your specific situation.</p>
    </div>
  </div>

  <!-- Leadership Section -->
  <div class="content-card">
    <div class="leadership-section">
      <h2 class="leadership-heading">Leadership Philosophy</h2>
      <p class="section-text">I believe effective leadership multiplies a team's impact. Throughout my career, I've prioritized building, coaching, and mentoring engineering teams. Nothing frustrates me more than seeing exceptional talent stifled by inadequate leadership.</p>
      <p class="section-text" style="margin-bottom: 0;">My leadership approach centers on empowering teams to do their best work. This means clear communication, thoughtful delegation, and creating an environment where innovation thrives. This experience in coaching and mentoring teams is why training and strategy work are such important parts of what I offer - the best systems are ones that teams can understand, maintain, and improve.</p>
    </div>
  </div>
</div>
