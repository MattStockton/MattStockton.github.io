---
title: "Karpathy's Practical LLM Insights"
excerpt: "I distilled two hours of practical wisdom from Andrej Karpathy on using large language models effectively — real tools, clear explanations, and valuable tips you can apply immediately."
---

I recently watched [Andrej Karpathy's two-hour talk](https://www.youtube.com/watch?v=EWvNQjAaOHw) on how he uses large language models in practical, everyday situations. My notes here reflect points I personally found valuable, but they're not comprehensive. I'm sure others watching will discover additional insights. I highly recommend viewing the full video, as it contains many more valuable discussions and examples.

Three key aspects stood out clearly:

1. **Real-World Examples**: Karpathy didn't merely describe theory; he provided concrete examples of tools and workflows he regularly uses.

2. **Clear and Approachable**: He explained complex concepts clearly enough for newcomers while still offering depth beneficial for experienced users.

3. **Highly Practical**: Each segment was directly applicable, filled with useful, actionable information.

## Tokenization

Karpathy demonstrated [tiktokenizer](https://tiktokenizer.vercel.app/), an interactive website that lets you explore exactly how different models tokenize text. You can clearly visualize specific tokens, including special tokens marking message boundaries. It provides clarity on how tokenization actually works.

## Managing Context Windows

He advised starting fresh chats when changing topics. Although we now have models capable of much longer context windows—which are fantastic—you still need to be selective and intentional about what you include. Keeping context precise maintains accuracy and responsiveness.

## Pre-training and Knowledge Cutoff

Karpathy explained pre-training as teaching models to predict subsequent tokens using extensive internet data. Each model has a "knowledge cutoff" date, after which it hasn't been trained on new information. If you're relying on these models for factual information without external tools, awareness of their knowledge cutoff date is crucial.

## How External Tools Are Activated

Karpathy described how large language models activate external tools (like internet search, calculators, and data analysis tools) using special tokens. This was particularly interesting because I hadn't fully considered it from a token-generation perspective. The model generates a special token signaling the application to pause token generation, perform an external action, and return the result into the context.

## Understanding Model Limitations and Hallucinations

Different models have different built-in tools, making it essential to understand their capabilities. Karpathy provided a compelling demo comparing models performing multiplication problems—highlighting Grok3, which lacks a Python interpreter and thus produces incorrect calculations. This demonstration clearly showed how crucial it is to match tasks to a model's available tools.

## Expanding Context with External Documents

Karpathy specifically demonstrated how he uses Claude for reading books or lengthy documents. He uploads entire chapters and interacts by asking specific questions, enabling rapid comprehension of complex or unfamiliar material.

## Training Models to Use Tools with Reinforcement Learning

Models learn effective tool usage through reinforcement learning, where human reviewers guide the model's behavior. Karpathy explained reinforcement learning clearly, emphasizing how human feedback significantly enhances a model’s decision-making around external tool use.

## Generating Mermaid Diagrams from Descriptions

Karpathy highlighted how effectively models generate Mermaid diagrams from simple verbal descriptions. Mermaid is a specialized diagramming language where you describe diagrams using plain text. It was valuable to discover how accurately and quickly these models can convert textual descriptions into clear visual diagrams, useful for representing software architectures and processes.

## Productivity Through Voice Interaction

Karpathy extensively uses voice interactions via SuperWhisper, stating about 80% of his interactions are voice-based. Voice interaction has similarly become my primary method of working with these models—speaking commands is intuitive and boosts productivity significantly.

## Differences in Voice Interaction Modes

Karpathy highlighted an important distinction in ChatGPT voice interactions: ChatGPT's advanced voice mode generates audio-specific tokens rather than standard text tokens. This fundamentally changes the interaction experience and affects how the model responds.

## Multimodal Capabilities

Karpathy demonstrated using ChatGPT to interact directly with live video inputs. He showed how you can point your camera at real-world objects and directly query the model about them. This interaction mode is unique and underutilized, offering substantial practical potential.

## Memory Management in ChatGPT

Karpathy discussed ChatGPT’s memory management, clearly explaining that users can explicitly add, edit, or delete memory entries to preserve context over longer interactions. Although he didn't demo this directly, his explanation highlighted its potential value.

## Specialized Custom GPTs

Karpathy shared a practical example of creating a custom GPT tailored for Korean translation. By using few-shot prompting—providing high-quality examples—he significantly improved its accuracy. This demonstrated the broad applicability of custom GPTs for specialized tasks.

## Recommended Tools and Resources

Throughout his talk, Karpathy mentioned valuable resources:

- [Claude Artifacts Showcase](https://claudeartifacts.com/): Real-world examples of Claude.
- [SuperWhisper](http://superwhisper.com/): Effective voice-interaction tool.
- [Excalidraw](https://excalidraw.com/): Karpathy didn't explicitly discuss this, but he used it throughout the talk to visually present content. It's an intuitive tool I discovered and plan to explore further.
- [NotebookLM](https://notebooklm.google.com): Useful for creating personalized podcasts and tailored content.

## Final Thoughts

Karpathy’s talk provided valuable insights into effectively using large language models. While these notes highlight points I found particularly interesting, the video itself contains even more useful information and demonstrations. To fully appreciate the depth and breadth of Karpathy’s insights, I strongly recommend watching the full talk.
