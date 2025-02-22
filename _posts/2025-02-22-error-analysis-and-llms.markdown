---
title: "The Most Overlooked Step in Building Reliable AI Systems"
layout: single
---

One of the biggest mistakes people make when working with AI systems is not looking closely enough at their data. They assume the system is working because it’s generating outputs, and they move on. But if you’re not actively reviewing what the model is doing — step by step, error by error — you risk missing fundamental problems. That was one of the key takeaways from [Hamel Husain](https://hamel.dev/)’s recent discussion on *Vanishing Gradients* ([episode link](https://vanishinggradients.fireside.fm/45)), where he emphasized the importance of error analysis. This post weaves in some of the key ideas from that conversation along with my own thoughts on these issues — why looking at your data matters, how to think about correctness, and why simple evaluation strategies can make or break an AI system. The best AI practitioners know that this process is where real progress happens.  

## Looking at Your Data is More Important Than Any Tool  

There’s a tendency in AI to overcomplicate things. People assume they need sophisticated monitoring dashboards, automated evaluation frameworks, or specialized tools before they can even begin debugging. But in reality, you don’t need anything fancy to get started. Just looking at the outputs — whether in a spreadsheet, a text file, or even a Word doc — and thinking critically about them is often the most valuable step. The key isn’t the tool, it’s the habit of reviewing results, asking what makes them right or wrong, and refining your understanding of the problem.  

A lot of teams miss this step. They focus on making API calls, building model interfaces, or displaying results in an app — but they haven’t really defined what a correct output even looks like. Sometimes, you don’t realize what you should be measuring until you start manually reviewing the results. And that process of reviewing isn’t just about fixing mistakes — it forces you to clarify the actual problem you’re solving.  

## What Does “Correct” Even Mean?  

One of the trickiest things about working with AI — especially large language models — is that correctness isn’t always clear-cut. In traditional machine learning, if a classifier is underperforming, you might inspect the training data, adjust feature selection, or refine decision boundaries. But with LLMs, you’re dealing with generated text. What makes an answer "correct" is often subjective.  

There are tools that claim to measure truthfulness, succinctness, or hallucinations — but these are vague, context-dependent ideas. **Truthful to whom?** **Succinct compared to what?** You can’t just trust automated scoring metrics; you have to define correctness in a way that makes sense for your specific use case.  

This is where domain experts come in. If you’re building an AI system for finance, medicine, or law, you might not be the best judge of whether an output is useful. You need to work with people who understand the domain deeply. And beyond that, as an engineer, you need to make an effort to understand the domain yourself — because at the end of the day, the hardest problems in AI aren’t technical. They’re about whether the system is solving the right problem in a way that actually makes sense for the people using it.  

## Avoiding the Tool Trap  

Once you’ve defined correctness, the next challenge is diagnosing errors without getting lost in unnecessary tooling. There’s a balance here. If you’re working with a distributed system, function calls, or chains of prompts, you need some way to trace and visualize what’s happening at each step. But many teams over-focus on tools and dashboards when what they really need is to just start looking at their outputs.  

There’s nothing wrong with setting up tooling to help with debugging, but don’t let it become a distraction. The important part is getting direct feedback on whether your system is working as expected. Pick something simple, get the feedback loop running, and iterate.  

## Evaluations Are Not Optional  

Even after you’ve identified common errors, you need some kind of structured evaluation. Many teams still rely on manual eyeball checks — “This looks good enough, let’s ship it.” That might work in the short term, but AI systems are constantly shifting. Foundation models get updated, user behavior changes, and new edge cases emerge. If you don’t have baseline evaluations, you won’t even know when things break.  

Your evaluations don’t have to be perfect. Maybe you start with basic checks — verifying expected keywords, tracking output lengths, or running lightweight unit tests to catch obvious issues. The point is to have something automated, so that when you change a prompt or adjust retrieval logic, you can measure the impact objectively.  

Having even a simple baseline allows you to iterate with confidence. If you know how your system is performing today, you can make changes without fear of unexpected regressions. And as your system matures, you can always add more tests to refine your evaluation process. The important thing is just to start.  

## Making This More Accessible  

For people with a data science background, all of this sounds obvious. But many AI practitioners today don’t come from that background. The worst thing that can happen with new technology is when early adopters hoard knowledge instead of making it accessible.  

So the real challenge is: how do we teach structured error analysis in a way that resonates with newcomers? And how do we build tools that naturally encourage good practices instead of expecting everyone to develop them from scratch?  

This is something I’ll be thinking about a lot. The teams that take this process seriously — who view it not as a chore but as the key to building better systems — are the ones that succeed. Everyone else is just playing with demos.  
