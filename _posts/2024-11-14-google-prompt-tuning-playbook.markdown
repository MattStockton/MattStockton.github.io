---
layout: single
title: "Notes From Google's Prompt Tuning Playbook"
---

[Varun Godbole](https://www.linkedin.com/in/godbolevarun/) and his team at Google recently released an excellent [prompt tuning playbook](https://github.com/varungodbole/prompt-tuning-playbook), packed with practical advice. Varun, a core contributor to Gemini, has generously shared this knowledge, and it’s worth a full read. I’ve summarized my takeaways below. If you’re aiming to get better at using LLMs, resources like this are invaluable — study them, experiment, and then apply what you learn.

### Understanding "Universes" of Information

LLMs are trained on a massive corpus of text from the internet, which encompasses many different "universes" or domains of information. For example, “All writing about basketball players” is a universe, as is “All writing about repairing cars.” Prompts that guide the model to recognize **which universe** to consider will produce better outputs.

> “When you give the model a fixed context window (i.e. prefix), it will try to infer from that prefix what universe it is in, and it will then behave in accordance with the rules, conventions, and facts of that universe. If you provide a prompt with very strong signals about context, it will be easier for the LLM to recognize the script.”

### The Role of Human-Curated Datasets

Models are post-trained using human-curated datasets, where real people have created input-output pairs by manually writing the responses. This reinforces the importance of writing prompts that a domain-knowledgeable person could understand and answer correctly.

> “When you're writing system instructions and prompts, you are writing them for something like the aggregated spirit of the post-training team’s rater pool, seeded by the aggregated spirit of the pre-training corpus. If we write instructions that the average rater (within that specific domain) is likely able to understand, comprehend and faithfully follow, the model is more likely to follow our instructions.”

### Core Principles for Writing Effective Prompts

The playbook offers essential principles for crafting prompts:

- Make prompts **clear, legible, concise, and explicit**.
- Avoid **contradictions** within prompts.
- Avoid too many instructions in a single prompt; if necessary, break it into a chain.
- Instruct on **what to do**, and not **what not to do** — be specific.
- Include guidance on edge cases, like any assumptions the model should make.
- **Time-box experimentation**; always searching for a "perfect" prompt can be unproductive.
- Allow the model to respond with “I don’t know” to limit inaccurate answers.

### Fewer Examples: Prioritize Zero-Shot Instructions

Interestingly, the paper recommends limiting few-shot instructions (teaching with a few examples) in favor of zero-shot instructions (tasking the model without examples). When using few-shot though, they suggest incorporating examples directly within instructions instead of using traditional few-shot examples.

> “Instead of full blown few-shot examples, prefer to weave in examples into the prose of our instructions. Consider the following system instruction that uses “For example” at the end of the instruction: *Always start your response to the user with something passive aggressive. For example, start with something like “Oh that’s what you want? I’m not saying you’re wrong. But I mean, sure, if that’s what you really want.” But keep it fresh and use a different start to each response, based on what’s in the user’s message.”*

### Systematic Approach to Prompt Development

The playbook outlines an organized approach for developing effective prompts:

1. Start with diverse input examples for your specific problem. For a summarization task, these might be texts you want to summarize.
2. Write the simplest prompt you can imagine working for all examples.
3. Test this prompt on your first example.
4. Adjust the prompt based on the model's output for this first example, **overfitting to it** if needed.
5. Move to the next example, refine the prompt further, and **generalize** as necessary.
6. Continue this process for all examples.
7. Clean up the final prompt - add structure, remove unnecessary text.
8. Re-run the final prompt on all examples to confirm consistency and quality.

### When to Use LLMs: The HMEC Principle

One of my favorite quotes from the playbook was about when LLMs are most useful:

> “LLMs are best where the answer is hard to make, but is easy to check.”

This insight, attributed to [Chris Gorgolewski](https://www.linkedin.com/pulse/hmec-principle-finding-sweet-spot-generative-ai-gorgolewski-ph-d--3zl5e/), points to the sweet spot for LLMs: tasks where generating the answer is challenging, but validating it is straightforward. 

---

If you're serious about improving your prompt-tuning skills, this playbook is a goldmine of techniques and ideas. From understanding the nuances of model training to crafting precise prompts, there’s a lot to learn and apply.