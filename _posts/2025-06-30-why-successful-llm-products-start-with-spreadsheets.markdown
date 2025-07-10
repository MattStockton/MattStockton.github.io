---
layout: single
title: "Why Successful LLM Products Start with Spreadsheets"
excerpt: "Philip Carter's process on Vanishing Gradients shows the value-added work most people skip - actually looking at your data and fixing what's broken."
---

[Philip Carter](https://www.linkedin.com/in/phillip-carter-4714a135/) from Honeycomb walked through his error analysis process on Vanishing Gradients, Hugo Bowne-Anderson's excellent podcast that consistently delivers practical insights for data practitioners. In [episode 51](https://vanishinggradients.fireside.fm/51), Carter's description is detailed and approachable - he tells you exactly what he did and how you can use LLM tools to help.

Systematic, manual review of your LLM outputs is what makes the difference between working products and demos. Carter's honest about what this requires - lots of time staring at spreadsheets, manually labeling data, and iterating on what works. It's not glamorous, but it's where the real progress happens.

This matters whether you're already building LLM features or evaluating whether to start. Most teams underestimate the evaluation work required to make these features reliable enough for real users.

## The Unglamorous Work That Actually Matters

Carter's process is about creating a flywheel where you look at data, find what's broken, fix it, then repeat. 

Many people building LLM features underemphasize this work. They focus more on prompt tweaking or architecture optimization. But the real leverage is getting out of your code and into a spreadsheet, asking: does this actually solve the problem I'm trying to solve? And are the results actually good?

Carter puts it simply: "I hate to say that like there's no magic to this process it's just very laborious and sometimes you just want to walk away and not stare at that spreadsheet for forever but it's really necessary I think."

## The Process

Carter worked with [Hamel Husain](https://hamel.dev/) on this approach. Husain appeared on an [earlier Vanishing Gradients episode](https://vanishinggradients.fireside.fm/45) where he detailed similar principles for error analysis that I've [written about before](/2025/02/22/error-analysis-and-llms.html). The process is straightforward - you don't need sophisticated tooling or advanced ML knowledge.

Start with a prototype and do "vibe checks" - Carter notes these are "actually very important. It's your first gauge for if something is actually feasible to do." Ship to users and collect real usage data. Export everything to CSV - user inputs, what you sent to the model, what the model returned, and any errors that happened.

Load the data into Google Sheets and start the manual review process. Go through samples and add your judgment in a separate column: good, bad, in-between. This requires domain expertise - you need to actually know what good outputs look like for your specific use case.

Once you have enough human-labeled examples, create an "LLM as judge" using your labeled data as few-shot examples. Then generate synthetic inputs that mimic real user patterns and run them through your actual system to get real outputs. Use your LLM judge to evaluate these synthetic input-output pairs, creating a much larger dataset of judged examples.

Take random samples of data that your LLM judge has evaluated. Judge those same examples yourself independently. Compare your judgments with the LLM's judgments and look for patterns in the disagreements.

Use those disagreement patterns to refine your judge. Update the judge prompt based on what you learn. Repeat this process and you start to figure out how well your LLM judge actually aligns with your human judgments.

## Why Spreadsheets Beat Dashboards

You have to get out of your tools and code and look at a spreadsheet. It doesn't take much work to get started, but it requires accepting that the most important work might be the least exciting work.

Instead of evaluating the latest model or optimizing your vector database, you're manually labeling outputs in Google Sheets. This forces you to focus on real problems instead of busy work.

## Scaling Human Judgment

The balance Carter strikes between doing manual labeling to establish human ground truth and then quickly using that labeled data within LLMs to improve both synthetic data creation and the LLM judge itself is smart.

You start with human expertise - someone who actually knows what good outputs look like in your domain. Then you use that expertise to train an LLM judge that can evaluate outputs at scale.

Instead of assuming your LLM judge is working correctly, you continuously test it against human judgment and refine it based on disagreements. The process scales human expertise rather than replacing it.

## From Prototype to Production

The difference between a demo and a production feature comes down to reliability. Carter's process creates that reliability through systematic evaluation rather than hoping for the best.

At Honeycomb, this work paid off. Their natural language feature became "the primary way that new users come into our product." That level of trust - where you're comfortable putting an LLM feature in your onboarding flow - only happens when you've done the unglamorous work of actually understanding what your system does.

Most teams skip this step. They define success as "the feature works sometimes" instead of "the feature works predictably." Carter's approach forces you to define what good outputs actually look like, then build systems to maintain that standard consistently.

The alternative is building monitoring dashboards and evaluation frameworks without first understanding your data. You end up measuring the wrong things because you never established what the right things were.

## Getting Started

Export a week's worth of your LLM outputs to a spreadsheet. Pick 50 random examples. For each one, ask yourself: is this actually good? Add a column with your honest judgment.

Look for patterns. Maybe 30% of outputs are too verbose. Maybe the model consistently fails on certain types of inputs. Maybe you realize your prompt is optimizing for the wrong thing entirely.

Fix the most obvious problems first. Then repeat the process. Each cycle teaches you something new about what your system actually does versus what you think it does.

Carter's full alignment process is powerful, but you can get value immediately just by looking. The discipline of actually reviewing your outputs - rather than assuming they're working - is what turns prototypes into reliable features.