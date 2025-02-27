---
layout: single
title: "Summarizing with LLMs: Video Walkthrough"
excerpt: "I recorded a video showing how I use LLMs to summarize podcast transcripts into concise, structured insights. This post covers the workflow, key takeaways, and how tools like the LLMOps database can help builders working with AI. If you're summarizing long-form content, here's how to do it efficiently."
---

In a previous [blog post](/2024/12/23/summarizing-podcasts-with-llms.html), I walked through how I use LLM tools to summarize podcast transcripts into concise, useful summaries. This time, I thought it might be helpful to create a video tutorial to show how the process works. Beyond the workflow itself, I also wanted to highlight two fantastic resources for builders working with LLMs: the [Vanishing Gradients](https://vanishinggradients.fireside.fm/43) podcast episode with [Alex Strick van Linschoten](https://x.com/strickvl), and Alex's [LLMOps database](https://www.zenml.io/llmops-database). If you're building systems with LLMs, these are well worth exploring.


<iframe width="560" height="315" src="https://www.youtube.com/embed/3nhqXDiTZ6U?si=5d8LwsrDrRZoQ_9Z" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## The Podcast and LLMOps Database  

The [LLMOps database](https://www.zenml.io/llmops-database) is packed with examples of how companies are implementing large language models. You can filter by industry, technology, or use case, and each entry links back to its original source. It’s a great way to discover ideas or just see what’s possible in this space.

The [Vanishing Gradients episode](https://vanishinggradients.fireside.fm/43) dives deep into building systems with LLMs. What stood out to me is Alex’s focus on applying solid engineering principles — testing, simplicity, and problem-first thinking — even when working with cutting-edge AI tools. If you're a builder looking for practical advice, both the database and this podcast episode are excellent starting points.


## My Workflow for Summarizing Podcasts with LLMs

Here’s a quick recap of how I use LLMs to summarize podcast transcripts, as demonstrated in the video. There is nothing complicated. The most important part is the attention and detail in the prompt itself.

1. **Get the transcript**  
   I either download the transcript or generate it using tools if it’s not readily available.  

2. **Write a detailed prompt**  
   I outline exactly how I want the summary structured — length, quotes, priorities, etc.

3. **Run the prompt through the LLM**  
   For this example, I used o1 pro, but other models also work well.

4. **Review and refine**  
   I go through the summary, adjust the prompt if needed, and re-run it. This iteration helps me better understand the content and refine the result.

Here’s the prompt I used in this example:

> ```plaintext
> Summarize the attached transcript of a podcast. Use these rules to create the summary:
> - Identify and summarize the 10 most valuable point discussed
> - Valuable in this context means: “How beneficial is this information for an Engineer who is building an LLM-based application?”
> - Each point should be summarized in 3 to 5 sentences, and should include a ‘header’ sentence that clearly and succinctly describes the essence of the point.
> - Include a direct quote after each summary, formatted as a blockquote, and clearly attribute it to the speaker. Ensure the quote is concise and relevant.
> - Prioritize points based on the potential impact and applicability to common challenges faced when building LLM-based applications
> - Include an overview paragraph providing the podcast title, host(s), guest(s), the primary focus of the discussion, and any key terms or concepts explained in the podcast.
> - Write in a professional but accessible tone suitable for engineers of varying expertise levels. Avoid technical jargon unless explained in the summary.
> - Ensure the overview paragraph flows logically into the summarized points. Maintain continuity and avoid redundancy across the points.
> ```

## Summary Output PDF

For this podcast, below are a few of the top take-aways. 

Also, here's [the full summary doc](/docs/assets/pdfs/llm_ops_summary.pdf) if you're interested as well.

**Start With the Problem, Not the Technology** - The most successful LLM-powered products do not start with “Let’s add AI!” but rather with a clear business or user need. This problem-first mindset guides the selection of model, design of the solution, and success metrics from the start. Companies that skip problem definition and go straight to adding AI often waste resources and end up with subpar products. Engineers should anchor all design and development in a real, validated problem to solve.

**Fundamentals Matter More Than Ever** - LLM-driven products still rely on classic software engineering best practices. These include DevOps essentials like stable deployments, robust error handling, scaling strategies, and version control for iterative improvements. Even though LLMs enable new kinds of capabilities, teams must not neglect the fundamentals that keep software functional and reliable at scale. When you mix complex machine intelligence with real user data, disciplined engineering is indispensable.

## Why This Workflow Works for Me  

This approach isn’t just about creating summaries; it’s about active learning. Writing the prompt, reviewing the summary, and iterating on the output forces me to further engage with the raw material. It helps me remember key ideas better than if I’d just listened passively.
