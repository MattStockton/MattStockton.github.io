---
layout: single
title: "Six Insights from Andrew Ng on Building Faster with AI"
excerpt: "Key takeaways from Andrew Ng's Y Combinator talk on adapting to the rapidly evolving AI development landscape."
category: "AI Strategy & Leadership"
tags: ["andrew-ng", "ai-strategy", "startup-advice", "product-development", "y-combinator"]
---

[Andrew Ng](https://www.linkedin.com/in/andrewyng/) is one of the best technical teachers out there - any content he puts out is guaranteed to be high quality. His recent YCombinator AI Startup School talk ["Building Faster with AI"](https://www.youtube.com/watch?v=RNJCfif1dPY) was valuable because it condensed practical, applicable advice into 45 minutes. In a space where best practices change every few months, having someone with Ng's experience distill what matters is useful.

The full talk is worth your time - Here are key insights that stood out to me.

## Everyone Should Learn to Code (Yes, Really)

Ng argues that everyone should learn to code regardless of job role. He calls this a "controversial opinion" but believes the ability to tell a computer exactly what you want is becoming one of the most important skills of the future. Most everyone on his team uses some aspect of coding for their job and performs better because of it.

There's growing debate about whether learning to code is still worthwhile, as AI coding agents become more capable. I think his advice is right because understanding how to code *plus* knowing how to use these tools gives you a large edge - almost like a superpower. The way we learn classical software engineering will change with these tools - I don't think it's essential to study computer science traditionally - but there's large benefit to learning the fundamentals, which is more approachable with these tools. Even with generative AI's capabilities, it's still useful to learn the fundamentals.

## Bigger Architecture Decisions Are Becoming Reversible

Ng applies Jeff Bezos's concept of "two-way doors" (reversible decisions) versus "one-way doors" (costly to reverse) to software development. Traditionally, choosing your software architecture or tech stack was a one-way door - you made the decision and lived with it. Now, with AI dramatically lowering the cost of software engineering, his teams are more willing to experiment with different approaches and backtrack to start over when necessary.

His point resonates with me. It's less expensive in time to try different approaches and build using different libraries and tech stacks. It's easy to get started with a project using AI coding tools. Sunk costs for architecture decisions are shrinking. I agree with his take that it's more approachable to try different things and then choose the one that best aligns with what you're building after you get some hands-on experience - which in the past was less true.

There's probably a slippery slope here though - you don't want to use this as a crutch for not building incrementally, which is always a good idea in software, but it does change the equation a bit. Learning through trying and throwing away more things is a much more viable path now.

## How AI Tools Work and Which Ones Work Best Changes Rapidly

Ng emphasizes that being even half a generation behind on the latest AI tools makes a significant difference. This is particularly evident in the coding tools space. What matters about the tools and how they work to get the most value changes frequently.

Six months ago, many tools were using a retrieval augmented generation (RAG) approach to embed your codebase in prompt context. Now it's clearer that agentic AI agents that can loop with simple tools like grep, file editing, and bash commands work much better. The Claude Code paradigm is the current clear winner to me - where you can give high-level instructions and the agent breaks them down into specific tasks with tool usage - different than what these tools looked like six months ago with RAG, which was different than what they looked like a few years back when GitHub Copilot was the predominant tool offering basic completions in an IDE. 

I don't think you want to get bogged down experimenting with every tool - because that could just become all you do without building anything of value. But the equation has changed. You need to be on the leading edge of what's available and dedicate time towards experimentation with these tools. You don't want to be building with what was the right approach 6 months ago, but is not the right approach now.

## Wrong Technical Decisions Are Exponentially Costly

This is somewhat counter to the experimentation argument above, but what resonated with me is that you have to know enough about the AI space - and choose the right tools and approaches for the problem you're solving. If you choose the wrong tool or wrong fundamental approach to solve a problem, you could end up moving much slower than what is possible.

The correct approach to solving a problem is fluid in the AI space, so you need to be aware of that fluidity and understand the options. Ng's point is that building up general leading-edge knowledge of the space is important. Pressure testing your thinking about how you're solving things, given that there are all these new building blocks, is critical. Building a network of skilled people who are also on the leading edge of this will also help you figure this out - Twitter is a fantastic place to do so as long as you're following the right people

We're in this interesting spot where we have this amazing toolbox of things that can help us build new things -- but we're still learning what tools to use when, and the contents of the toolbox also changes constantly. 

## AI as Lego Building Blocks

This is where I spend the most time thinking. Ng argues you can think of the foundational components in the AI space as building blocks - prompting, fine-tuning, agentic behaviors, tool usage, reasoning models, multimodal capabilities - are all building blocks. There are many terms, but fundamentally many of them are different "LEGOs" you can combine in interesting ways.

Ng's point is that as you figure out and experiment with how to combine these things, there's a combinatorial output - there's so much new stuff to be built. One thing I've been thinking about recently is that Deep Research via API combined with MCP servers gives you an interesting capability to leverage extremely capable models with proprietary data programmatically. Another example: combining reasoning models with multimodal capabilities lets you build applications that can analyze documents, images, and data together to draw conclusions that weren't possible before.

This seems like a huge opportunity for building interesting things - you can now build applications that combine the research capabilities of frontier models with your own data sources automatically.

The more building blocks you understand and can utilize, the more complex and innovative applications you can build. As Ng puts it, the number of things you can combine them into "grows kind of combinatorily or grows exponentially."

In the past I've been weary of the "solution in search of a problem" issue, where you apply flashy technology in ways that people just don't need, and you don't end up solving real problems. I am less skeptical of it now, and actually like the thought exercise of "What's newly possible with these tools?" - it's because so many people truly don't realize *how capable* these building blocks actually are - so if you combine them in interesting ways (even without a deep understanding of a specific domain), you may just stumble on something that actually is needed or useful to people.

## The Product-to-Engineer Ratio Debate

Ng highlights that product management work is increasingly becoming the bottleneck, leading his teams to propose having more PMs than engineers for a project - "twice as many PMs as engineers" - which was surprising to him.

I don't believe thinking about these ratios or how to change them is the most valuable way to think about it. I think it's about having people with agency and curiosity who leverage these tools to amplify their skills across domains. The people that are product-curious or product-focused engineers are more empowered to do both things now because their productivity can increase on the coding side with AI coding tools, and their access to thought partners on the product side has also been amplified through these tools.

I think the companies that figure this out and blur the lines are the ones that will win. The line between product manager and engineer will become blurry, and success will come from not differentiating between these roles and creating handoff periods.

I think Ng is right that product sense and product taste matters a lot in this environment - I just think high-agency Engineers with curiousity are able to fill this gap as well (and so can high-agency Product Managers who learn a thing or two about building)

## Tying It Together

The common thread through all of these insights is that the rules are changing faster than most people realize. Learning to code gives you superpowers. Architecture decisions that used to lock you in for years can now be experiments. Tool paradigms shift every few months. The blocks available for buildiung amazing products are growing exponentially.

The teams and individuals who embrace this fluidity and build systems for continuous learning will have significant advantages. Those who wait for things to stabilize will be perpetually behind.

This week: pick one AI coding tool to try, question one technical decision you thought was permanent, or identify one building block you don't understand yet. The landscape won't slow down for you.

Go [watch the full talk](https://www.youtube.com/watch?v=RNJCfif1dPY). You'll come away with actionable insights regardless of your role.