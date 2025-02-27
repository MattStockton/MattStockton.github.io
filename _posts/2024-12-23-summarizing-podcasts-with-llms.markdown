---
layout: single
title: "Summarizing Podcasts with LLMs (Using o1 Pro)"
excerpt: "I use LLMs to summarize podcasts into structured takeaways, making it easier to revisit key insights. This post walks through my workflow — meta-prompting, refining outputs, and generating summaries. If you want to extract useful details from long-form content, here’s how I do it."
---

I’ve been experimenting with using LLMs to distill key details from podcasts. I listen to most episodes while running and afterwards want a succinct record of what stood out. Below is how I approach that process, along with a look at two summary artifacts I created from a recent High Agency Podcast episode - [How to build great AI products with Vanta Software Developer Noam Rubin](https://www.youtube.com/watch?v=PdT8STmhUqg). I used o1 pro for all of this - I recently got access to this model, and have been experimenting with it to see how it works differently than previous OpenAI models.


## Why Summarize Podcasts with LLMs?

1. **Active Reflection**  
   After listening, I want a quick reference to specific insights that captured my attention. Summaries let me extract and organize the big ideas so I can revisit them later without scrubbing through an entire recording.

2. **Efficient Note-Taking**  
   Since I usually run while listening, it’s not practical to jot notes in real time. Asking an LLM for the highlights and direct quotes from a transcript acts as my “post-run” notebook. I can guide it to the aspects I found interesting within the prompts.

3. **Potential for Reuse**  
   Once I have a concise summary, I can share parts of it in a blog post or keep it for personal reference. This reusability is one of the biggest advantages of a well-structured summary.

---

## My Summarization Workflow

Below is a simplified breakdown of my usual process. I adjust the details (like how I phrase the prompts) depending on the type of content I’m summarizing and what my objectives are.

### 1. Listen First, Note What’s Interesting
I go through the podcast episode once, mentally flagging interesting moments or quotes. In this case, Vanta’s approach to rigorous AI testing and domain-expert collaboration were two interesting areas.

### 2. Generate a Full Prompt Using Meta-Prompting
Next, I work with an LLM to *build* the exact instructions I’ll need for summarizing. A typical meta-prompt for me might look like this:

> **“Please build me a prompt for an LLM to analyze a transcript of a podcast, using the following instructions: Break it down into one-minute increments. For each one-minute block, produce a short summary of at most four sentences focusing on the key takeaway. Include a direct quote, but do not count this quote in your four-sentence limit. If a minute doesn’t have a meaningful point, combine it with the next. Overall, select the 20 most compelling points from the entire transcript and rank them from highest to lowest importance.”**

I can adjust the output prompt based on my goals — sometimes I want a high-level summary, other times I need more technical depth. One aspect to clarify is that I usually provide more detail about what 'importance' means. LLMs perform better if you provide specific instructions - importance is a concept that can mean many things, and it's useful to be more specific. 

### 3. Provide the Transcript
After finalizing the prompt, I feed the full podcast transcript (often copied from YouTube’s auto-generated captions) into the LLM alongside the instructions.

### 4. Refine the Summaries
After getting the initial output, I iterate. If quotes lack context, I request more detail. If certain points don’t match what I found compelling, I ask the LLM to reorder them or expand on specific items. It depends on my goals, and the current state of the outputs, but I've found it useful to have more of a 'conversation' to get to the final result.

### 5. Remix (As Needed)
Depending on how I plan to use the summary, I may switch up the format. If it’s purely for personal recall, I might just have the LLM expand on a few bullet items I found particularly interesting. But if I’m aiming for a distribution-ready overview, I could request a narrative “one-pager.” There’s no single “right” way — it all depends on the goal.

### 6. Publish Excerpts or Archive
Occasionally, I share snippets in a blog post (like this one). I’ve found that if I really want to remember something and go back to it, it’s easier to store it publicly on my website rather than in a private Notion.

---

## Two Summaries of the Vanta Episode

I tested this workflow on the episode linked above. The conversation was packed with practical advice for anyone building AI features at scale. Below are two final outputs I created, each linked in full:

1. **[Key Takeaways](/docs/assets/pdfs/build_ai_products_key_excerpts.pdf)**  
   A multi-point list capturing 10 core insights — everything from focusing on real user value, to using “golden sets” for thorough evaluation, to dogfooding your own product. Each item includes a direct quote.

2. **[One-Pager](/docs/assets/pdfs/build_ai_products_summary.pdf)**  
   A concise, narrative-style rundown of how Vanta systematically adopts AI for security and compliance. It distills the previous list into a shorter, more narrative version.  

## Final Thoughts

- **Experimentation Is Essential**: Finding a process that works takes iteration and patience. Be ready to play around with prompt language, formatting, and the level of detail you need.  
- **Refining Your Written Language**: The more precise and thoughtful your prompts (and your follow-up instructions), the better the results.  
- **Focus on What Works for You**: Whether you only need a few bullet points or a full narrative, tweak the workflow until it fits your needs — and remember that your process can evolve over time.