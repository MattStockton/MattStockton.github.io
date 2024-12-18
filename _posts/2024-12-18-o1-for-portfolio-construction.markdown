---
layout: single
title: "Trying Out O1 for Portfolio Strategy Generation"
---

OpenAI recently released their O1 model, and I’ve been following the early feedback closely. [A tweet from Deedy Das](https://x.com/deedydas/status/1869049071346102729) caught my attention, stating that O1 Preview is “far superior to doctors on reasoning tasks, and it’s not even close.” If that’s accurate, it’s a remarkable milestone. I’ve been eager to experiment with O1 and had an idea that aligned with my interests in portfolio construction and systematic investing, givine me a nice opportunity to dive in.

One of my favorite sources for portfolio research is [Verdad](https://verdadcap.com/), led by Dan Rasmussen. Their work consistently presents systematic ideas in an accessible way. This week, they published an article called *Persistent Alpha* ([read it here](https://us13.campaign-archive.com/?u=6dc62f307511d466ff78a94fe&id=fdcea4b391)), exploring whether you could build a portfolio by rotating into ETFs with strong historical alpha. Their backtest results suggested this approach could replicate some of the performance advantages hedge funds achieve when allocating capital to their top-performing teams. 

This concept struck me as a compelling challenge to test using O1. Could I use O1 to generate new strategies inspired by Verdad’s concept? To test this, I used a metaprompter built with GPT-4 to craft a detailed prompt for O1. I then provided O1 with Verdad’s article for context and asked it to generate a set of similar strategies. The goal was to explore whether O1 could brainstorm similarly structured yet novel portfolio construction ideas in a systematic and efficient way.

The result of this experiment was a [document of eight generated strategies](/docs/assets/pdfs/portfolio_construction_strategies.pdf), each inspired by the core ideas in Persistent Alpha. These strategies represent potential variations that could be worth further investigation or backtesting. In this post, I’ll walk through the process I used to produce these results, from crafting the prompt to reviewing O1’s output, and share my thoughts on what I learned along the way.

## The Process

Here’s how I approached the project:

### 1. Understanding Verdad’s Idea

Verdad’s [Persistent Alpha article](https://us13.campaign-archive.com/?u=6dc62f307511d466ff78a94fe&id=fdcea4b391) introduced the idea of systematically allocating capital to ETFs with strong historical alpha. I appreciated the simplicity and structure of their approach and wanted to see if I could generate related strategies that expanded on the same concept.

### 2. Understanding How to Prompt O1

O1 requires a much different prompting style than earlier versions of OpenAI’s large language models. It’s been trained and tuned with reinforcement learning on chain-of-thought reasoning, so understanding how to structure your prompts is critical to getting meaningful outputs. I came across [a tweet about building a metaprompter for O1](https://x.com/mattshumer_/status/1866159172657786980), which outlined a method for crafting prompts tailored to this model. This was great to ensure I could communicate my goals effectively to O1. It also allowed me to short-cut learning about the best techniques for prompt building with O1.

### 3. Using GPT-4 to Build the Prompt

I executed the above prompt, and described my goals to GPT-4 in simple terms, explaining Verdad’s approach and what I wanted to accomplish. Specifically, I asked GPT-4 to help me generate 5-10 strategies inspired by Verdad’s systematic approach. Here’s the exact text I narrated to create the prompt. Yes, this is just me talking to ChatGPT

> So I came across this article from Verdad Capital called Persistent Alpha, which describes a portfolio construction strategy where they look at ETFs and they measure the alpha over a historical time period, and they basically rebalance into the high alpha funds, like the top decile of high alpha funds. And the article makes the argument that this is like sort of what the pod shops are doing, like the hedge funds, where they have a bunch of siloed manager teams and they kind of rebalance into the teams that are generating alpha. And so, you know, basically what this article says is that if you kind of measure, they did a back test, right, where they measured the alpha over a historical period and then rebalanced, or looked at like forward alpha for one month, six month, and 12 month looking periods. And then they looked at a performance, basically they simulated a public pod shop strategy where they rebalanced into the top 10% of funds ranked by trailing 12 month alpha. I thought this was really interesting and I want to identify maybe like five to 10 similar derivative strategies, like related strategies that I can consider testing to see how they perform, kind of with the same essence of what this paper describes. And I will attach the paper to the prompt when I send it to O1.

### 4. Sending the Prompt to O1

Using the detailed prompt generated by GPT-4, I attached the full Verdad article to provide additional context and sent everything to O1. Here’s the prompt I sent to O1 (which was generated in step 3 above)

```
<task>
    Identify 5-10 derivative portfolio construction strategies inspired by the essence of the "Persistent Alpha" strategy outlined in the attached article. The key characteristics of the original strategy are:
    - Measuring historical alpha of ETFs over a defined time period.
    - Rebalancing into the top decile of funds ranked by trailing 12-month alpha.
    - Simulating a "public pod shop" approach, where allocations are adjusted to prioritize consistently high-performing funds.

    <context>
    The strategy should involve a systematic and repeatable methodology for identifying and reallocating to outperforming assets. Consider variations that:
    - Use alternative metrics or signals (e.g., Sharpe ratio, volatility-adjusted returns, momentum).
    - Explore different asset classes or fund types (e.g., mutual funds, individual stocks, sectors).
    - Employ alternative rebalancing periods (e.g., quarterly, monthly, semi-annually).
    - Incorporate risk management layers or constraints to mitigate concentration risk.
    - Investigate dynamic thresholds or ranking mechanisms for fund selection.
    - Leverage forward-looking factors, such as earnings growth or sentiment, in addition to historical performance.
    - Simulate adaptive strategies that adjust based on market conditions or macroeconomic factors.

    Include clear, actionable descriptions for each derivative strategy, ensuring they are distinct and testable. Focus on preserving the systematic nature of the original approach while introducing creative and meaningful variations.
    </context>
	<article>
		<!-- ACTUAL ARTICLE ->
	</article>
    <end-state>
    For each strategy, provide a detailed one-pager that includes:
    - **Strategy Overview**: A comprehensive explanation of the strategy and its core mechanics.
    - **Rationale/Viewpoint**: The underlying viewpoint or hypothesis of why the strategy might be beneficial, including links to the original "Persistent Alpha" approach.
    - **Implementation Details**: Step-by-step guidance on how to implement and test the strategy, including data requirements, selection criteria, and rebalancing methodologies.
    - **Testing Framework**: A detailed plan for back-testing or simulating the strategy, specifying metrics for evaluation (e.g., returns, risk-adjusted performance, drawdowns).
    - **Risks and Limitations**: A discussion of potential risks, weaknesses, and scenarios where the strategy may underperform or fail.
    - **Extensions/Variations**: Suggestions for further exploration or modifications that could enhance the strategy or make it more robust.
    - **Conclusion**: A summary of why the strategy is worth exploring and its potential fit within a broader investment framework.
    </end-state>
</task>
```

O1 generated eight distinct portfolio strategies. Each was clearly summarized, and while they varied in complexity, they all had enough structure to explore further.

### 5. Evaluating the Output

While I’m not skilled enough to evaluate the financial validity of these strategies in depth, I’ve built technology in this space and have a reasonable sense of what might work. Some of these strategies passed the “sniff test” and seemed logical enough to consider backtesting. This is one of the most exciting parts — seeing that a tool like O1 can help to create actionable starting points without a ton of effort is remarkable. Imagine what it could do with a bit more thought and instruction.

## What I Learned

The biggest takeaway from this experiment is that O1 has huge potential to change how we approach complex problems. It’s immensely capable, and getting started doesn’t require much time or effort. In just 15 minutes, I had eight structured strategies to consider. The barrier to entry for experimenting with this model felt low. I bet if I spent a few more hours tuning the prompts, I'd get much further.

I’m keen to continue exploring O1 and learning how it works. I’ve started working through a new training session from [deeplearning.ai](https://www.deeplearning.ai/short-courses/reasoning-with-o1/) on how to use O1 effectively. It's a mini-course that is about an hour long. I'm about halfway through - it's extremely informative but requires a lot of attention to follow. They get fairly deep in the weeds. I'll put together a follow-up post on what I learned from it. It seems like having the right mental model for when to use O1 - and how to use it - is extremely valuable.

## Links and Resources

Here are the key resources I used (or generated) in this experiment:  

- [Verdad’s *Persistent Alpha* Article](https://us13.campaign-archive.com/?u=6dc62f307511d466ff78a94fe&id=fdcea4b391)  
- [Tweet on Building a Metaprompter for O1](https://x.com/mattshumer_/status/1866159172657786980)  
- [PDF of the Generated Strategies](/docs/assets/pdfs/portfolio_construction_strategies.pdf)

## Final Thoughts

This was a straightforward experiment, but it showcased how powerful tools like O1 can be. The model’s ability to tackle structured, complex problems and produce meaningful outputs quickly is impressive. I’m excited to see where further experimentation leads, both with portfolio construction and other applications.  

If you’ve been exploring O1 or have thoughts on the strategies it generated, I’d love to hear from you. For me, this was a great first step, and I’m eager to keep learning and sharing as I go deeper.