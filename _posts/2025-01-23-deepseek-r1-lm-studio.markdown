---
layout: single
title: "DeepSeek R1: A Reasoning Model with Thinking Tokens"
---

I experimented with [**DeepSeek R1**](https://www.deepseek.com/), an LLM that uses chain-of-thought reasoning. For those interested, I recorded a six-minute demo, showing how the model works and why I find it so fascinating. If you’d prefer a quick summary, below are my key takeaways. **TLDR:** You can learn a lot about the problem you're trying to solve from the reasoning tokens themselves, not just the final model output.

<iframe width="560" height="315" src="https://www.youtube.com/embed/VtnHfU0z_Xk?si=lxiqqkLQSIIV8qGZ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<br/>

DeepSeek R1 is similar to OpenAI’s reasoning models (e.g. o1), but it has a major difference: its reasoning process is fully transparent. While OpenAI’s models use chain-of-thought reasoning behind the scenes, DeepSeek R1 exposes this process through **thinking tokens** — intermediate reasoning steps that show how the model approaches a problem before generating a final answer.

Chain-of-thought reasoning is when the model generates a sequence of intermediate reasoning steps to arrive at its final conclusion. These steps mimic how humans break down complex problems into smaller, more manageable parts. This technique improves the model’s performance on tasks requiring logic, reasoning, or multi-step problem solving. What makes DeepSeek R1 special is that these intermediate steps are visible to the user. You can watch the model think through a problem in real time. It’s like observing someone’s internal thought process or background thread of reasoning.

What stood out to me while testing DeepSeek R1 was how much value you might get from reading these thinking tokens. They might spark new ideas or perspectives you didn't consider about the problem you're solving. Seeing this process can provide clarity and inspiration that the final answer alone might not deliver. Here's a screenshot of an example I tried in the video:

<img src="/docs/assets/images/deepseek-r1/1.png" width="800px" height="800px"/>

I tested a distilled version of DeepSeek R1 on my MacBook M3 Pro (18GB RAM) using [**LMStudio**](https://lmstudio.ai/), a tool for running local models. It performed well, handling tasks smoothly with no noticeable issues. Running models locally is becoming much more achievable, and this setup demonstrates how far we’ve come. For most problems, I still think using the API is more practical, but running R1 locally is a great way to experiment. This approach can also run entirely offline, meaning you could use it on an airplane or in other situations without internet access.

DeepSeek R1 highlights how accessible and transparent AI tools are becoming. Its thinking tokens provide a unique way to engage with reasoning models and explore how they solve problems.