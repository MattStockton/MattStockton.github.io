---
layout: single
title: "Automating the Path from Frontier Models to Fine-Tuned Models"
excerpt: "A tweet about fine-tuning on frontier model outputs got me thinking about how much of that loop could be automated."
category: "Software Engineering"
tags: ["ai-tools", "llm", "fine-tuning", "mlops", "software-engineering"]
---

I saw a post from [Virat](https://x.com/virattt/status/2027809465789980896) at [findatasets](https://x.com/findatasets) recently about using GPT 5.2 to parse 8-K filings. It works well but it's expensive at scale. His plan was to accumulate examples and fine-tune an open model to bring cost down. [I replied](https://x.com/mstockton/status/2027854211992764430) that this loop - frontier model generates outputs, outputs become training data, training data fine-tunes a cheaper model - could be almost fully automated.

I haven't done fine-tuning in a while. Frontier models just work for most of what I've needed, so I haven't had a reason to. But Virat's post got me thinking about this pattern more carefully, and it seems like something worth exploring.

## Structured Extraction and Evaluation

The reason this pattern seems especially interesting for structured extraction is that it's easier to evaluate. If you're pulling known fields out of semi-structured documents - dates, entities, financial figures - there's a clearer definition of "correct" than with freeform text. Some checks can be automated (does this parse as a valid date? does this value appear in the source document?), and people can review the rest.

If you're using a frontier model for extraction at any real volume, you should already be evaluating its outputs - having people review results, label quality, build an evaluation set. That evaluation work produces labeled (input, output) pairs. And if you orchestrate the system correctly, those labeled pairs can double as training data for a cheaper model.

## What the Retraining Loop Would Look Like

I think the workflow would look something like this:

1. **Run the frontier model on your extraction task.**

2. **Evaluate outputs.** People review and label results. Automated checks can help with the obvious stuff (schema validation, format checks, cross-referencing source documents). This is ongoing work, not a one-time thing.

3. **Evaluated outputs become your training dataset.** Every (input, output) pair that's been reviewed and labeled goes into your training set.

4. **Fine-tune a smaller, cheaper model on this data.** Once you have enough high-quality examples, fine-tune an open model like Llama or Mistral.

5. **Evaluate the fine-tuned model out of sample.** Check how it performs on examples it wasn't trained on. This tells you whether it's actually good enough to deploy.

6. **Deploy the fine-tuned model for bulk traffic.** If it meets your quality bar, route extraction volume through the cheaper model. Use the frontier model as a fallback for cases where the fine-tuned model's confidence is low. You'd also want a way for people to flag bad outputs, so those can feed back into your training data.

7. **Continue accumulating data and periodically retrain.** The frontier model fallback path keeps generating new examples for people to evaluate. Each cycle grows the training set.

If you set up the right hooks - a pipeline for people to label outputs, a process for checking fine-tuned model performance out of sample, off-ramps for routing traffic to cheaper models - the retraining loop falls out of the orchestration. You're connecting evaluation work you should already be doing to a fine-tuning pipeline.

## This Is Just MLOps

The thing that struck me about this pattern is that it's not new. It's the same retraining loop that classical ML teams have been running for years. Collect labeled data, train a model, deploy it, monitor performance, collect more data, retrain.

In traditional ML, labeling was always the bottleneck. You'd hire annotators to label documents from scratch, and it was tedious, expensive, and slow.

Now frontier models are good enough that they can do the initial extraction at high quality, and you can use techniques like LLM-as-judge to get reasonable confidence that the outputs are correct. You still need humans in the loop reviewing labels, but you're spot-checking outputs that are already mostly right rather than creating labels from zero. That makes the human review much less costly, which is a big part of why this pattern feels more viable now than it would have a couple years ago.

I'd imagine teams with classical ML experience have an advantage here. They already know how to build data pipelines, version datasets, run A/B tests between model versions, and monitor for drift. If you've ever built a retraining pipeline for a classification model or an NER system, you probably already know most of what this requires.

## Where I Think This Does and Doesn't Apply

I haven't validated all of this myself, but based on what I've read, it seems like the pattern fits well when:

- There's a clear definition of "correct" - structured extraction, classification, entity recognition
- Volume is high enough to justify the investment (thousands of examples)
- The domain is relatively stable - document formats don't change weekly
- Cost matters at scale - you're spending real money on frontier model API calls

And it probably fits less well when:

- Outputs are subjective or hard to evaluate - summarization, creative writing, open-ended Q&A
- The domain shifts frequently, invalidating your training data
- You need the frontier model's breadth and general reasoning, not narrow pattern-following
- Volume is low - if you're processing a hundred documents a month, just keep using the frontier model

From what I've read, fine-tuning starts making sense around a few hundred to a few thousand high-quality examples.

## Fine-Tuning Has Gotten Easier

The last time I experimented with fine-tuning was through the [OpenAI fine-tuning API](https://platform.openai.com/docs/guides/fine-tuning), and it was mostly hello-world level stuff. I didn't have a real use case to push it further.

The tooling seems like it's gotten a lot better since then, and there are more options now. [Unsloth](https://github.com/unslothai/unsloth) is one I've seen mentioned frequently for running fine-tuning on a single GPU. I have some projects on the horizon where this kind of loop might be worth experimenting with, so I want to spend more time here.

## Final Thoughts

The human evaluation part of this doesn't go away, and I don't want to downplay that. Someone needs to define what "correct" means, review outputs, and make judgment calls about when the fine-tuned model is good enough. But the orchestration around it - the pipeline from evaluated outputs to training data to fine-tuned model to deployment with off-ramps - that part seems like it can be set up once and mostly run itself.

I'm curious whether teams are actually doing this today, and what their experience has been. If you're running frontier models on structured extraction at volume and you're already evaluating outputs, it seems like you're close to having what you need. I want to spend more time exploring this and see what it takes to get a working version of this loop running end to end.
