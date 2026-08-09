---
layout: single
title: "Using OpenAI's Deep Research"
excerpt: "OpenAI's Deep Research generates structured reports with citations in minutes, making research faster and more efficient. I tested it for portfolio analysis, using meta-prompting to refine my queries. Here's how it streamlined my decision-making and how you can use it too."
category: "Building with LLMs"
tags: ["deep-research", "openai", "research", "portfolio-analysis", "meta-prompting"]
---

When you need deep, structured research on a topic, the usual approach is slow — digging through sources, organizing notes, and synthesizing insights. OpenAI’s [Deep Research](https://openai.com/index/introducing-deep-research/) changes that, generating baseline structured reports with citations in minutes. Instead of manually compiling information, you can describe your research goal, and the tool will return a well-organized summary backed by sources.  

I wanted to see how well it fit into my workflow, so I tested it during our yearly portfolio rebalance. My task was straightforward: evaluate three mutual funds we held and decide whether to keep them or swap them for better alternatives. I wanted an analysis that considered fund performance, ratings, tax drag, historical returns, and fees — a structured breakdown to help me reach a decision.  

## The Workflow  

I used a technique called **meta-prompting**, where you ask an LLM to help craft a prompt to use as a follow-on prompt. One of the biggest advantages of meta-prompting is that you don’t have to get the prompt right the first time. Instead of carefully constructing a perfect query, you can **just talk** — describe what you're trying to do in plain language, dump your thoughts, and refine as you go. With a little back and forth, you can guide the model to generate a well-structured prompt.  

I used this approach with ChatGPT 4o, asking it to help me build a Deep Research query. I described my goal in simple terms: compare three mutual funds against alternatives based on performance, fees, tax drag, and historical returns. ChatGPT helped refine my request, turning my rough explanation into a structured query that I could then feed into Deep Research.  


### Research Report  

I compiled the full exercise into a single document. It includes:

- The meta-prompting process – How I used ChatGPT to refine my Deep Research query.
- The final Deep Research prompt – The exact input I used to generate the structured report.
- The full research report – The output from Deep Research, providing a structured analysis of the three mutual funds I was evaluating.

📄 [View the full document (PDF)](/docs/assets/pdfs/open_ai_deep_research_mutual_funds.pdf)

## Results  

The Deep Research report provided a structured breakdown of the three mutual funds, outlining historical performance, fee structures, and tax implications. It also surfaced alternative funds with better metrics. What stood out was how the report framed trade-offs — whether a fund’s tax efficiency outweighed slightly higher fees, or whether a lower-cost alternative had a risk profile that justified switching.  

This didn’t replace my own judgment, but it streamlined the decision-making process. Instead of spending hours gathering data from multiple sources, I could focus on interpreting the results and weighing my options.  

## Why This Is Useful  

Getting structured research on demand makes it easier to evaluate complex questions. In this case, instead of spending hours gathering fund performance data from multiple sources, I could focus directly on deciding whether to adjust my holdings.  

The most valuable part of this process was how little effort it took to create a solid Deep Research query. Instead of trying to write the perfect prompt up front, I described my task in plain language and let ChatGPT handle the formatting. That step alone saved time and made the workflow smoother.  

## Exploring Other Tools in This Space  

OpenAI isn’t the only company offering a Deep Research tool — **Perplexity AI** and **Google** have similar features as well. Each has its own approach to sourcing and structuring information, so if you're curious about trying them out, it's worth doing your own research to see how they compare and which one fits your needs best.  

These tools change quickly, so it is worth testing the same task in more than one of them. I am interested in hearing what works for other people.

If you’ve been experimenting with Deep Research, I’d love to hear how you’re using it and what prompting techniques have worked well for you.
