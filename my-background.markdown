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

  @media (max-width: 760px) {
    .background-page { padding: 3rem 1rem; }
    .background-header { padding-bottom: 2.25rem; }
    .background-header h1 { font-size: 3rem; }
    .background-section { grid-template-columns: 1fr; gap: 1.25rem; padding: 2.5rem 0; }
    .background-principles { grid-template-columns: 1fr; gap: 2.5rem; padding-top: 2.5rem; }
    .years { width: 100%; margin: 0.2rem 0 0; }
    .experience-item.current { margin: 0; }
  }
</style>

<div class="background-page">
  <header class="background-header">
    <h1>Background</h1>
    <p>More than 20 years building software, data systems, and engineering teams.</p>
  </header>

  <section class="background-section">
    <h2>Current work</h2>
    <div class="current-copy">
      <p>I build software with client teams through PragmaNexus. Recent work includes investment research tools, document search and report generation, production machine learning, and AI-assisted software development.</p>
      <p>The projects combine software, data, machine learning, and language models. The goal is software that teams can test, operate, and maintain.</p>
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
        <p class="job-description">Build software with client teams, from technical assessment through production implementation.</p>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">Director of Engineering</span>
          <span class="company">at <a href="https://www.teamshares.com/">Teamshares</a></span>
          <span class="years">2021 to 2024</span>
        </div>
        <p class="job-description">Built the company's data infrastructure and started a software team. The platform gave acquisition and operations teams access to shared data and internal tools.</p>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">Director of Data Science and Engineering</span>
          <span class="company">at <a href="https://raconcapital.com/">Racon Capital Partners</a></span>
          <span class="years">2020 to 2021</span>
        </div>
        <p class="job-description">Worked with the Head of Quantitative Research to build investment algorithms and the infrastructure used to backtest and trade them.</p>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">Director of Engineering</span>
          <span class="company">at <a href="https://circleup.com/">CircleUp</a></span>
          <span class="years">2014 to 2020</span>
        </div>
        <p class="job-description">Helped build a data and machine learning platform that combined hundreds of sources to identify and analyze more than 100,000 consumer businesses. The platform supported investment and lending decisions.</p>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">VP of Engineering</span>
          <span class="company">at <a href="https://www.harqen.com/">Harqen</a></span>
          <span class="years">2010 to 2014</span>
        </div>
        <p class="job-description">Helped build a digital interviewing platform used by millions of applicants to submit recorded audio and video interviews.</p>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">Senior Software Engineer</span>
          <span class="company">at Stark Investments</span>
          <span class="years">2007 to 2010</span>
        </div>
        <p class="job-description">Built derivatives and credit default swap trading software for a multi-billion-dollar hedge fund during the 2007-2008 financial crisis.</p>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">Engineering Leadership Program</span>
          <span class="company">at General Electric</span>
          <span class="years">2004 to 2007</span>
        </div>
      </article>

      <article class="experience-item">
        <div class="experience-heading">
          <span class="job-title">iOS Developer</span>
          <span class="company">side projects</span>
          <span class="years">Late 2000s</span>
        </div>
        <p class="job-description">Built and released seven iOS applications.</p>
      </article>
    </div>
  </section>

  <div class="background-principles">
    <section class="background-principle">
      <h2>How I work</h2>
      <p>I prefer direct collaboration, working software, and feedback from the people who use it. The plan changes as we learn more.</p>
      <p>The answer might be a language model, traditional machine learning, ordinary software, or no new software at all.</p>
    </section>

    <section class="background-principle">
      <h2>Managing teams</h2>
      <p>A leader's job is to make good work easier. I care about clear goals, direct communication, sound technical judgment, and giving people room to own decisions.</p>
      <p>The team should understand its systems, maintain them, and know whether they work.</p>
    </section>
  </div>
</div>
