---
layout: single
title: "Anthropic Demo for LLM Text Classification"
excerpt: "Anthropic's classification demo showed me a different way to approach text classification — structured XML prompts, retrieval-augmented examples, and clear evaluation with PromptFoo. It's practical, well-documented, and has me rethinking when to reach for an LLM over traditional ML tools."
category: "Building with LLMs"
tags: ["text-classification", "anthropic", "xml-prompts", "promptfoo", "evaluation"]
---

I’ve typically leaned on classical machine learning tools like scikit-learn and XGBoost for classification tasks. I recently found a demo notebook from Anthropic, and it made me rethink some of my assumptions. [Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook/tree/main) contains high-quality, practical notebooks for learning how to use LLMs in real applications.

This [specific demo](https://github.com/anthropics/anthropic-cookbook/blob/main/skills/classification/guide.ipynb) builds a classifier for insurance support tickets, determining whether a ticket is about billing, claims, or something else. Here’s what stood out:

### 1. Clear And Structured Prompting with XML

The notebook introduces a structured prompting technique, using XML format to define classification categories and their definitions. Structured prompts like this tend to perform better because they give the model clear instructions and a framework to follow.

### 2. Making Outputs Usable Downstream

It shows how to pre-fill the prompt output and use stop sequences to force the model to return outputs in a specific format (e.g., XML in the shape you want). This makes it easy to integrate the results into downstream software.

### 3. Including Dynamic Example Classifications In The Prompt

The demo uses a vector database to pull examples of past classifications and embed them directly in the prompt (depending on the query). This retrieval-augmented generation (RAG) technique provides the model with relevant context, improving its accuracy and making the classifications more consistent.

### 4. Asking the LLM to Think With Chain Of Thought

The demo uses a chain of thought (COT) approach, where the prompt asks the model to explain its reasoning step by step. It instructs the model to use a “scratchpad” XML element where the model lays out its thought process in the output. This improves interpretability and slightly boosts performance.

### 5. Iterating / Evaluating with PromptFoo

The notebook incorporates PromptFoo, a tool for running model evaluations and testing different setups. It evaluates various configurations like model type, temperature settings, and whether to use RAG or COT. This helps identify the best-performing approach for your use case. It's straightforward to configure and run through a bunch of different permutations.

### 6. Evaluating with a Confusion Matrix

The notebook provides code to generate a confusion matrix for each model run. This is based on demo data, but the performance is solid and easy to visualize, making it simple to spot areas for improvement.

### Why I Liked This

This demo is practical and full of useful techniques. I especially liked the structured prompts, the use of examples, and the focus on testing and evaluation. It’s straightforward to implement and gives you everything you need to build a solid baseline classifier for real-world tasks. Next time I have a classification problem, I’ll definitely consider using this approach and see how it works with a real-world problem.