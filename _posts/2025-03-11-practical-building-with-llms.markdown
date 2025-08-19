---
layout: single
title: "Practical Takeaways on Building with LLMs from John Berryman"
excerpt: "Success with LLMs isn't about picking the right API  it's about structuring problems in a way that works. In this podcast recap, I break down John Berryman's insights on better prompts, structured workflows, and human-AI collaboration that lead to real results."
category: "Building with LLMs"
tags: ["john-berryman", "practical-tips", "prompting", "workflows", "podcast-recap"]
---

Most people approach large language models by picking tools first. But the real challenge isn’t which API you call, it’s how you frame the problem. I recently listened to an episode of [*How AI Is Built*](https://share.transistor.fm/s/7eb9804c), a podcast hosted by [Nicolay Gerold](https://www.linkedin.com/in/nicolay-gerold/) that consistently delivers deep yet approachable technical content. This episode featured [John Berryman](https://www.linkedin.com/in/john-berryman-864b1713/), who shared some of the most useful, real-world advice I’ve heard on working with LLMs. No AI hype, just practical insights on what actually works. One of the key insights Berryman shared was about how to frame prompts in a way that models understand more reliably.

## The Little Red Riding Hood Principle

He calls it the *Little Red Riding Hood* principle: having your prompts stay on the path of what the model was trained on. That means your prompts will work better if they align with the structures and formats present in the training data. Structuring input in a familiar way improves results. A simple example is using markdown to delineate sections of a prompt if the model has been trained on markdown. In more specialized domains, like medical data, understanding how that data was presented in training can guide prompt design. Adopting patterns the model has already learned makes it easier for it to generate coherent and accurate responses.

That said, as models mature, this technique may become less necessary. The impact of aligning prompts with training data may diminish over time, but it remains a useful mental model. It forces you to think critically about how you structure prompts, which is always beneficial when building effective LLM applications.

## Structuring Inputs: Prioritizing Information

Longer context windows give more flexibility in what can be included in a prompt, but that does not mean everything should be thrown in. Having a mental model for what is truly critical and what is not helps keep prompts effective.

Instead of treating all data equally, it is useful to develop a system for categorizing input information by importance. Some data is essential for the model to generate useful responses, while other data may provide supporting context or be extraneous. Overloading a model with too much information can dilute its focus, making responses less precise.

A structured approach to input selection helps ensure the model is given what it needs without unnecessary distractions. Thinking through what is most relevant for a given use case leads to better results and a more systematic way of working with LLMs.

## Experiment First, Then Evaluate

Berryman emphasized the importance of just getting started with prompt iteration. The term *vibe testing* can have some slight negative connotations, but in this context, it simply means iterating quickly on different prompting approaches and analyzing outputs to build intuition before moving to structured evaluation. Berryman is completely right that you need to start prompting for a specific problem and develop an understanding of how things are working. You do not need to overcomplicate it. Just find a quick way to prototype and test different approaches.

However, once you gain some understanding of how the model behaves and start getting stable results, it is critical to move toward structured evaluations. You cannot just vibe test forever. Transitioning to a systematic way of assessing and improving performance is necessary. It is an important part of the process, but it must lead to structure.

## Breaking Problems Into Steps

A critical part of building with LLMs—or solving any complex problem—is breaking it into smaller, manageable components. Many problems can be represented as a graph, where each node has:

- A clear **input**
- A well-defined **output**
- A way to validate that output
- A structured way to connect steps together

Since LLMs take unstructured input and produce unstructured output, it is easy to overlook the need to break problems into smaller steps. The flexibility of these models allows them to return something useful even when a problem is loosely defined, but without structure, the results can be volatile and inconsistent. Defining clear steps ensures stability, makes debugging easier, and allows for controlled iteration.

Berryman shared an interesting example of an application designed to help companies handle SOX compliance. Instead of trying to generate an entire compliance report in one step, the problem was broken down into smaller components, each responsible for processing a specific section of documentation. This structured approach made validation easier, improved reliability, and allowed for iterative refinement of individual steps.

Good software engineering always involves breaking problems apart, but it is especially critical for LLM applications where outputs can shift unpredictably. Applying this mindset ensures more reliable and maintainable solutions.

## Humans in the Loop

Berryman talked about how people intersect with the work that LLM applications are doing and how critical it is to design for this interaction. The user experience of these models is where some of the most interesting breakthroughs can happen. It is not just about automation, but about understanding how people and models collaborate effectively.

Designing applications with a clear vision of how users will interact with the model is essential. The model does not have to do everything. It just needs to fit seamlessly into the workflow of the people using it. Being intentional about how humans and models work together leads to more effective and practical solutions. Thoughtful UX design in LLM applications is not an afterthought; it is a core part of building something that actually works.

## Tools Do Not Matter—Just Start

This has been my mindset for a long time. The most important thing is to get started. Do not overthink which tool, framework, or system you need. Just begin. The best way to make progress is to take one of the foundation models, open a notebook, and experiment with the specific problem you are trying to solve.

Once you gain traction and are considering moving to a production system, observability, logging, and evaluation become essential. Having a structured way to track prompts, completions, and performance is critical at that stage. But if you are just starting out, do not let these concerns slow you down. The first step is to dive in and start working with the model. Everything else can come later.

## Final Thoughts

This episode had a lot of useful, no-nonsense advice. The big takeaways—structuring input effectively, breaking problems into smaller steps, designing better human interactions, and iterating quickly—are just good engineering. They happen to be especially important for AI applications, where it's easy to get vague, but they apply to any complex system.

Berryman’s approach reinforced something I’ve always believed: the best way to make progress is to stop overthinking and start experimenting. LLMs will give you something back no matter how you structure the problem, but the people who take the time to break things down, design thoughtful workflows, and refine their approach will get the best results.

These ideas have shaped how I work with LLMs, and they’ve made a real difference in my ability to get better results. If you haven’t started yet, open a notebook and start testing things. You’ll learn more by doing than by thinking about it too much.
