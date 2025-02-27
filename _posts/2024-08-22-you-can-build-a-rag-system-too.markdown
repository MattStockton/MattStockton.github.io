---
layout: single
title: "You Can Build a RAG System Too"
excerpt: "RAG sounds complex, but it’s really just using a custom search engine to feed better context to an LLM. A great place to start is Santiago’s step-by-step tutorial — under 100 lines of code. If you’re curious, just dive in. The hardest part is getting started."
---

In software engineering, we have the tendency to invent complex terminology to describe relatively simple concepts. I’ve experienced that as I’ve learned more about Large Language Models and what we can do with them. Here’s an example: **Retrieval Augmented Generation (RAG)**. What’s that? To me, it is: *Using a custom search engine to find information, and including that information in your initial model prompt before running it*.

Even better than my definition — you can actually use LLMs to explain stuff like this to you. I sent the following prompt to ChatGPT: 

>Prompt: “Explain RAG to me in 2 sentences assuming I work in a technology company but am not a software engineer. Explain it simply, without any acronyms, and in a casual manner”
>
>Response: “RAG is a smart way for AI to first look up the best information from a huge collection of data, and then use that info to create accurate and detailed responses. It’s like having a supercharged assistant that quickly finds and shares the right answers, making tasks like support or writing much easier.”

Not bad. This use-case of ‘explain it to me like this…’ is one I love to use for concepts I’m eager to learn about. You can have fun with it too:  

>Prompt: “Explain how the planets move. I am 5 years old’
>
>Response: “The planets move around the Sun like a big merry-go-round. They keep spinning in circles, each one on its own path, and they never bump into each other because they stay in their own lanes.”

It’s always refreshing to me when I find content online that describes complex subjects in very accessible ways. For RAG, I found one recently, that I absolutely love. It’s a 50 minute YouTube video called ‘A gentle introduction to RAG’ paired with a Github Repo. It’s by [Santiago](https://x.com/svpino) - who puts out a lot of other high-quality content as well.

- [YouTube Video](https://www.youtube.com/watch?v=q9MD_hU2Yd8)
- [GitHub Code](https://github.com/svpino/gentle-intro-to-rag/blob/main/rag.ipynb)

It walks you through step-by-step on how to build a baseline RAG demo. It’s under 100 lines of code. It walks you through all of the key building blocks, with great diagrams. The explanations are clear and succinct. If you do it, you’ll even learn about other tools like Llama, LangChain, Vector Stores, and Embeddings. You are well on your way to building something in under an hour — so much signal to noise here. I truly think anyone, with enough persistence, could work through this example in an hour or two. Like I always say, if you want to learn - **Just Get Started**.

The cool thing is, once you learn the baselines and build some curiosity — it opens up all of these other paths to explore. Watched the video, and think RAG is cool? You can go as far down the rabbit hole as you'd like to. 

For example, this is a recent Podcast I listened to:  [**Contrarian Guide to AI: Jason Liu on Betting Against Agents while Doubling Down on RAG & Fine-Tuning**](https://podcasts.apple.com/us/podcast/contrarian-guide-to-ai-jason-liu-on-betting-against/id1747605459?i=1000663186339)

[Jason](https://x.com/jxnlco) is truly an expert in this space, and shares a ton of great knowledge on how you can improve your RAG implementation. He briefly mentions Hypothetical Document Embeddings in the podcast. Sounds scary right? Let me check:

>Prompt: “What does Hypothetical Document Embeddings mean for RAG? I am new to LLMs”
>
>Response: “Hypothetical Document Embeddings in the context of RAG (Retrieval-Augmented Generation) refers to a technique where the AI creates “imaginary” summaries or representations of possible documents, even if they don’t exist in the database. These summaries help the AI think about what information *could* be out there and improve its ability to find or generate accurate and relevant responses, especially when the exact data isn’t readily available. It’s like giving the AI a better sense of what to look for when answering complex questions.”

Okay, I think I understand it a bit better now! And this podcast has like 5 other concepts that you might be eager to explore once you listen. It all branches out if you have curiosity and time. Jason also says something that I firmly believe:

There is a discussion about what is constant about skills that will be valuable, regardless of the current tech hype (I don’t recall the exact context but it was something like this). The response from Jason was something like: **Can you clearly describe what you want? Can you write well?** - I think this is more true than ever — even more so with the emergence of LLMs. Honestly, they make it **more accessible** for a broad range of skill-sets to build a thing. If you think you can't get started because you don't have the background of the skills, I think you're wrong. Go try a thing, you'll be pleasantly surprised.

It’s an amazing time to be building in this space. Are you or your company curious? Do you need some help, advice, or some cheering on to get you started? Don’t hesitate to reach out: mattstockton@gmail.com