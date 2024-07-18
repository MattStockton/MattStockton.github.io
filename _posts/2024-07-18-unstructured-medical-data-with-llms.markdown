---
layout: single
title:  "Exploring my unstructured medical data from PDFs with Claude"
---


<img src="/docs/assets/images/medical-data/1.png" width="600px" height="600px"/>

### TLDR 

I want to share something interesting I’ve been playing with recently. I've been experimenting with LLMs to build user interfaces for unstructured data. This experiment also got me thinking about how LLMs might be useful in the medical field (when used appropriately and with strong human guidance / human oversight).

Using Claude, I built a small web application to explore my recent blood test results. I uploaded a set of unstructured PDF test results exported from MyChart, and worked with Claude to make sense of it. Want to check out the tool? [Here's the link](https://claude.site/artifacts/2f3789fb-655a-45fb-8e67-f53d983b25b3)

### Video Walk-Through

<iframe width="560" height="315" src="https://www.youtube.com/embed/fkxh_xwzFdg?si=Lco4lZpP78qCYu0M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Making Sense of Unstructured Data

If you’ve ever had to deal with unstructured data -- whether in PDFs, Word docs, raw text files, or something else -- you know how messy and time-consuming it can be to make sense of it all. LLMs are particularly well-suited to help you extract structured information from these sources. LLMs can help structure, distill, and summarize unstructured data, turning a jumbled mess into something you can actually work with and visualize using analytical tools.

A few weeks ago, I had my yearly physical and got a bunch of blood tests done. I was curious to see if I could use Claude to help visualize and analyze my results. The tools within MyChart are OK -- but are fairly basic and not exactly user-friendly for looking at time-series information.

As an experiment, I downloaded a few of my recent test results as PDFs and fed them into Claude. I asked Claude to build me an interactive tool to explore my test history. I also gave it some basic information like my age and gender, and hit go.

As refererence, below is a small excerpt from one of the PDFs. The PDFs have varying formats -- depending on the test, and depending on what year the test was done

<img src="/docs/assets/images/medical-data/3.png" width="600px" height="600px"/>


### How Claude Did

With limited prompting, Claude generated an application that let me visualize my test results over time. It flagged abnormal values and provided general health insights about the results. The entire process took five minutes, and I didn’t need to do any heavy lifting. It was amazing to see how quickly and effectively it transformed my raw data into something useful. I imagine I could drastically improve the outputs with a bit more effort in the prompt. Here is the prompt I used:

>I want you to build me an interactive tool for exploring my medical test result history. Here are some details on what I am looking for.
>
>   - I will attach several PDFs that contain various test results and diagnostic levels
>   - I want to be able to explore this data interactively in the browser
>   - I want the tool to highlight any abnormalities
>   - I want the tool to highlight any recommendations that I should take action on
>   - I want the tool to be creative in nature. The way I explore this data should be differentiated and unique compared to how one might explore this data normally.
>   - I want the tool to take into account any additional public data or relevant information for a 41 year old male.
>
>Feel free to ask me any questions you have first.

Here's an additional screen-shot from the application it built:

<img src="/docs/assets/images/medical-data/2.png" width="600px" height="600px"/>


### Expanded use-cases in the medical field

This experiment got me thinking about how LLMs can be used more broadly in the medical field. Below are some high-level concepts that are interesting to me

- Analyzing Personal Medical Records: LLMs can help you analyze your personal medical records, making it easier to spot trends and anomalies over time.
- Incorporating Medical Research: They can also relate your personal data to the vast amount of medical research out there, potentially providing insights that you or even your doctor might not have considered.
- Identifying Non-Obvious Patterns: LLMs are capable of finding patterns in large datasets that might not be immediately obvious.
- Visualizing Data Easily: With minimal coding, LLMs can help you visualize data in unique and helpful ways.
- Quickly Building Interfaces: LLMs can help you rapidly create user interfaces for unstructured data, saving time and effort.
- Empowering Personal Data Exploration: LLMs help you to explore your own data without needing specialized tools or skills.

### Why I Think This Matters

With the help of LLMs, individuals can take a more active role in understanding and managing their own data, even if their only access to that data is via an unstructured format. Experimenting with tools like this isn't a replacement for enterprise-grade tools or medical professionals -- but I think it unlocks really interesting ways to bridge the gap between personal data and the wealth of medical knowledge available. I also think we'll see more of this technology appled to existing tools in the space, and we'll certainly see competitors building tools to capture markets where existing tools are slow to catch up. 

### Final Thoughts

My advice is pretty consistent when it comes to LLMs. **Just try it out for something you're working on, and see what happens.** Whether it’s Claude, ChatGPT, or another LLM - the only way to learn about what they are good at is to try something. As always, I’m keen to hear about your experiences and what you’re working on. Feel free to reach out!
