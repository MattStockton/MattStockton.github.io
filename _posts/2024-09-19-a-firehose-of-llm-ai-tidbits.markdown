---
layout: single
title: "A Firehose of LLM / AI Tidbits"
excerpt: "A rapid-fire list of AI insights, tools, and concepts that have caught my attention lately — from practical prompting tips to the latest breakthroughs in multimodal models. If you're looking for a nudge to dive deeper into this space, there’s something here for you."
---

I’ve been pretty far down the rabbit hole of Large Language Models for a while, yet there's still so much for me to learn. I feel so early in the journey. At the same time, I realize I’ve built up a lot of knowledge worthy of sharing. I enjoy writing about what I’m learning here on my site. It’s been a fun way to experiment with tools, get some writing practice in, and connect with others who are curious too. I have a large backlog of topics I’d like to write about. For this post, I’m trying something new. Instead of going deep on a single thing, here’s a firehose of quick tidbits. My goal in sharing this is twofold: (1) to categorize and solidify things I’ve found interesting over the past month or so, and (2) to inspire a few of you to go deeper in this space. Maybe you’ll find something here that is the nudge you need to go deeper. Happy building and exploring.

### The Firehose

When you’re doing something manual or time-consuming, always be thinking about how ChatGPT might help. Like this guy who created calendar invites from a picture of his [kid’s school calendar](https://x.com/mikeknoop/status/1828519928737210549) - I tried this too and it worked. You can use these tools for tedious things. Sometimes they just work.

LLMs will continue to get better at dealing with ambiguity in data inputs. But it’s never a bad idea to structure your input data intentionally. Intentional design around your company’s documentation formats, and [making them ‘LLM friendly’,](https://x.com/_xjdr/status/1827737014315483483) will make adopting these tools easier for you in the long run.

LLM hallucination is a feature, not a bug. It’s *by design* non-deterministic. It can do amazing things for you, if you work with it the right way. Don’t reject it too early, and learn about what it’s good at and why. There are techniques to make it more deterministic and more reliable. Learning these techniques are valuable, but it’s ultimately more valuable to accept the uncertainty and [build with it in mind](https://x.com/simonw/status/1828074949330030893).

Don’t think of AI tools as ‘it will do the work for me’ - think of them as thought partners to get better at your work. Treat it like a work partner, an intern, a teacher. It doesn’t do your work, it [helps you get better at it.](https://x.com/nateliason/status/1828100294640796122)

The AI ecosystem is like a set of lego building blocks. There is a huge set of tools to consider using, at multiple abstraction levels (e.g. build from scratch, use some libraries, use one tool, use a suite of tools), and also with different modality focuses (e.g. text, video, voice, etc.). It’s really easy to feel overwhelmed, but building a mental model for [what you use when, and why](https://x.com/eglyman/status/1828114640108237216) — is an extremely valuable exercise. It’s also iterative.

There are truly amazing breakthroughs happening in the vision and image space. Things that weren’t possible a year or two ago are trivial now. This is going to lead to some wildly novel products — and understanding the ‘new possible’ is a really valuable thing. What can you build with it now? So much new opportunity space. As example, this is wild to me: predicting rainfall not based on weather data, but on [actual past radar weather maps](https://x.com/emollick/status/1828453641830699200)

There’s no excuse now to get started learning. There is a huge amount of high quality, free content to [help you learn](https://x.com/bentossell/status/1831252122257813843) . Go to [bensbites.com](https://bensbites.com/)  → Course Catalog → Filter For Free → Choose Difficulty Beginner. 68 courses to choose from. Choose one that catches your eye and just get started.

The big players like Anthropic Claude have fantastic documentation for stuff like learning how to prompt. Better yet, there’s incredibly talented people who are summarizing the [key take-aways for you](https://x.com/simonw/status/1829352666142757365) - Find the right people and follow them on Twitter.

It’s not just Twitter though. There are some truly incredible people sharing their knowledge for free on their personal site. For example, if you spent a day or two reading all of what [Eugene Yan](https://eugeneyan.com/start-here/) writes, you’d be so much further ahead than almost everybody. You don’t even have to read everything. The first link on this page is ‘[Lessons from a year of Building with LLMs](https://applied-llms.org/)’ - Read that alone and you’re probably ahead of 90% of people in terms of knowledge. Find the ‘Eugene Yans’ that write about what you’re trying to learn.

You can get a lot of interesting ideas for products to build by just looking at different datasets. LLMs give us an entirely new way to use data. If you’re itching to build a product, spend a day just looking through [free datasets](https://x.com/Sumanth_077/status/1830248952022921588) with the background thread of ‘what product could I build with this?’

Most people I know who are excited about the space and are eager to learn more had 1 or 2 - ‘Holy Sh*t, you can do that?’ moments. It’s actually not that hard to find one, where you can try it out end-to-end yourself. Maybe that’s the nudge you need to get started. As an example, here’s a quick tutorial on how to make [AI images of yourself using Flux](https://x.com/fofrAI/status/1831359030733709433)

Circling back to video and image stuff. The things you can do *out of the box* now are just mind boggling. Multi-modal models can just do things. [Incredible things](https://x.com/emollick/status/1829165609525096929)

If someone is talking to you about why AI is all good or all bad, [don’t listen](https://x.com/emollick/status/1830350308729380981). Like anything, there is nuance. Lacking nuance while learning is just going to block your exploration. Like any tool, understanding how it works, when it should be used, and what it’s good at — is going to make you better as using it.

I said above that you can think of AI tools as an intern, a teacher, a co-worker, a professor. Another way to think about it: [It’s a map](https://x.com/zswitten/status/1830423444502261907)

There are so many tools in this space, and it’s easy to get bogged down, but it’s also good to know what’s out there. Let other people do the work for you, and keep a pulse on what [others are using](https://x.com/omarsar0/status/1833913149395030222) - But don’t make that the focus. You could spend all your time keeping track of all the things.

There’s a lot of noise on prompting techniques, but there’s some gold in the hills. Rely on the documentation provided by the big players (e.g. [Anthropic](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)), and also [people that really have deep experience](https://x.com/skirano/status/1835386182512894407) playing with these tools. There’s huge alpha in learning prompting, and continuing to learn and iterate on what works for you

Writing Evals is a big topic right now for folks building LLM systems. There’s some really interesting and helpful [emerging content on this](https://x.com/alexalbert__/status/1835717512404914401). But the key thing to remember is that you’re building software, and you need to test it — just like every other piece of software you build. LLM outputs are probabilistic, but there are still plenty of techniques you can use to build robust and tested systems.

You should try out NotebookLM to [create a podcast](https://mattstockton.com/2024/09/12/2024-custom-podcasts-with-notebook-lm.html). If you haven’t had your ‘Holy Sh*t’ moment, let this be it. It’s free and takes 10 minutes

Keep close tabs on OpenAI’s o1 models. It feels like we’re really on the verge of a step-level change in what’s possible. Here are a few interesting tidbits about that:

- [Writing code from a technical paper](https://x.com/emollick/status/1835342797722767592)
- [Oscar Health’s experience so far](https://x.com/emollick/status/1835000528972984829)
- What an [extremely smart person](https://x.com/simonw/status/1834361725560225969) has learned about it so far about the different models
- Some pretty cool (and short) [video demos](https://x.com/swyx/status/1834284741610405965)

If you build stuff, you should try out [Cursor](https://x.com/svpino/status/1836015426376998956) or [Replit](https://x.com/bentossell/status/1836038650758590638). I know there’s been some amount of resistance to using these tools, particularly for experienced folks — but this is where things are going. My honest take is that these tools are even more valuable for experienced folks, because they still can use all that hard-won knowledge to fix the errors the tools make. 

Finally, it’s very hard to keep up in this space. You could accidentally make that your full-time job. You need to find the balance of ‘keeping up’ but also actually trying things and building. My hard and fast rule: Don’t overthink it too much, don’t be too anxious if you feel like you’re missing new things, and if you are uncertain about how to spend your time, bias towards building. The best way to learn is to put in the reps. 

In terms of keeping up, you’ll notice that almost all of the above links are to Twitter. Twitter is *by far* the best way to keep up on the space. You just have to follow the right people, ignore the noise, and know when to put it aside. 

### What Are You Building? How Can I Help?

Hope you found this helpful. If you have good resources, notes, knowledge to share, send them my way. If you or your company need help building or learning more — I can help. [More about how you can work with me here](/work-with-me.html)