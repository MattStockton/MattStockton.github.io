---
layout: single
title: "Building Small-Scale Custom Software with LLMs and Gumloop"
excerpt: "LLMs have drastically lowered the cost of prototyping custom software. Using Gumloop, I built an AI-powered podcast summarizer in under an hour — automating transcription, summarization, and PDF generation. It’s never been easier to experiment and build useful tools."
---

The cost to prototype custom software that solves niche problems can be substantially lower with LLM capabilities. Aspects of a software system that previously required deep technical knowledge to build can now often be implemented cheaply and easily with the help of LLMs.

Not every problem you or your company has is worthy of being solved by software. The normal filters still apply, like: "How much time/money will we save?", or "How does the quality of the output change?", or "How long is it going to take to diligence vendors, de-risking that they can actually solve this problem?" - These aren't the only questions, but the point is that there are base costs for consideration when building a thing, and often times these considerations lead you to just do what you were always doing in the first place.

The default assumption until recently is that a problem's scale or impact has to be somewhat large before you consider trying to build something yourself. With emerging LLM capabilities and the tools being built around them, that cost equation is rapidly changing. The base costs have been drastically reduced. It makes more sense now to prototype things sooner, because its easier to see if they work well in a very short period of time.

Here's a small (somewhat toy) example, but it's a real problem that I want to solve in my life. 

### Problem
I listen to a lot of podcasts on my daily run. Most podcasts are technical in nature, and often have a few key take-aways or concepts I want to follow up on. I try to jot down notes on my run, but this doesn't always work well. I want a succinct way to keep track of the key highlights from these podcasts.

### What I did
I used a tool called Gumloop to protoype this. [Gumloop](https://www.gumloop.com/) is a tool that enables you to automate AI workflows with a drag-and-drop UX. I built a simple workflow that did the following:

1. Scraped the website of a recent podcast I listened to (the one I tried was this [Latent Space episode about Brightwave](https://www.latent.space/p/brightwave), which was fantastic)
2. Extracted the full transcript from the website, using a Gumloop node that made an LLM query to GPT-4o
3. Used Claude to generate an LLM prompt that gave detailed instructions on how to summarize the transcript
4. Plugged that prompt in as a new Gumloop node, asking it to run this summarization prompt
5. Added a Gumloop 'Generate File' node, to take the output from the above step and create a PDF from it.

You can see the [final result here in PDF form](/docs/assets/pdfs/podcast_take_aways.pdf), which is a pretty good summary of the key take-aways from the episode (given the constraints I wanted in the prompt generated in step 3 above)

Pretty amazing that you can prototype all of this in under an hour.

### Video Walk-Through
I added a lot more context and narrative to what I did in the below YouTube video. If you watch it, you'll get a much better feel for how tools like Gumloop work, and how you might be able to apply it to problems you're trying to solve.

<iframe width="560" height="315" src="https://www.youtube.com/embed/-dDl3q5vNNA?si=XhXDkY2g2B_Zgw7H" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Time To Build
It's never been easier to get started building. I'm eager to hear what you're trying to build, and where you could use some assistance. I love hearing how others are getting value out of these tools, and what they are struggling with. Let me know what you're working on, and how I can help. I offer consulting services to companies who want to figure out how to adopt these emerging LLM capabilities. If you want to learn more about that, check out [this page](/work-with-me.html), and reach out to me.



