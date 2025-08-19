---
layout: single
title:  "Prompt Engineering Quickstart"
category: "Getting Started with AI"
tags: ["prompt-engineering", "quickstart", "fundamentals", "techniques", "learning"]
---

I want to build my [Prompt Engineering](https://en.wikipedia.org/wiki/Prompt_engineering) skills. As I highlighted in a [previous post](/2024/04/29/cointelligence-take-aways.html), I’m convinced that LLMs will be a huge part of the future of work. Understanding how to use them most effectively will be an incredibly valuable skill. There are many published resources on Prompt Engineering out there. It’s difficult to filter the signal from the noise. After a bit of searching, I decided to watch [Andrew Ng](https://twitter.com/AndrewYNg)’s and [Isa Fulford](https://twitter.com/isafulf)’s [Prompt Engineering Course](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/) on Coursera. I recently audited Andrew Ng’s [Machine Learning Specialization](https://www.deeplearning.ai/courses/machine-learning-specialization/) Course, and he is a fantastic instructor. He is able to explain complex topics very clearly. He is also pretty funny.

I enjoyed the Prompt Engineering course. Although there is still a lot to learn in the space (and it's changing every day), this course provides solid building blocks in a very short amount of time. I encourage interested folks to spin through the course themselves (it takes an hour or two). Below are my notes from the course.

### Course Notes

- Write clear and specific instructions. Clear and specific does not necessarily mean short. Good instructions are often quite detailed.

- When including additional data in the LLM prompt (e.g., text you want to summarize), use delimiters within the prompt (e.g. triple back ticks) to distinguish the instructions from the data.

- Ask the LLM for structured output, such as HTML or JSON. For JSON, specify the keys you want to be present in the output.

- Ask the LLM to check if certain conditions are true within the instructions. If conditions aren’t true, ask it to generate a different output (e.g. ‘If the text doesn’t talk about XYZ, output ‘false’ instead of the output described above’)

- Use the ‘few-shot’ prompting technique, where within the prompt itself, you provide a few sample ‘correct’ answers to the prompt. This helps to guide the LLM on what a good answer looks like.

- Break apart the task you want the LLM to complete into separate steps (e.g. instead of asking for the final answer, give the LLM sub-tasks to complete that builds towards the final answer — step 1: do this, step 2: do that, step 3: finally, do this).

- When breaking apart a task into sub-tasks, you can specify the output you want the model to provide for each sub-task. For example, if the first step is to create a summary of text, and the next step is to translate the text, you can ask it to format the response as:
    - Summary:
    - Translation:
<br><br>

- Ask the LLM to show its work. If it is a multi-step problem, asking the LLM to show incremental work will allow it to identify errors while building towards the final answer.

- When building a prompt, you should iterate. The prompt will generally not be ideal the first time you try it. Start somewhere, analyze the results yourself, and continue to iterate the prompt based on the results. There is no such thing as a ‘canned perfect prompt’ —  an iterative process, where you revise based on how well you think the LLM is performing, will give you better results.

- LLMs are useful for summarization tasks. When summarizing, it is useful to be specific on how you want text to be summarized. For example, you can specify how many words you want, or what aspects of the original text you want the summary to be focused on.

- LLMs can be useful for inferring information from text. For example, you can use LLMs to understand the sentiment of a product review.
    - When asking for sentiment, it is useful to ask about a specific sentiment (e.g. ‘Does this review represent anger,? give your answer as true or false’)
    - You can extract / infer multiple aspects at once (in a product review, this could be ‘item’ and ‘company’.)  In your prompt, you can give a bulleted list of the aspects you want to extract, and even specify the format you want in the answer (e.g. JSON).
<br><br>

- LLMs can infer the topic of text. It is useful to specify the list of possible topics that the LLM should choose from (e.g. instead of instructing it to ‘identify the topic’ , ask it to ‘identify the topic from the list: x, y, z’).

- LLMs are useful for transforming and translating text. Some example usages:
    - Translating text from one language to another
    - Transforming the tone of a specific text (e.g. ‘transform this text into more formal language’)
    - Transforming data from one format to another (e.g. ‘transform this JSON list into an HTML table’)
    - Proof-reading, spelling and grammar correction (being as specific as possible about what you want to correct can be beneficial)
<br><br>

- LLMs can be useful to generate new text or respond to text based on a set of instructions. (e.g. generating a draft response to a customer complaint email). Be specific about what you want the model to do (e.g. what tone do you want? what aspects of the original text do you want to highlight? If the input text has a specific sentiment, do you want the response to be something different?).

- Using the temperature setting in the LLM API is a way to control the variability of the answer. Remember that LLMs are at the core just predicting the next word in a response. If you increase the ‘temperature’ you are allowing the LLM to select a ‘less likely’ next word. The default for temperature is generally 0, which leads to more ‘stable’ responses given the same input. If you are okay with more variability, experiment with increasing the temperature.

- When using the OpenAI API, you can pass in a list of messages to the API, and specify what type of message it is (either system, user, or assistant). The system message sets the overall context of the conversation (e.g. you are guiding the assistant). The user message is the ‘user’s input’, and the assistant message is the LLM’s response. Sending a list of messages to the API allows for continuity in the conversation, and allows you to build much more elaborate experiences than what you can have via the standard OpenAI web interface.

### Other Resources
Here are some other resources I intend to check out as well. What else are you using to learn? Drop me a note!

- [Prompt Engineering Guide on Github](https://github.com/dair-ai/Prompt-Engineering-Guide?tab=readme-ov-file)
- [OpenAI Prompt Engineering Guide](https://help.openai.com/en/articles/6654000-best-practices-for-prompt-engineering-with-the-openai-api)
- [Learn Prompting](https://learnprompting.org/)
- [Awesome GPT Prompt Engineering on Github](https://github.com/snwfdhmp/awesome-gpt-prompt-engineering)