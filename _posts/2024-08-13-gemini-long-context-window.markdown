---
layout: single
title: "Using Google Gemini's Long Context Window to Analyze Small Cap Stock Annual Reports"
excerpt: "I used Gemini's long context window to analyze company annual reports — processing hundreds of pages in minutes to rank small-cap stocks. This kind of deep document analysis was nearly impossible before, but LLMs are changing what's feasible at scale."
category: "Finance & Investing"
tags: ["gemini", "long-context", "document-analysis", "small-cap", "annual-reports"]
---

Google built an LLM with a large input context window named [Gemini](https://blog.google/technology/ai/google-gemini-next-generation-model-february-2024/). A context window is the amount of text an LLM can consider at once when generating a response. Gemini 1.5 Pro has a context window limit of 2 million tokens. As comparison, ChatGPT 4o has a limit of 128k. A large context window lets you create long LLM prompts with limited data preparation work. To give you a frame of reference, the entire Harry Potter series contains just over a million words. A token isn't a word, but it's likely you could use all of the book text in a single LLM prompt. Then, the LLM could reference all the material to answer the real prompt you asked. Incredible stuff.

I wanted to experiment with long context windows, and put together a video of this experimentation. You can watch the video here, and see the steps I took outlined below. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/yG9r8a0chLc?si=_ayRICKiAHmcWwVF" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### Analyzing Company Annual Reports Using Gemini

I’ve spent a bunch of time in the investment field at a few hedge funds and FinTechs. I’ve seen my fair share of very long and dense PDFs, and a desire across many colleagues to make sense of this unstructured data. Long context windows can be a great tool to help solve problems like this, which would have been near impossible to solve before.

I applied this concept to annual report PDFs from US companies. I’ve always been interested in small cap stocks, but not interested enough to dedicate substantial time to find, research, and analyze companies. I wondered if I could surface a few companies and learn more about them within 30 minutes. I wanted to go deeper than just going to Yahoo Finance and reading some articles. I wanted to use the actual documentation the companies submit at the end of the year.

### What I Did

Here are the steps I took. You can see below that I used a handful of different LLM tools to accomplish this. This is one of the cool things about the space. **You don’t have to choose one tool, you can use a bit of everything to solve your specific problems**. 

1. I used Claude Anthropic to generate ideas for stock screening criteria (note the prompt is a little funky because I was speaking it versus writing it, which is another awesome use-case in itself — **just talk to your LLMs** -- they are good enough to deal with messy text as input)
    
    > I would like you to get me a useful stock screener that's successful investors use to find stocks in the small cap size. I'd like five good filtering attributes that I could plug into a stock screener to service 10 to 15 companies. 

    Claude helped me settle on the following criteria:

        - Market Cap: 300m to 2b
        - P/E Ratio: < 20
        - Debt-to-Equity: < 0.3
        - Revenue Growth: > 15%
        - ROE: > 20%

1. I used a free screening tool called FinViz to filter stocks using the above criteria.
    
    <img src="/docs/assets/images/gemini-stocks/1.png" width="600px" height="400px"/>
    
1. I used [AnnualReports.com](http://AnnualReports.com) to download annual reports for the companies in PDF format. Here’s an image of 1 page of a single report. The total page count across all the reports approached 1000 pages, and the data was very unstructured (images, tables, paragraphs, graphs, etc.)
    
    <img src="/docs/assets/images/gemini-stocks/2.png" width="500px" height="300px"/>
    
1. I used ChatGPT to generate a prompt which instructs the LLM on how to analyze the PDFs. This is one really cool use-case of LLMs. **You can use LLMs to create better LLM prompts!**. There are even specific tools out there now to help you with this, but even using ChatGPT to help you build prompts is really valuable and beneficial.

    > You are an expert prompt creator for large language models. I am going to tell you what I want to do and I want you to give me a prompt that I can use for a large language model. Below is what I want to do between triple ticks:
    > 
    > 
    > I want to upload a set of about 10 PDFs of annual reports from companies I'm considering investing in. I want the large language model to do an analysis of the companies and come up with a ranked list of what it thinks I should invest in. Please give me a prompt that I could use for this.

1. I plugged all of the above into a prompt on [Google AI Studio](https://ai.google.dev/aistudio) (both the text prompt and all of the PDFs). Google AI Studio is a web-based interface that allows you to try out their different models. Very similar to ChatGPT but with different controls. Here’s a snapshot of what that looks like:
    
    <img src="/docs/assets/images/gemini-stocks/3.png" width="500px" height="300px"/>
    

    The output from the above was pretty impressive. Here’s a snapshot of the output from Google Gemini:

    <img src="/docs/assets/images/gemini-stocks/4.png" width="500px" height="300px"/>

1. I even asked a follow-up question to get the LLM to describe how it ranked the top company over the second ranked company:

    > Can you describe how you ranked Esquire Financial Holdings above Ardmore Shipping Corporation. Please walk me through your thought process step-by-step

    <img src="/docs/assets/images/gemini-stocks/5.png" width="500px" height="300px"/>

### Final Thoughts

Overall, this is really impressive stuff. In less than 30 minutes, I had a bunch of distilled information about these companies I had never heard about before, along with some comparison between them. If done from the browser, it’s all free. If you automated this in software, the analysis would likely cost you under 1 dollar. This is definitely a novice approach to curating investments, and it’s surely not investment advice — but for a ‘first pass’ in 30 minutes, and no cost? Amazing.

I’m eager to track all of the developments in this space around context window length. I’m also eager to learn more about when you should be using long context windows versus when you should be using something like [RAG](https://www.promptingguide.ai/research/rag). One interesting aspect for all of these models is the output windows are still quite small — so you are limited in the amount of text you can output in a single prompt. This limitation is also why it’s worth understanding the techniques for chaining queries together and for prompting in general — having an output from one query be an input to another query is a really good pattern to understand. I wrote a bit about prompting [in this post](/2024/05/07/prompt-engineering-quickstart.html) 

I hope you enjoyed this post. Are you working on something that could benefit from LLMs? Do you need some help or advice? I’d love to hear from you and figure out how we could work together. **I'm open to Fractional CTO roles, co-founder roles, and AI / LLM consulting projects starting in September**. Email me: mattstockton@gmail.com
