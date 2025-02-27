---
layout: single
title: "Analyzing Companies with LLMs - A Simulated Investor Conversation"
excerpt: "I used LLMs to simulate a conversation between Warren Buffett and Joel Greenblatt analyzing a company’s annual report. The results were fascinating — and just a glimpse of what’s possible with creative prompting. Full inputs and outputs included."
---
***Note***: I’m trying something new in this post. I’ve included a PDF document at the bottom that contains some full input and output prompts from the experiments described below. It’s a lot of text, so I didn’t want to include it inline. Let me know if you read through that piece, and what you think!

### Previous Experiment With Company Annual Report PDFs

LLM Long context windows allow you to analyze unstructured data with limited effort. As I’ve written before, I'm interested to research how this capability enables us to summarize and extract signals from company annual reports for investing purposes. [In this previous post](/2024/08/13/gemini-long-context-window.html), I wrote about how I:

1. Used an LLM to build an attribute-based stock screening criteria
2. Identified 10 stocks matching the criteria using a free screening tool
3. Downloaded the annual report PDFs for the stocks
4. Used an LLM to build a detailed prompt to analyze the reports
5. Used Google Gemini’s Long Context Window capabilities to run the prompt and make some recommendations

### Why you should care about LLMs - creativity

LLMs can be helpful in summarizing dense information and extracting knowledge. That’s essentially what the above is doing. This is useful, but I think the *really cool stuff* is within more creative utilizations of these tools. There are a few things I love about LLMs:

1. Their ‘brain’ has read mostly everything on the internet, and can use that information to generate responses
2. They can ‘think’ faster than everyone else
3. They are up to almost any challenge, however unique or absurd it is, and will never say no. They are willing to try anything.

### Getting Creative With Company Analysis

To me, #3 is where the real fun stuff can happen. It’s just up to you to play along and have a bit of creativity as well. With that viewpoint, I followed up on the Small Cap Investing exercise and did the following:

1. I focused on the company that Gemini was most excited about (Esquire Financial Holdings)
2. I used Claude Sonnet to build a detailed LLM prompt that simulates a conversation about ESQ amongst well-known investors. **Using prompts to build prompts continues to be one of my favorite use-cases**. Here’s the prompt I used:
    
    > You are an expert prompt designer. I want you to design a prompt for the following problem:
    > 
    > I want to be able to upload the annual report of a company. I want to build a prompt that instructs the large language model to pretend to have a conversation between Warren Buffett and Joel Greenblatt. The large language model should take on the persona of these two very notable investors. The goal of the conversation between them would be to analyze and talk about the company from the annual report. Ultimately, I want them to come up with a recommendation to either invest or not invest in the company and give their reasonings why

3. I used the output of step 2 above, along with the ESQ annual report PDF, and plugged it into Gemini. The results were interesting. Here’s a snippet (and you can see the full conversation in the assets attached below)
    
    > **Greenblatt:** I agree. Their balance sheet is also quite robust, with a healthy liquidity position, low debt, and strong capital reserves. Their Tier 1 capital ratio is 14.13%, well above the regulatory requirements. That’s a good indicator of their financial strength and their ability to withstand economic shocks. But let’s see if their business has any staying power.
    > 
    > **Buffett:** That’s where I start getting curious. What’s their competitive advantage? Do they have an economic moat?
    > 
    > **Greenblatt:** They’ve got a couple. Firstly, they’ve carved out a niche within the legal industry, focusing on litigation-related lending. This gives them a specialized expertise and a deep understanding of their client base, which has allowed them to build strong relationships and capture a large market share. Second, their payment processing business is also profitable and provides a stable source of revenue. I’d say they have a decent moat in those areas.
    > 

### What Else You Can Try

Fascinating stuff. And this is just scraping the surface with 10 minutes of work. There are many directions you can go from here. As an example, I asked the LLM to re-generate the conversation with Howard Marks and David Einhorn included as participants, which added some differeing views. As another quick follow-on, you could consider building a new prompt with the following instructions:

>You are an expert prompt designer. I have used the prompt below (between double quotes) to generate a conversation between well-known investors about a small company. I have the output of the conversation, and I want to generate a new LLM prompt to analyze the conversation. The analysis should be conducted by a third-party, who is an expert at picking small companies to invest in. They should analyze the conversation between the well-known investors and try to poke holes in their analysis. They should be as detailed as possible and ultimately give their own assessment based on both the feedback of these key investors and the information they know about the company from the annual report

I tried the above, and had interesting results — but I leave it as an exercise to the reader instead of posting the outputs here. Because ultimately, the best way to truly learn about these tools and what they are capable of, is to use them. As I’ve said before — if you are curious about how LLMs can help you: **Just Get Started**

Need help with these technologies? Curious but not sure where to start? Think your company could use some help? Send me a note: mattstockton@gmail.com

### Prompt Inputs / Output

I built a PDF that contains some of the inputs and outputs I mentioned above, you can download it here:
- [Stock Research Inputs and Ouputs](/docs/assets/pdfs/stock_research_llm_inputs_outputs.pdf)

### Disclaimer

The content provided in this post is for informational and educational purposes only and should not be construed as financial or investment advice. The opinions and analyses presented are those of the author and do not constitute recommendations to buy, sell, or hold any securities or investments. Please consult with a qualified financial advisor or conduct your own research before making any investment decisions. Investing involves risk, including the potential loss of principal.