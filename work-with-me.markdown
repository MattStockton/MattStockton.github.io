---
layout: default
title: Work With Me
permalink: /work-with-me.html
description: "I help teams turn a specific problem into working software, from AI products to internal tools and production ML."
---

<div class="wrap">
  <header class="page-head">
    <h1>Consulting through {{ site.company.name }}.</h1>
    <p class="lead">I help teams turn a specific problem into working software, from AI products to internal tools and production ML. I can work with an engineering team or handle the technical work myself.</p>
  </header>

  <div class="offer">
    <section aria-labelledby="what-heading">
      <h2 id="what-heading" class="label">Typical work</h2>
      <ul class="checklist">
        <li>Applied AI products and product features</li>
        <li>Agentic systems and workflows</li>
        <li>Internal AI tools</li>
        <li>ML and data systems</li>
        <li>Technical reviews and engineering practices</li>
      </ul>
    </section>

    <section aria-labelledby="how-heading">
      <h2 id="how-heading" class="label">How I work</h2>
      <div class="about-copy offer__copy">
        <p>Engagements start with the same question: what is the most important problem you are trying to solve, and where does AI actually add value for it?</p>
        <p>I start by understanding the users, the existing system, and what the software needs to do. From there, the work might be an assessment, a focused prototype, an improvement to an existing system, or a production build.</p>
        <p>I work in short cycles using real data and feedback from the people doing the job.</p>
        <p>Sometimes the answer is an AI system. Sometimes it's traditional software, a process change, or a decision not to build anything.</p>
        <p>Even the advisory work is hands-on, in the codebase. I judge the work by whether the team can test, operate, and maintain the result once I'm out of the picture.</p>
      </div>
    </section>
  </div>

  <section class="cases" aria-labelledby="cases-heading">
    <div class="section-head">
      <h2 id="cases-heading">Case studies</h2>
      <a class="text-link" href="{{ site.company.case_studies }}">On the {{ site.company.name }} site &nearr;</a>
    </div>
    <ul class="list">
      {% for title in site.data.case_studies %}
      <li class="list__row list__row--plain"><span class="list__title">{{ title }}</span></li>
      {% endfor %}
    </ul>
  </section>
</div>

{% include contact-cta.html %}
