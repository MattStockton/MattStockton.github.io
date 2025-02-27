---
layout: single
title: "Key Takeaways from Jason Liu's Podcast on RAG Pipelines"
excerpt: "Jason Liu’s TwiML podcast covered high-signal lessons on RAG pipelines — why structured evaluations beat stochastic testing, how chain-of-thought prompting outperforms multi-step prompts, and why structured reports often deliver more value than chatbots. A must-listen for LLM builders."
---

[Jason Liu](https://jxnl.co/) creates incredibly high-signal AI and LLM content online. I try to read or listen to everything he creates. His recent [podcast appearance on TwiML](https://twimlai.com/podcast/twimlai/why-your-rag-pipeline-is-broken-and-how-to-fix-it/) did not disappoint. I’ve been trying to better distill my key takeaways from podcasts and articles. Here are my notes from this podcast. Each point references a quote from the episode. I pulled the quotes from the YouTube transcript, so they might not be 100% accurate — but they are directionally correct. This episode is definitely worth a full listen.

### Build structured validations before using stochastic testing methods like LLM-as-judge

It might seem easier to write another prompt to test your outputs, but what are you really testing for, and do you want a stochastic process to own that? Figure out what ‘correct’ really means and write a structured test for it first.

> "You feel in control because you can fumble with it, but you're not going to get any results. And they said, okay, well, let me work with a different prompt instead, rather than building a precision recall dataset, right? I think there are many, many tasks that take milliseconds to compute, that we could run tests across thousands of examples and figure out what the relevancy looks like rather than looking at them as a judge."

### Wanting "Complex reasoning" could signal a lack of clarity on the problem

If you want specific behaviors, build specific prompts. If you don’t know what specific behaviors you want yet, do problem discovery first. LLMs aren’t magic; they do what you tell them to do. Don't let them fill in the gaps of problem discovery for you.

> "…I really wish these models were capable of more complex reasoning. And it's like, do you want the complex reasoning because you haven't reasoned about what the customer wants?"

### Use prompt chaining, especially in multi-modal use cases

Have an image? Ask the model to output a description of that image, and use that description as input to another prompt or as data in your retrieval system.

> "What I've seen go really well is actually using a visual language model to give a detailed description as like a paragraph of the image, and then just X embed the paragraph. But what this means is now the describe this image prompt is another hyperparameter to experiment against."

### Measure prompt iterations quickly with quantitative outputs

When iterating a prompt, you need tests that run quickly and provide quantitative outputs (e.g., % recall). Quantitative measures allow you to improve incrementally, preventing a whack-a-mole effect. This is particularly useful when you have team members who haven't done classical ML testing. Giving them a baseline set of evaluations allows them to 'hill-climb' and learn the art / science of iterative improvements. 

> "And I've seen situations where if you just say, describe this image, recall is like 27 percent. But if you can teach this concept of recall to an engineer, and you just make them hill climb for like a day and a half, we've been able to get to like an 87 percent recall just by improving the prompt."

### Avoid relying on long context lengths as a crutch

Long context lengths give you a ton of optionality, but shouldn’t be used for putting junk into the context window. The better you focus the model with concise prompts and clean, high-signal data, the better outcomes you’ll achieve.

> "And so, like just saying, like, this is the number of context length doesn't say enough about how well the model, how good a job the model does at attending to all the various things in the context. And so, you know, that gets to, you know, concepts like precision and recall and other things. Like, do you have a structured way that you think about that or like the way that you would approach evaluating a different context length?"

### Detailed chain-of-thought prompting can outshine multi-prompt patterns

Using a single, detailed chain-of-thought prompt often yields better results than breaking tasks into multiple prompts, especially when working with long context windows. This approach allows you to guide the model through each step in one go, leveraging its capacity to attend to all relevant information without splitting instructions across stages.

Chain-of-thought prompting also forces you to clarify your problem-solving process, helping you refine your approach as you lay out precise instructions. This single-prompt structure is easier to iterate on, leading to more consistent, high-quality outputs and a clearer understanding of your task requirements.

> "And that's mostly how I think about using a lot of context models when it comes to very few data, which is just to say, I want you to attend over everything, reorganize the information in your chain of thought, in your scratch pad, and then finally give me a final result. And that has usually worked pretty well. That's been the difference between something we could ship to something that is actually sending follow up emails right now in production."

### New model integration is straightforward with structured prompting

With a well-structured, single-prompt approach, integrating a new model becomes much simpler. Since the entire prompt logic is contained in one place, it’s clear where adjustments need to be made. When you want to try a new model, you can often just update the model number in the API query — no need to adjust multiple prompt stages or agentic patterns, which can be harder to manage. This simplicity enables faster experimentation and testing with the latest models.

### UX and micro-copy can dramatically impact data collection in feedback loops

Sometimes, the most effective improvements come from simple product or UX changes. Jason boosted user feedback by 5x with a single micro-copy adjustment. Small, thoughtful tweaks like these compound over time, so it’s valuable to incorporate this mindset into your process for continuous system enhancement.

> "Like one of the great examples I discovered with Zapier, working with them for a couple months, was we changed the copy of 'how did we do' to 'did we answer your question today?' And that in itself 5x the amount of feedback we were able to collect per day. And that basically meant within one month, we got enough data that we could get together as a team, review all the examples, and figure out what we want to do next month."

### Structured reports can be more valuable than chatbots for many LLM use-cases

For many LLM applications, a structured report format is often more effective than a chatbot. Defining the ideal report format is itself a valuable exercise in problem and solution discovery, helping you clarify what information matters most and how it should be organized. Building a system to generate these reports can add more targeted value than open-ended chat, offering users clear, actionable insights in a format tailored to their needs.

> "One of my most popular takes on RAG is that question answering is very low value and cost centered. Whereas one of the big things I see in the companies that I've been advising, like Vantager, for example, [vantager.com](http://vantager.com/), they do report generation. So instead of saying, given a data room, can I ask a bunch of questions about how the founders met and what is the TAM of their business? Vantager just says, if you give me a data room, I will just pre-generate every report that you use to make a decision in your business. And now you can just use the workflow of reviewing reports. But now you can start processing 40 businesses a quarter, you can do 80 businesses a quarter."