---
layout: single
title: "Building Production AI Evaluations: A Systematic, Domain-Driven Approach"
excerpt: "Teresa Torres went from zero AI experience to shipping production evaluations by combining domain expertise with systematic thinking - her journey shows how to build reliable AI systems without extensive ML background."
category: "Building with LLMs"
tags: ["evaluations", "domain-expertise", "product-management", "interview-coach"]
---

[Teresa Torres](https://www.producttalk.org/about/) went from product management coach to shipping an AI interview coach very quickly - with zero AI experience when she started. She built a tool that analyzes interview transcripts and gives students detailed feedback on their interviewing technique. Since the feedback quality directly impacts student learning, she needed systematic evaluations to ensure the AI wasn't reinforcing bad habits.

Evaluations are an essential part of building serious AI-driven applications, yet people often struggle with where to start - it feels overwhelming. Torres shows how combining domain expertise with systematic thinking and the right AI tools can get you from zero to production quickly.

Watch the full [talk with Hamel](https://www.youtube.com/watch?v=N-qAOv_PNPc) - I'll be pointing people to it when they want to learn how to start with evaluations. Here are the points that resonated most with me.

## Domain expertise beats everything else

Torres could build better evals than most engineers because she actually understands what makes a good interview. She's seen thousands of students make the same mistakes.

You need both: someone who understands what's right and wrong in the domain, plus someone who can translate that into code that works. Torres became both - domain expert and builder - which is honestly a superpower when building AI applications. The domain expertise lets you spot the simple solutions that actually work.

## Not everything requires a large language model

Torres needed to detect "general questions" in interview feedback. Instead of building an LLM-as-judge system, she realized one of her evaluation strategies could include simple text matching - checking if a question contained words like "typical," "usually," "generally."

> "What's funny about this very elementary eval is it has a really high alignment rate. like it never has false positives and it catches almost everything I catch."

This is interesting because sometimes you don't need elaborate LLM-as-judge evaluations. You should think through the right approach for everything - not everything requires a large language model. An engineer working alone would have definitely overthought this with complex prompts instead of simple text matching.

## Don't overemphasize the tool - just start

What I found smart about Torres' approach: she used Airtable to capture her traces and look at her data, then annotate from there. Not because it's optimal, but because getting started mattered more than finding the perfect tool.

This resonates because too many people get stuck on tooling decisions instead of actually looking at their data. Even using a text file is better than spending too much time evaluating specialized frameworks. The most important thing is to use something where you can capture your data and just get started.

The more time you spend researching and trying out tools is less time you're actually spending looking at input and output from the system you're building and reasoning about whether that output's good for your specific context.

## Manual annotation work is essential

Torres went through interview transcripts manually, listening and annotating them inline. She built a taxonomy of failure modes - "suggests a leading question," for example - and labeled them in her spreadsheet.

Many people skip this manual work, but it's essential. You have to look at live data and understand your failure patterns before you can code for them.

## Claude Code is perfect for building custom annotation tools

Torres used Claude Code to build custom annotation UIs when Airtable wasn't enough. She mentioned this strategy was more accessible than she expected it to be - you can "vibe code" your way to moderately complex interfaces without understanding implementation details.

I've also found Claude Code to be exceptional at quickly building tools that don't need to be the most robust and are for internal use cases. I'm never a fan of reinventing the wheel, but I'm coming around to the idea that building these little custom pieces of software is just so inexpensive now in terms of time that it's almost always worth it if it's small enough versus trying to figure out how to configure or use an off-the-shelf tool.

Building it yourself also forces you to acknowledge the real problem instead of adapting to generic tools.

## Figure out your workflow inputs and outputs

Like any system design, there are many different ways to structure your inputs, outputs, and workflows. Being thoughtful around this can go a long way. Torres' use case involves big transcripts, but she realized she could extract structured information once (questions, answers, coaching tips) then use those as inputs to evaluations. Both faster and cheaper than reprocessing everything repeatedly.

> "I can run all my helper functions once for all my transcripts. And then as I change a eval, the input data isn't changing. So I don't have to rerun all those helpers."

Spend time thinking about what different components or modules you should be building and how those things fit together. This modularization not only gives you better results, but lets you test individual pieces of your workflow more thoroughly. Instead of one big black box that's hard to debug, you can isolate problems to specific components.

## Breaking up workflows is often a trade-off

Torres highlighted an interesting trade-off and experimented with different modules she should test - ultimately deciding to run evaluations against the full LLM output versus individual components. I'm not sure exactly how I feel about this. There are different approaches and maybe the context under which you do this matters, but I liked how she experimented with both testing bigger components and then testing smaller components, ultimately settling on something that allowed her to work quickly but also still have good results. It's all about the outcomes, and an experimentation mindset to get you there.

## Fast feedback loops are the primary reason to build evaluations

You must build evaluations in order to have a systematic way to iteratively test changes you make to your application. The faster this feedback loop works, the faster and more confidently you can iterate. Torres built a system where she could make a change and then see exactly how it affected the things she cared about. Her traces-as-rows, evaluations-as-columns visualization gave her a quick smoke test of whether improvements actually changed anything meaningfully.

Having quantitative information about how your change impacted your results and being able to see that in real time gives you a superpower to iterate quickly.

## Measure before you try to improve

The ordering is important here. You should take a step back and figure out what exactly you're trying to measure and how you're going to measure that, then build that before you make the improvement. This mindset helps you avoid the pattern of breaking one thing while you fix another. Taking a systematic approach, which has always been true in classical software engineering, goes a long way even with these new large language model based systems.

## Final Thoughts

Torres' journey demonstrates what's possible when you combine domain expertise with systematic thinking. Her approach - starting simple, being methodical about measurement, leveraging domain knowledge for better decisions - shows how to build reliable AI systems even without extensive ML experience.

The self-directed learning aspect is crucial too, and that was a theme throughout. These tools are powerful for people who have the agency and persistence to work through problems systematically. If you're having trouble getting started with evaluations, Torres' [talk with Hamel](https://www.youtube.com/watch?v=N-qAOv_PNPc) shows exactly how systematic approaches and domain knowledge can guide you from complete beginner to production system.