---
layout: single
title: "How I Used LLMs to Summarize Workflow Hacks from a Twitter Thread"
excerpt: "I used an LLM to distill insights from a Twitter thread on AI workflow hacks — turning a noisy flood of replies into a clear, structured top 10 list. The process itself became a meta-experiment in using AI to cut through information overload efficiently."
category: "Building with LLMs"
tags: ["summarization", "twitter-threads", "workflow-hacks", "information-processing", "meta-usage"]
---

Twitter is the absolute highest signal for learning about leading-edge LLM advancements -- if you follow the right people. That said, it’s also overwhelming and noisy, and keeping up can easily consume time you should spend building. 

I experimented with using an LLM to distill insights from a Twitter thread packed with advice on workflow hacks. The goal was to create a concise list of actionable tips while minimizing the usual time sink of scrolling through replies. The process itself turned into a fun meta use case of leveraging AI. Here’s how I did it.

## The Original Thread

The starting point was [this Twitter thread](https://x.com/SullyOmarr/status/1854938666126258562) by SullyOmarr:

> *"Every AI power user I talk to has some workflow hack they think is obvious.  
> eg: for me it's voice—10x faster for prompts than typing.  
> What's your 'obvious' AI workflow that others should know about?"*

It received a flood of responses with interesting ideas, both common and unique. I wanted to consolidate and summarize these replies into a "Top 10 Workflow Hacks" list that captured both frequently mentioned tips and contrarian gems.


## The Process

Here’s the full step-by-step breakdown of how I tackled this:

1. **Screen Recording the Replies**  
   Using QuickTime on my Mac, I scrolled through the thread’s replies and recorded the screen to capture everything. This was much faster than copying text or screenshots.

2. **Drafting a Prompt**  
   I headed to Anthropic’s Prompt Workbench and wrote an initial prompt to guide the summarization process. The idea was to upload the screen recording into a multi-modal LLM (Gemini) for analysis. My prompt was:

   > *"I found a great Twitter thread. The initial prompt was:  
   > 'Every AI power user I talk to has some workflow hack they think is obvious...'  
   > There were many responses. I took a screen recording where I scrolled through all the replies. From this, I want to create a succinct list of the 'top 10 hacks' to use. I want each hack to be clear. I want it to be based on both the frequency of suggestion, but also include anything that is unique/contrarian. I will use a multi-modal LLM where I will upload the screen capture."*

3. **Using Gemini**  
   I uploaded the screen capture and the prompt to Gemini, which gave me a decent initial list. 

4. **Iterative Refinement**  
   After reviewing Gemini’s output, I revised the prompt to make the list more specific, include quotes from the replies, and highlight any “hidden gems” buried in the thread. Gemini refined the list, and the result was solid.

5. **Final Touches**  
   I made a few final edits to polish the wording and structure of the list. Below is the finished product.


## The Final List of AI Workflow Hacks

Here are the top 10 workflow hacks from the thread, compiled and refined with the help of Gemini:

1. **Voice Input**  
   *SullyOmarr*: "For me it's voice. 10x faster for prompts than typing." Voice input speeds up brainstorming and initial prompting significantly.

2. **Break Down Complex Tasks**  
   *NickDobos*: "Copy-paste your to-do list [...] and ask GPT to break it down into smaller steps, like doing dishes." This approach tackles procrastination by simplifying tasks.

3. **Cursor as a Powerful Tool**  
   *JasonSigmon*: "Using Cursor to write out longer posts, essays, or writings." *SullyOmarr* adds: "Cursor as a note-taking app is underrated!" Cursor is more than an editor; it’s a central hub for writing and organizing.

4. **Markdown for LLMs and Humans**  
   *Olivier Manuel*: "Use markdown. It is structured, human-readable, and LLMs understand the structure." Markdown bridges clear communication between humans and AI.

5. **Iterative Prompting: Voice to Text**  
   *Millin Gabani*: "Voice in -> text out interface for brainstorming with AI." Combines the speed of voice with the precision of text for refining prompts.

6. **Custom GPTs for Specific Projects**  
   *Florian S*: "Create a private Custom GPT in ChatGPT for each of your software projects." This maintains project-specific context and saves setup time.

7. **Modular Prompts for Complex Tasks**  
   *RethyNK AI*: "Using modular prompts—breaking down complex tasks into smaller, clear steps and feeding them into the AI iteratively." This enhances accuracy and focus.

8. **Automated Transcription for AI Input**  
   *Uttam Kumar*: "I have ChatGPT voice interview me, then we use the transcript as source material for our content." Great for repurposing audio/video material.

9. **Specificity in Prompts**  
   *Clifton*: "[As an expert prompt engineer, write a] clear, concise, and specific prompt optimized for [...]" Hidden gem: *AlbertPCoH*: "Speak broken English to LLMs," emphasizing simplicity in prompts.

10. **Contextual Background Documents**  
   *Gerrad Lipscombe*: "Have a series of background documents that you can toggle on/off for specific tasks as context." Saves time and ensures consistency by avoiding repetitive inputs.

## Closing Thoughts

This was a fun experiment, not just for summarizing insights, but also for exploring how LLMs can support workflows in a meta way. It’s worth noting that this blog post itself was created using ChatGPT (LLM inception at work!). For reference, I’ll post the full raw notes below alongside this post. This is what I fed into ChatGPT

Good luck building. Here's the prompt input:
<br/>
<img src="/docs/assets/images/twitter-summary/1.png" width="700px" height="700px"/>
<br/>
...
<br/>
<img src="/docs/assets/images/twitter-summary/2.png" width="700px" height="700px"/>