---
layout: single
title: "Using LLMs to Build Software - A Working Game in 5 Minutes"
excerpt: "I built a playable word game in 5 minutes using Claude's Artifacts feature — no coding required. LLMs are making software development more accessible, reducing the time to prototype, and enabling new types of small, custom applications that wouldn't have been built before."
category: "Building with LLMs"
tags: ["claude", "artifacts", "software-development", "prototyping", "no-code"]
---

<img src="/docs/assets/images/wordspy/1.png" width="600px" height="600px"/>

**TLDR**: I built a word game that you can play online in 5 minutes, without writing any code. Want to play it? [Here's the link](https://claude.site/artifacts/5dda4bea-e334-42cd-a822-71dd2f098840) - Warning -- the sound is a bit annoying, you might want to mute first

### Using Claude to build software in the browser

I'm amazed by Claude's Artifacts functionality. You can create runnable code in the browser using just prompting. This capability substantially lowers the barrier to software development, allowing anyone to build functional software, even without prior coding experience. You can even publish the working software, so that other people can try it out. Below are some of my thoughts on this, along with a link to a game I built in about 5 minutes. If you just want to try out the game, [here's a link to it](https://claude.site/artifacts/5dda4bea-e334-42cd-a822-71dd2f098840). Watch the video below to learn more about how I built it. 

### How I built WordSpy

<iframe width="560" height="315" src="https://www.youtube.com/embed/zQoBKqrOlCM?si=87vW33jHUx57hcls" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Lowering the Barrier to Building Software

Claude Sonnet and LLMs in general have the potential to democratize software development. With Claude, you can write software by simply describing what you want in plain English. People without a significant background in software engineering can start building their own tools and applications. You can create a small piece of software to solve specific problems without needing to understand complex programming languages or frameworks. I still think strong foundational software skills are valuable and necessary to build anything that is moderately complex -- however, having LLMs as a partner during prototyping allows you to accelerate the necessary learning. LLMs can substantially increase the rate at which you can learn how to build software.

### Enabling Custom Software Solutions

Traditionally, many small, custom software solutions never see the light of day because the cost and effort to develop them are too high. LLMs change this dynamic by making it easy and quick to create the baseline of these solutions. Whether it’s a tool to automate a repetitive task or a simple application to address a unique need, you can now start to build it yourself very quickly. Things that otherwise wouldn't have been built in software now can be. The concept of 'disposable software' becomes more realistic with the aid of LLMs.

### Accelerating Prototyping

Another benefit of LLMs is the speed at which you can prototype and develop a working baseline for your ideas. In the past, turning an idea into a working prototype could take weeks or months. With LLMs, this time is drastically reduced. You can have a functional prototype up and running in minutes, allowing you to test and iterate on your ideas faster than ever before.

### Builing a simple word game in 5 minutes

To illustrate these points, here are some additional details on building the game shown above. I decided to recreate a simple game I had built years ago in iOS called “WordSpy” The game involves rows of scrolling letters, and the player’s task is to identify words embedded within these rows. Here’s how it works:

- **Game Description**: The game features rows of letters that scroll from left to right. Most letters are random, but some form a hidden word. The player’s goal is to identify these words as they scroll by.
- **Building with Claude**: I described the game to Claude in plain sentences. I outlined the mechanics, such as the scrolling speed increasing as the player progresses and the option to have multiple rows.
- **Interactive Development**: Claude asked relevant questions about the game, like the number of letters visible at a time and if a visual indicator was needed. After answering these questions, Claude generated working code that I could test in the browser.
- **Refining the Game**: I made some tweaks, such as adding more words to the dictionary and smoothing out the scrolling animation. Claude’s ability to handle these adjustments was impressive.
- **Adding Features**: Within five minutes, I had added options for multiple rows and even some background music. The game was fully functional without writing any React code.


### How should you use this stuff? 

Claude Sonnet’s ability to create runnable code from plain language prompts is a game-changer. It empowers anyone, regardless of their coding background, to experiment with building custom software quickly and efficiently. This opens up a world of possibilities for small, tailored solutions that might otherwise never be developed. Whether you’re looking to prototype an idea rapidly or automate a simple task, Claude Sonnet is a tool that can significantly reduce the time and effort involved.

I encourage everyone to experiment with Claude Sonnet and see what you can create. Feel free to share your experiences and projects with me. I’m always excited to see what others are building. Happy coding!


### One Last Thing

I actually used ChatGPT to help me construct this blog post itself. The first thing I did was record the demo video embedded above, and then I extracted a transcript of the video to help me create the post. I edited the draft that ChatGPT gave me, but it was certainly a good starting point. It's pretty amazing what you can use LLMs for in your day-to-day. I still think there is plenty of room for people to manage and edit the outputs of these models, but they work really well for creating first drafts, acting as thought-partners, etc. The prompt I used to bootstrap this post is below:

```
I would like you to help me write a blog post for my site. Here are some details:

- My site is mattstockton.com, and I would like the style of the post to be similar to previous posts on the site
- The post should be about Claude Sonnet's ability to create runnable code in the browser using prompts.
- The post should highlight the following key benefits:
	1. People without software engineering experience can now build things. Claude lessens the barrier to building software
	2. Removing the barrier will allow people to build small custom software that otherwise wouldn't be built
	3. The time to prototype an idea, or build a workable baseline, has been drastically reduced by these tools.
- I created a youtube video about the game I built. I want you to use the transcript of the video to further enhance the contents of the post. The post should mention details of the game I built. The transcript is below between triple ticks:

<TRANSCRIPT HERE>
```