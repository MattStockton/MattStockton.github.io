---
layout: single
title: "Tool Calling and the Value of Understanding AI More Deeply"
excerpt: "Understanding how AI building blocks like tool calling work gives you a framework for figuring out where AI fits into the problems you're actually trying to solve."
category: "Building with LLMs"
tags: ["tool-calling", "ai-fundamentals", "ai-tools", "llm-architecture"]
---

Everyone has areas where they go deep and areas where they don't. AI is one where going a bit deeper pays off - not because you need to become an expert, but because AI applies to so many different problems. When you understand the building blocks, you can pattern match against what you're actually trying to solve.

One building block worth understanding is tool calling. This post explains what it is, why it matters, and how you might use it - but more broadly, understanding tool calling gives you a better appreciation for how these models actually work.

## What Tool Calling Actually Is

At their core, LLMs predict the next word based on patterns in text. If you could load all the text on the internet into your brain, you'd probably be pretty good at predicting the next word too. ([3Blue1Brown has an excellent video](https://www.youtube.com/watch?v=LPZh9BOjkQs) that goes deeper on the mechanics if you want to build intuition.)

So if LLMs just predict next words, how do they actually do useful things in the world? In 2023, OpenAI released tool calling, which extends this same prediction mechanism. The model still predicts next words, but instead of predicting words that just get output to you, it can predict words that trigger an action.

Here's the classic example: you ask "What's the weather today in Milwaukee?" A baseline LLM has no access to real-time information. It will hallucinate an answer - confidently give you something that sounds plausible but isn't grounded in reality.

What would you actually want a computer to do? Look it up somewhere. And that's exactly what tool calling enables.

You can give the model a tool - a piece of code that takes a city name and returns the actual weather. When you ask about the weather, the model doesn't generate a made-up answer. Instead, it outputs something like "call the get_weather tool with the city Milwaukee." At that point, the model stops generating text and executes the tool. That tool is just regular code - Python, for example - that calls a weather API and returns real data.

The model gets the result back and uses that actual information to answer your question.

This matters because that tool code is deterministic and testable. You can build a tool you know works reliably, let the LLM have access to it, and the LLM figures out when to call it. The model handles the intelligence of knowing when to use the tool - the tool itself just needs to work.

## You're Already Using Tool Calling

When you use ChatGPT today, you're not just using a large language model. ChatGPT is an application - a harness - that uses a large language model. Under the covers, it's calling different tools constantly: web search, code execution, image generation, file analysis. You don't see the tool calls, but they're happening.

This same capability is available to you. Whether you're building AI into a product or just automating a workflow for yourself, you can define tools and give them to an LLM. The model figures out when to use them.

## A Real Example: Document Generation

I'm working on a document generation project that makes this concrete. I have a set of documents with tables of quantitative data, written sections, and a mix of structured and unstructured content. These documents are also different from each other, not uniform in structure.

The naive approach would be to dump all that text into an LLM and say "figure this out." But for specialized documents with nuanced structure, you can do better.

I built Python code that knows about these specific documents. Not AI - just straight code I could have written years ago before any of this new wave of AI existed. This code understands the document structure and can extract specific information reliably.

Then I encapsulated that code in a Python method and registered it as a tool available to the LLM. I described to the model: here's a tool you have, this is how it works, this is when you should use it.

Now when I ask the LLM a question about these documents, it looks at the tools available and figures out whether to use my custom tool for this specific problem. If it decides to use it, it calls the tool, gets reliable results from my deterministic code, and then uses that information to answer my question.

You get the best of both: the LLM's intelligence and the tool's reliability.

The result: I can ask questions about these documents and get reliable, structured answers - something that would have been tedious manual work before, and that a naive LLM approach would get wrong half the time.

## Go One Level Deeper

Tool calling is one of many building blocks that have emerged in the last couple years - structured outputs, chain-of-thought prompting, prompt chaining, agentic workflows, to name a few. They're capabilities that let you build AI systems today that solve more complicated problems, more reliably, than what was possible even 12 months ago.

When you hear "AI hallucinates" or "it's just not accurate enough," that's often true for naive approaches. But these building blocks help. You can have parts of your system that must be 100% reliable handled by traditional code, while still leveraging AI for the parts that benefit from intelligence and flexibility.

Just knowing what the building blocks are, how they fit together, and when to use each one goes a long way. You don't need to master all of them. But if you can look at a problem and recognize that it's a good fit for tool calling, or structured outputs, or prompt chaining - that's valuable. You can be the person who figures out what's actually possible.

I think a lot of people are overly intimidated by going a level deeper on AI. But the concepts are actually quite understandable. Once you get tool calling, there are other building blocks that work similarly - and you'll start to see problems where you think, "that building block could help here." We're still early in getting people and organizations to build this knowledge. You could be one of those people with a little bit of time, curiosity, and effort. I hope this encourages you to dig in.
