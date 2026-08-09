---
layout: splash
title: Work With Me
permalink: /work-with-me.html
---

<style>
  .work-page {
    max-width: 1040px;
    margin: 0 auto;
    padding: 4.5rem 1.5rem 4rem;
  }

  .work-hero {
    display: grid;
    grid-template-columns: minmax(0, 1.25fr) minmax(280px, 0.75fr);
    gap: 4rem;
    align-items: start;
    padding-bottom: 3.5rem;
    border-bottom: 1px solid var(--color-border);
  }

  .work-kicker {
    margin: 0 0 0.85rem !important;
    color: var(--color-primary);
    font-size: 0.74rem;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }

  .work-page h1 {
    max-width: 650px;
    margin: 0 0 1.25rem;
    font-family: var(--font-serif);
    font-size: clamp(2.65rem, 5.3vw, 4rem);
    font-weight: 400;
    line-height: 1.02;
    letter-spacing: -0.03em;
  }

  .work-lead {
    max-width: 640px;
    margin: 0 !important;
    color: var(--color-text-muted);
    font-size: 1.08rem;
    line-height: 1.6;
  }

  .work-services {
    padding: 1.5rem;
    border: 1px solid var(--color-border);
    border-top: 3px solid var(--color-primary);
    border-radius: 10px;
    background: var(--color-surface);
  }

  .work-services h2 {
    margin: 0 !important;
    padding: 0 0 0.75rem !important;
    border: 0 !important;
    color: var(--color-text);
    font-family: var(--font-display);
    font-size: 0.86rem !important;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  .page__content .work-service-list {
    margin: 0 !important;
    padding: 0 !important;
    list-style: none;
  }

  .page__content .work-service-list li {
    margin: 0 !important;
    padding: 0.72rem 0 !important;
    border-bottom: 1px solid var(--color-border);
    color: var(--color-text);
    font-size: 0.92rem;
    line-height: 1.4;
  }

  .page__content .work-service-list li:last-child {
    padding-bottom: 0 !important;
    border-bottom: 0;
  }

  .work-approach {
    display: grid;
    grid-template-columns: 190px minmax(0, 1fr);
    gap: 3rem;
    padding: 3rem 0;
  }

  .work-approach h2 {
    margin: 0 !important;
    padding: 0 !important;
    border: 0 !important;
    font-family: var(--font-serif);
    font-size: 1.75rem !important;
    font-weight: 400;
    line-height: 1.1;
  }

  .work-copy {
    max-width: 680px;
  }

  .work-copy p {
    margin: 0 0 0.85rem !important;
    color: var(--color-text);
    font-size: 1rem;
    line-height: 1.65;
  }

  .work-copy p:last-child {
    margin-bottom: 0 !important;
  }

  .work-cta {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 2rem;
    padding: 1.5rem 1.65rem;
    border-left: 3px solid var(--color-secondary);
    border-radius: 8px;
    background: var(--color-surface-elevated);
  }

  .work-cta p {
    margin: 0 !important;
    color: var(--color-text-muted);
    font-size: 0.94rem;
    line-height: 1.5;
  }

  .work-actions {
    display: flex;
    flex-shrink: 0;
    flex-wrap: wrap;
    gap: 0.6rem;
  }

  .work-action {
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

  .page__content a.work-action {
    border-bottom: 1px solid var(--color-primary);
  }

  .work-action.secondary {
    background: transparent;
    color: var(--color-primary) !important;
  }

  @media (max-width: 820px) {
    .work-page { padding: 3rem 1rem; }
    .work-hero { grid-template-columns: 1fr; gap: 2.25rem; padding-bottom: 2.5rem; }
    .work-services { max-width: none; }
    .work-approach { grid-template-columns: 1fr; gap: 1.25rem; padding: 2.5rem 0; }
    .work-cta { align-items: flex-start; flex-direction: column; gap: 1.25rem; }
  }

  @media (max-width: 520px) {
    .work-page h1 { font-size: 2.65rem; }
    .work-actions { width: 100%; }
    .work-action { justify-content: center; width: 100%; }
  }
</style>

<div class="work-page">
  <section class="work-hero">
    <div>
      <p class="work-kicker">Client work</p>
      <h1>Consulting through PragmaNexus.</h1>
      <p class="work-lead">I help teams define a specific problem, build the software, and put it into production. I can work with an engineering team or handle the technical work myself.</p>
    </div>

    <aside class="work-services">
      <h2>Typical work</h2>
      <ul class="work-service-list">
        <li>Internal AI tools</li>
        <li>ML and data systems</li>
        <li>AI project reviews</li>
        <li>AI coding practices for engineers</li>
      </ul>
    </aside>
  </section>

  <section class="work-approach">
    <h2>How I work</h2>
    <div class="work-copy">
      <p>I start by learning how the work gets done and what needs to change. From there, the work might be an assessment, a focused prototype, an improvement to an existing system, or a production build.</p>
      <p>I work in short cycles using real data and feedback from the people doing the job. We adjust the plan as we learn more.</p>
      <p>Sometimes the answer is an AI system. Sometimes it is traditional software, a process change, or a decision not to build anything.</p>
    </div>
  </section>

  <section class="work-cta">
    <p>See the PragmaNexus site for case studies and contact information.</p>
    <div class="work-actions">
      <a class="work-action" href="https://pragmanexus.com">Visit PragmaNexus</a>
      <a class="work-action secondary" href="https://pragmanexus.com/case-studies.html">See case studies</a>
    </div>
  </section>
</div>
