---
layout: splash
title: Background
---

<style>
  .background-page {
    max-width: 1040px;
    margin: 0 auto;
    padding: 4.5rem 1.5rem 4rem;
  }

  .background-header {
    padding-bottom: 3rem;
    border-bottom: 1px solid var(--color-border);
  }

  .background-header h1 {
    margin: 0 0 1rem;
    font-family: var(--font-serif);
    font-size: clamp(3rem, 6vw, 4.5rem);
    font-weight: 400;
    line-height: 1;
    letter-spacing: -0.035em;
  }

  .background-header p {
    max-width: 700px;
    margin: 0 !important;
    color: var(--color-text-muted);
    font-size: 1.08rem;
    line-height: 1.6;
  }

  .background-section {
    display: grid;
    grid-template-columns: 190px minmax(0, 1fr);
    gap: 3rem;
    padding: 3rem 0;
    border-bottom: 1px solid var(--color-border);
  }

  .background-section > h2,
  .background-principle h2 {
    margin: 0 !important;
    padding: 0 !important;
    border: 0 !important;
    font-family: var(--font-serif);
    font-size: 1.75rem !important;
    font-weight: 400;
    line-height: 1.1;
  }

  .current-copy p,
  .background-principle p {
    margin: 0 0 0.85rem !important;
    color: var(--color-text);
    font-size: 0.98rem;
    line-height: 1.65;
  }

  .current-copy p:last-child,
  .background-principle p:last-child {
    margin-bottom: 0 !important;
  }

  .experience-list {
    border-top: 1px solid var(--color-border);
  }

  .experience-item {
    padding: 1.35rem 0;
    border-bottom: 1px solid var(--color-border);
  }

  .experience-item.current {
    margin: 0 -1rem;
    padding: 1.35rem 1rem;
    border-left: 3px solid var(--color-secondary);
    background: var(--color-surface-elevated);
  }

  .experience-heading {
    display: flex;
    align-items: baseline;
    flex-wrap: wrap;
    gap: 0.25rem 0.5rem;
  }

  .job-title {
    color: var(--color-text);
    font-family: var(--font-display);
    font-size: 0.98rem;
    font-weight: 700;
  }

  .company {
    color: var(--color-primary);
    font-size: 0.9rem;
    font-weight: 500;
  }

  .company a {
    color: var(--color-primary) !important;
    text-decoration: none !important;
    border-bottom: 1px solid transparent !important;
  }

  .company a:hover {
    border-bottom-color: var(--color-primary) !important;
  }

  .years {
    margin-left: auto;
    color: var(--color-text-light);
    font-size: 0.76rem;
    white-space: nowrap;
  }

  .job-description {
    max-width: 690px;
    margin: 0.55rem 0 0 !important;
    color: var(--color-text-muted);
    font-size: 0.88rem;
    line-height: 1.55;
  }

  .background-principles {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 4rem;
    padding: 3rem 0 0;
  }

  .background-principle {
    padding-top: 1.25rem;
    border-top: 3px solid var(--color-primary);
  }

  .background-principle:last-child {
    border-top-color: var(--color-secondary);
  }

  .background-principle h2 {
    margin-bottom: 1rem !important;
  }

  .background-outro {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 2rem;
    margin-top: 3.5rem;
    padding: 1.5rem 1.65rem;
    border-left: 3px solid var(--color-secondary);
    border-radius: 8px;
    background: var(--color-surface-elevated);
  }

  .background-outro p {
    margin: 0 !important;
    color: var(--color-text-muted);
    font-size: 0.94rem;
    line-height: 1.5;
  }

  .background-actions {
    display: flex;
    flex-shrink: 0;
    flex-wrap: wrap;
    gap: 0.6rem;
  }

  .background-action {
    display: inline-flex;
    min-height: 44px;
    align-items: center;
    padding: 0.7rem 1.1rem;
    border: 1px solid var(--color-primary);
    border-radius: 6px;
    background: var(--color-primary);
    color: #fff !important;
    font-size: 0.95rem;
    font-weight: 650;
    text-decoration: none;
  }

  .page__content a.background-action {
    border-bottom: 1px solid var(--color-primary);
  }

  .background-action.secondary {
    background: transparent;
    color: var(--color-primary) !important;
  }

  @media (max-width: 760px) {
    .background-page { padding: 3rem 1rem; }
    .background-header { padding-bottom: 2.25rem; }
    .background-header h1 { font-size: 3rem; }
    .background-section { grid-template-columns: 1fr; gap: 1.25rem; padding: 2.5rem 0; }
    .background-principles { grid-template-columns: 1fr; gap: 2.5rem; padding-top: 2.5rem; }
    .years { width: 100%; margin: 0.2rem 0 0; }
    .experience-item.current { margin: 0; }
    .background-outro { flex-direction: column; align-items: flex-start; gap: 1.25rem; margin-top: 2.5rem; }
    .background-actions { width: 100%; }
    .background-action { justify-content: center; width: 100%; }
  }
</style>

<div class="background-page">
  <header class="background-header">
    <h1>Background</h1>
    <p>More than 20 years building software and data infrastructure, about a decade of it in machine learning and AI. Most of that has been at investment firms and venture-backed fintech companies, building trading systems, investment platforms, and the data infrastructure underneath them.</p>
  </header>

  <section class="background-section">
    <h2>Current work</h2>
    <div class="current-copy">
      <p>I run <a href="https://pragmanexus.com">PragmaNexus</a>. Most of my recent work is applied AI for investment research: document search and report generation, workflow automation, and data analysis tools. I also work with teams in fintech, healthcare and life sciences, and consumer software.</p>
      <p>Engagements start with the same question: what is the most important problem you are trying to solve, and where does AI actually add value for it? From there I build it. Even the advisory work is hands-on, in the codebase.</p>
      <p>I judge the work by whether the team can test, operate, and maintain the result once I'm out of the picture.</p>
    </div>
  </section>

  <section class="background-section">
    <h2>Experience</h2>
    <div class="experience-list">
      <article class="experience-item current">
        <div class="experience-heading">
          <span class="job-title">Founder and Principal Consultant</span>
          <span class="company">at PragmaNexus</span>
          <span class="years">2024 to present</span>
        </div>
        <p class="job-description">Work runs from technical assessment and prototyping through production build.</p>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">Director of Engineering</span>
          <span class="company">at <a href="https://www.teamshares.com/">Teamshares</a></span>
          <span class="years">2021 to 2024</span>
        </div>
        <p class="job-description">First data leader at a company moving small businesses to employee ownership. Built the data infrastructure that ingested financial data from nearly 100 businesses, and hired the first data team.</p>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">Director of Data Science and Engineering</span>
          <span class="company">at <a href="https://raconcapital.com/">Racon Capital Partners</a></span>
          <span class="years">2020 to 2021</span>
        </div>
        <p class="job-description">Sole engineer for a quantitative macro investment strategy, working directly with the investment team. Owned the whole stack: terabytes of financial data, model orchestration, and risk tools for portfolio exposure.</p>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">Director of Engineering</span>
          <span class="company">at <a href="https://circleup.com/">CircleUp</a></span>
          <span class="years">2014 to 2020</span>
        </div>
        <p class="job-description">Built and led the engineering team behind CircleUp's platform for sourcing and scoring consumer packaged goods companies for investment. Started with one data scientist and one engineer, and grew to analyzing more than 100,000 businesses.</p>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">VP of Engineering</span>
          <span class="company">at <a href="https://www.harqen.com/">Harqen</a></span>
          <span class="years">2010 to 2014</span>
        </div>
        <p class="job-description">Joined as a full-stack engineer and grew into leading the team. Four of us ran the entire stack for an asynchronous video and voice interviewing platform, including the telephony infrastructure. Millions of applicants used it.</p>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">iPhone Developer</span>
          <span class="company">independent</span>
          <span class="years">2009 to 2013</span>
        </div>
        <p class="job-description">Launched six apps to the App Store. One passed 100,000 downloads.</p>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">Senior Software Engineer</span>
          <span class="company">at Stark Investments</span>
          <span class="years">2007 to 2010</span>
        </div>
        <p class="job-description">Built derivatives and credit default swap trading software for a $14 billion hedge fund, through the 2007-2008 financial crisis.</p>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">Software Security Engineer</span>
          <span class="company">at General Electric</span>
          <span class="years">2004 to 2007</span>
        </div>
        <p class="job-description">Started in the Edison Engineering Development Program, rotating through software, firmware, quality, and service. Then wrote software that made network-connected medical devices safer: authentication, authorization, audit, and intrusion detection. Filed several patent applications.</p>
      </article>
    </div>
  </section>

  <div class="background-principles">
    <section class="background-principle">
      <h2>How I think about the work</h2>
      <p>Direct collaboration, working software early, and feedback from the people who actually use it. The plan changes as we learn more, and that is usually a good sign.</p>
      <p>I spend as much time deciding what not to build as what to build.</p>
    </section>

    <section class="background-principle">
      <h2>Managing teams</h2>
      <p>A leader's job is to make good work easier: clear goals, direct communication, sound technical judgment, and room for people to own decisions.</p>
      <p>I've started teams from one or two engineers more than once. The team should understand the systems it runs, be able to maintain them, and know whether they are working.</p>
    </section>
  </div>

  <section class="background-outro">
    <p>I write about this work here, and take on client projects through PragmaNexus.</p>
    <div class="background-actions">
      <a class="background-action" href="/writing.html">Read the writing</a>
      <a class="background-action secondary" href="/work-with-me.html">Work with me</a>
    </div>
  </section>
</div>
