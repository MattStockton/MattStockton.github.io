---
layout: single
title:  "Building Custom GPTs"
---


Building Custom GPTs is an interesting way to create customized LLM chat functionality with limited effort. I've observed that most people using LLMs tend to use the standard interfaces provided by Claude, OpenAI, etc. These interfaces are easy to use, yet there is still adoption friction, simply because people don't know how to get started, or what prompt context to provide. Custom GPTs allow you to add customized context to a chatbot, and allow you to add buttons to get the conversation started without typing. It's an interesting paradigm that could lessen adoption friction amongst teams.

<img src="/docs/assets/images/custom-gpts/1.png" width="600px" height="400px"/>


Here's a video demo of a Custom GPT I built to help guide leadership decisions. I read a lot. I enjoy reading leadership / management books. I take notes and highlight aspects I find interesting, but like any information that I don't use regularly, it disappears from my brain over time. I've wondered if GPTs are well-suited to solve this retention problem, by being able to access the context and learnings from books I've found interesting **in the context** of a specific decision I'm trying to make. This Custom GPT was my 'attempt to prototype a solution in 10 minutes'

If you want to try out the Leadership Decision Mentor GPT, you can [use it here](https://chatgpt.com/g/g-Z94a9Qz8a-leadership-decision-mentor)

### Video Walkthrough

<iframe width="560" height="315" src="https://www.youtube.com/embed/6IPzktF-Qzg?si=kHxW8jWFrNPeXYLy" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Key Benefits of Custom GPTs

In the video, I go into detail on what I find most interesting about the custom GPT paradigm. Here are a few key take-aways:

- **Tailored Prompts / Instructions** : Custom GPTs let you embed specific instructions that are always available to the GPT. Writing good prompts isn't difficult, but it requires some baseline knowledge of what effective prompting looks like (if you're looking to learn more on this, I highly recommend Andrew Ng's prompting course on Coursera). If you're trying to build LLM functionality for your team, and you have decent knowledge of how to prompt effectively, custom GPTs are a great thing to try out.
- **Conversation Starters** : One friction to adoption of LLMs is that people don't know what to ask or where to start. With Custom GPTs, you can build a set of buttons that a user can just click to get started. In the example above, I added a few 'leadership questions' I've had over the years. Instead of typing something out to get started, the user can just click a button. One example I added is: `I need help communicating a change to my organization's team structure.`
- **Quick and Easy Setup**: The creation process for custom GPTs is straightforward, allowing you to build prototypes quickly without needing any coding skills. In just a few minutes, you can have a working custom GPT that you can share out to your team. OpenAI actually uses a Custom GPT to help you build your own Custom GPT (a bit confusing I know, but check the video.)
- **Enhanced Contextual Responses**: You can configure these GPTs to reference specific books, documents, or even APIs. In the example above, I asked it to reference books like “High Output Management” and “Radical Candor” when answering questions. The GPT will use context from those books to inform the chat. It doesn't have to be books, it could be a set of documents that you want the custom GPT to use. For example, if you have a company SOP manual, you could consider uploading it so that the custom GPT had access to it when chatting.
- **Easy Sharing**: Once your custom GPT is set up, sharing it is simple. You can publish it or share a link, making it easy for your team to access and start using it right away. This aspect is the most interesting to me, because I think it's a way for LLM early adopters to get some of their teammates involved in the fun.
- **Potentially Improved Adoption**: Custom GPTs reduce the friction in adopting large language models by offering more guided and context-aware interactions. This makes it easier for teams or companies to integrate and benefit from these technologies, without having to build custom software.

### Final Thoughts
Creating custom GPTs is a valuable, low-effort way to build curated functionality for your team. With just a bit of setup, you can embed specific instructions and references, making these tools more tailored for your specific needs. This paradigm is a nice middle-ground between using the generic LLM UIs, and building custom software. Building something custom takes more effort -- and you'll have more control over it -- but using a custom GPT is so much lower friction, with some clear upsides. I'm eager to continue prototyping a few ideas I have with this technology. Reach out to me if you have questions, or if you are building anything cool with LLMs and want to chat. I'm happy to help you out.

Here's one more screenshot from the custom GPT I built:

<img src="/docs/assets/images/custom-gpts/2.png" width="600px" height="400px"/>
