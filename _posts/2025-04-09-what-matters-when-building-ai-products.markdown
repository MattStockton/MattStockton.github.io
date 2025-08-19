---
layout: single
title: "What Actually Matters When You're Building AI Products"
excerpt: "A few takeaways from Hamel Husain's guide to improving AI products — from avoiding the tools-first trap to empowering domain experts and focusing on fast, iterative learning. One of the most useful pieces I've read on building with LLMs."
featured: true
category: "Building with LLMs"
tags: ["product-development", "evaluation", "ai-systems", "best-practices"]
---

[Hamel Husain](https://hamel.dev/) wrote a piece that’s too good to summarize. But I’m going to anyway.

It’s called [*A Field Guide to Rapidly Improving AI Products*](https://hamel.dev/blog/posts/field-guide/), and it’s one of the best things I’ve read on building with LLMs. If you’re even a little bit serious about working in this space, you should just go read it. Don’t settle for my notes — the original is better, and sharper, and more complete.

This post is mostly for myself. I use writing as a way to remember the things I want to revisit. But I also hope it nudges a few people toward [Hamel’s work](https://hamel.dev). His writing makes this space more approachable, more rigorous, and more grounded in solving actual problems.

Here’s what stuck with me.


## Don’t start with tools

This has always been true in software: teams over-engineer before they understand the actual problem. But in AI, the failure mode is even worse because the tool landscape changes daily. There’s always another framework or feature to chase. It creates the illusion of progress.

Hamel tells a story where he pauses a team walking through their system diagram and just asks, “How are you measuring if this works?” Nobody has an answer.

It’s a great reminder: skip the tech stack for now. Start with the job to be done. Look at real examples. Understand what’s failing. That’s where the leverage is.

**Write some unit tests instead of evaluating new RAG frameworks.**


## Custom data viewers are worth building now

One of the most practical points in the post: if you want to improve your system, you need a way to *see* what it’s actually doing.

Hamel makes the case for building a custom data viewer — something that lets your team inspect and annotate the raw outputs of your LLM system. That might be a conversation, a generated summary, a draft report, or something else entirely. The specifics vary, but the need is the same: full context, minimal friction, fast feedback.

A few years ago, I would’ve said this was too much effort. But now? With tools like Cursor and decent AI code generation, it’s often easier to build exactly what you need than to force your use case into someone else’s UI.

And the payoff is real. These kinds of viewers help teams find failure modes, track quality, and move fast. If you want to iterate quickly, this is where you start.

I haven’t leaned into this yet myself — but the idea is compelling enough that I’m planning to try it in a few future use cases.


## “Prompts are just English” — so stop gatekeeping

This line from the post says a lot with very few words. Too often, teams treat prompt engineering as something only engineers can do. But in most cases, the people who know the domain best are also the ones who know what the model *should* say.

Instead of giving them direct control, we create unnecessary friction: a domain expert explains what they want, an engineer translates that into a prompt, the result doesn’t work, and everyone’s frustrated.

What resonated most here is the idea of building admin tools that allow domain experts to directly test, tweak, and own the prompts. Letting them work in-context — within a sandboxed version of the actual product — just makes sense. It’s more efficient, and it puts the right people in control of what the system is actually saying.


## Binary evaluation creates better clarity

If you’re evaluating LLM outputs, don’t use a 5-point scale. Ask yourself: did this do what we needed or not?

Numeric scores sound precise, but they just introduce a layer of indirection. You still have to interpret them — “is a 3.5 good enough?” — which defeats the purpose. Binary evaluation forces a clear decision: pass or fail. Then you pair that with a short critique to explain why.

The deeper value is in what this unlocks. It forces detailed, nuanced conversations — led by domain experts — about why something works or doesn’t. That reflection builds stronger instincts. It surfaces edge cases. It tightens the feedback loop into prompt development and testing. And over time, it produces better products.


## Plan experiments, not features

AI development doesn’t follow the same rules as traditional software. You don’t always know what’s possible. So planning to ship a specific feature on a specific date doesn’t work — and trying to force it will burn time and trust.

Hamel suggests a different framing: the *capability funnel*. You measure progress by how far your system moves down this funnel:

1. Can the model respond at all?  
2. Can it respond with valid structure or syntax?  
3. Can it return something relevant?  
4. Can it match user intent?  
5. Can it fully solve the problem?

That’s a much more useful way to scope AI work. Instead of pretending you know what the end result will be, you define what success might look like — and you set up fast, focused experiments to learn what’s feasible.

This is about creating a learning loop. Not just iterating quickly, but validating ideas quickly. You want to find out where things break, where they’re close, and where to push. That’s how you get better systems — and more informed teams.


## Why this post is worth returning to

What I liked most about Hamel’s piece is how much it focuses on the real work — not the frameworks, not the hype, but the small systems that help you learn faster, reduce ambiguity, and involve the right people.

There are at least five other ideas in the article that stood out to me — but I didn’t want to pile on more summary here. The point of this post isn’t to cover everything. It’s to nudge you to go read the full thing.

If you’re building with LLMs, read it. If you’ve read it already, read it again. I think you’ll be glad you did.
