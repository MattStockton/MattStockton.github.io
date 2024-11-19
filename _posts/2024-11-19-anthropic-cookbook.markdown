---
layout: single
title: "Why You Should Spend a Day with Anthropic’s Cookbook"
---

[Anthropic’s Cookbook](https://github.com/anthropics/anthropic-cookbook/tree/main) is a collection of Jupyter notebooks that teach foundational techniques for working with LLMs. These examples go beyond just using Claude - they offer reusable knowledge that applies to any model you might work with. It’s a practical, high-signal resource that can significantly improve your LLM skills.

One standout example demonstrates how to build prompts for [summarizing content with citations](https://github.com/anthropics/anthropic-cookbook/blob/main/skills/citations/guide.ipynb). The notebook focuses on two use cases: (1) a Q&A system backed by a knowledge base and (2) a method for asking questions about a large PDF document. These examples demonstrate good prompting techniques, and also show how to build applications grounded in verifiable sources - a critical component of user trust.

Why are citations important? LLMs, by design, can hallucinate information that isn’t accurate. Including citations grounds outputs in real sources, and when users can easily verify those sources, their trust in the application grows. This is a perfect example of why thoughtful user experience design - including structured outputs and transparency / lineage - is essential for building effective LLM-driven tools ([User experience is everything](/2024/11/17/my-takes-on-ai.html#user-experience-is-everything))

---

### Here’s What I Loved About This Example

- **Prompt crafting and formatting**: The example demonstrates how to structure prompts using XML tags to organize sections and includes the use of a system prompt to define the model’s behavior. These patterns are simple yet highly effective for improving prompt reliability.

- **Few-shot prompting and Chain of Thought reasoning**: The notebook shows how to guide the model with a few well-chosen examples (few-shot prompting) and how to structure prompts to encourage step-by-step reasoning (Chain of Thought). These techniques significantly enhance the quality and interpretability of outputs.

- **Response prefilling and stop sequences**: Response prefilling nudges the model to begin with specific tokens, aligning outputs with a structured format like XML or JSON. Stop sequences further ensure that the model’s output adheres to your schema by defining where it should stop generating text.

- **Structured outputs and JSON formatting**: The example illustrates how to prompt the model to generate structured JSON data directly. This reduces the need for post-processing and ensures seamless integration into applications.

- **Post-processing strategies**: Rather than expecting the LLM to do everything, the example demonstrates how to offload tasks like linking citations to post-processing steps. This approach enhances usability while keeping the model focused on generating accurate outputs.

- **Integration with external tools**: The example includes using PDF extraction libraries to preprocess unstructured input data. This makes the workflows highly applicable to real-world projects where raw data often requires preparation before it’s ready for the model.

- **Evaluation with tools like PromptFoo**: Anthropic goes a step further by showing how to evaluate prompts using tools like PromptFoo. Evaluations ensure your prompts perform reliably across different scenarios, a step that’s critical for building robust, scalable applications (read more in my [previous post on PromptFoo](/2024/09/24/testing-your-prompts-llm-evals.html)).

---

Anthropic’s Cookbook isn’t just about promoting Claude - it’s a resource that teaches foundational skills for working with LLMs. The examples provide clarity and depth, offering a great baseline that can help you when building actual applications.

If you have an hour to improve your LLM skills today, start with the Summarization with Citations notebook. Walk through the code, try out the techniques, and see how far it takes you. My advice, as always, is to just start - Anthropic’s content gives you everything you need to take that first step.