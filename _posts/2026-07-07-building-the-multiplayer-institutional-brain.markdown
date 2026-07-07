---
layout: single
title: "Building the Multiplayer Institutional Brain"
excerpt: "I joined Khe and Brett on the Invest with AI podcast to talk about how investment firms move from individual AI experimentation to a shared, firm-wide capability. These are the seven strategies from our conversation."
category: "AI Strategy & Leadership"
tags: ["podcasts", "ai-adoption", "investment-research", "skills", "workflows"]
---

I recently joined [Khe](https://x.com/khemaridh) and [Brett](https://x.com/FundamentEdge) on the [Invest with AI](https://www.fundamentedge.com/invest-with-ai-episodes/04) podcast to talk about the transition from individual AI experimentation to a shared "multiplayer" institutional brain. Most of our conversation was about process and communication, because in my experience that's where firms get stuck - more than on the technology itself.

![Building the multiplayer institutional brain: scaling AI from individual to institution](/docs/assets/images/invest-with-ai/institutional_brain.jpg)

Here are the core strategies from our discussion:

## 1. Start with the "Job to Be Done"

Identify specific, named workflows - reviewing earnings transcripts, summarizing SEC filings - and systematize them one at a time. Design each one around your firm's investment thesis and the specific lens you use to evaluate data. That's how context moves out of individual silos and into shared spaces where a model can apply your firm's approach.

## 2. Use Models as Thought Partners to Solve Articulation

About 80% of AI engineering is clear communication. Many experts are "intuitive pianists": they have masterful processes but struggle to write them down coherently. The models themselves are excellent interviewers for extracting that intent. My favorite version of this is to record a rambling voice memo of my thoughts, transcribe it, and ask the model to exhaustively ask me questions until it understands my intent and can turn it into structured instructions.

## 3. Prioritize Local Access for Deep Experimentation

To build a firm-wide brain, you first have to prove what works in a single-player environment. Get out of the browser and use harnesses like Codex or Claude Code that have direct access to your local file system. The model can open folders and look through things to find context on its own, which changes how fast you can iterate - I wrote more about this in [why tool calling and file system access matter](/2025/12/29/why-tool-calling-and-file-system-access-matter.html). You'll eventually move these workflows into a shared, centralized environment, but you can't prove the process until the tool can see the data you're working with.

## 4. Adopt a "Hill Climbing" Feedback Loop

Treat development as hill climbing: apply a red pen to the model's logic and iterate on its errors. The loop I use is to record a specific critique of what was good or bad about a particular output and feed that transcription back into the system to refine the underlying skill. Do this enough times and the model starts to speak your professional language and handle the nuanced calls correctly.

## 5. Build Durable "Skills" Instead of Custom Code

Build a firm-wide library of "skills": reusable, English-language recipes for specific tasks. Because they're written in plain language, they stay durable as you switch between underlying models like GPT or Claude. When a team member finds a recipe that works, it goes into a shared repository so the whole firm benefits.

## 6. Design for Adaptability and the "Bitter Lesson"

The half-life of an AI technique is short; be prepared to throw away or redo your work as models improve. Build workflows around the underlying intent and logic rather than rigid, over-prescribed instructions. Work built that way can be evolved and repurposed instead of going obsolete every time a new model ships.

## 7. Treat LLMs as Orchestrators

LLMs are one tool in your kit, and they're often the wrong tool for the job. They're non-deterministic, which makes them good at judgment and reasoning and unreliable at perfect math or quantitative analysis. Don't ask an LLM to perform calculations; use it as an orchestrator that triggers deterministic code or specialized tools to handle the numbers. Once a task is proven and repeatable, move it to smaller, cost-optimized models for better efficiency at scale.

---

My advice has been consistent through this entire AI wave: **there are no shortcuts**. The only way to get good at this and understand what works for your lens is to put in the time - it's [what I tell everyone getting started](/2026/01/29/what-i-tell-people-getting-started-with-claude-code.html). As we said on the podcast, hitting a professional level of fluency usually takes hundreds of hours of hands-on work. The tools will keep shifting; the time you spend in the weeds is what carries over. You have to get in there and find the "aha moments" for yourself.

If you want the full conversation, you can listen to the [complete episode](https://www.fundamentedge.com/invest-with-ai-episodes/04) on the Fundament Edge site.
