---
layout: single
title: "Investing With Language Models"
excerpt: "Verdad used LLMs to analyze thousands of Japanese company reports, categorizing their valuation plans and linking them to stock performance. This kind of structured analysis — translation, summarization, and categorization —  is exactly where LLMs shine. We’re just getting started."
---
How we can use information found in unstructured data to drive investment ideas is an area I’m really interested in. When used appropriately, language models can be great at summarization and categorization tasks. For those who want to build a better mental model of ‘what LLMs are good at’, I highly recommend [Andrew Ng’s Prompt Engineering course](/2024/05/07/prompt-engineering-quickstart.html) or just take a spin through this [Prompt Engineering Guide](https://www.promptingguide.ai/)

I’ve written a few pieces about how we can use LLMs for investing over the last few months. One example I am excited about is leveraging long context windows to process [unstructured company reports](/2024/08/13/gemini-long-context-window.html). Another example is the ability to spin up tools to [visualize economic data](/2024/06/24/economic-dashboard-with-claude.html), without needing to know how to code. 

Today, I saw a really compelling use case, highlighted by [Verdad in their newsletter](https://mailchi.mp/verdadcap/activism-at-scale-in-japan?e=d672c968ec). It’s a quick read so I encourage you to read it in full — but in summary:

### Verdad Overview / What They Did

1. Japanese stocks have been undervalued for a long period of time, using standardized financial metrics like Price / Book. The drivers behind this are numerous and detailed. That’s a book in and of itself.
2. The Japanese government and stock exchanges have an interest to change this (lots to be read on this as well) — and took action, requiring companies to define their plans to increase company valuation.
3. Thousands of companies submitted plans on what they will do to increase valuation.
4. The plans submitted by companies — although likely structured differently — have a finite set of ‘menu options’ that range from ‘passive / do nothing’ to something more assertive and meaningful (e.g. allocating a specific dollar amount for dividends and repurchases)
5. Verdad used Language Model tools to:
    1. Scrape, extract, and summarize information from the several thousand reports submitted to the stock exchange
    2. Determine the type of action planned by each company (e.g. do nothing, repurchase shares, issue dividends, sell strategic holdings)
    3. Assess the ‘robustness’ of the claim by the company (for example: is the repurchase plan actually meaningful in $ amount compared to company market cap?), and use this robustness to potentially re-categorize (e.g. if the company says it’s going to re-purchase, but the plans are too high-level, don’t give them ‘credit’ for being in this category)
    4. Build a final categorization of the several thousand companies, and calculate the average stock return for each company in each category since the plans were filed

### Verdad's Findings

Not surprisingly, the companies with the most detailed and robust plans had the highest average returns. The companies who failed to disclose or lacked clarity in their actual plan had the lowest average returns. In hindsight, this result seems really predictable.

### Why It Matters

So why does this matter? Because you could easily imagine **having this investment hypothesis on day 1, when the above reports were submitted**. It’s not a far leap to think that companies with **more specific and detailed plans to increase valuation** might perform better than companies that just say ‘we’re not sure yet.’  So if you had this hypothesis on day 1, and wanted to invest on it, how would you do it? This is why Language Models are so interesting. When orchestrated appropriately, Language Models can be great at the following, and can do them incredibly quickly:

- Translation
- Summarization
- Categorization

These are exactly the 3 core steps that Verdad had to do in this analysis. Perhaps the companies in the highest returning bucket (e.g. ‘selling cross-share and strategic holdings’) could have been identified as soon as the reports were submitted. The average return is meaningful — the top bucket is 56%, the bottom bucket 21%

### Where We Go Next

Before Language Models, you could have done this type of analysis (it’s not impossible) - I just think it would have taken a ton more time and would have involved a lot of manual / tedious work. I am not sure how long this analysis took, but if I had to place a bet, I think the ‘time-to-value’ here is a lot shorter than most people think. These models can be incredibly good at extracting information from large unstructured data, given good prompting techniques. You could imagine going a step further here as well — after identifying the companies with the most detailed and actionable plans, you could prompt the Language Model to do a discrete ranking of the companies based on some other investment hypothesis you wanted to mix in. There are so many other ways to augment this core idea.

I think we’re just scraping the surface of how we can apply these technologies, and it’s super-fun to see folks like Verdad using these tools, and getting meaningful / interesting results. What are you building? What are you interested in related to AI and Language Models? How can I help you? Reach out at mattstockton@gmail.com