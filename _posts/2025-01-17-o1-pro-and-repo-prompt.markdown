---
layout: single
title: "Repo Prompt and prompting for o1 pro"
---

Here's a video I made demonstrating a tool called [**Repo Prompt**](https://repoprompt.com/). At its core, Repo Prompt automates the process of injecting local files into the context window for models, making it especially valuable for coding tasks. It helps you structure prompts that guide models to produce usable, structured outputs and even enables workflows like generating diffs you can apply directly to your files.


<iframe width="560" height="315" src="https://www.youtube.com/embed/VPuYI7Oz_hI?si=3tDbMvA91mFaSM3c" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<br/>
Repo Prompt fills an important gap for o1 pro. Since o1 pro isn’t available via API or integrated into tools like Cursor, Repo Prompt allows you to automate prompt construction and avoid the manual process of copying and pasting from your docs. In this demo, I used Repo Prompt in a different way: injecting context from my blog posts into a prompt to distill and summarize across them. While this isn’t a typical use case, it highlights how Repo Prompt can also support non-coding workflows by streamlining prompt creation.

## Key Takeaways
### Using Models for Meta Prompting
I demonstrate how I like to use LLMs for meta-prompting. This involves asking the models to act as prompt generators. I also generally do this using voice input — so instead of typing out the instructions, I’m just talking to the models, which is a seamless way to interact with these tools. It saves time and, in my view, doesn’t compromise the quality of output even if the transcription is unpolished.

### Structuring Effective Prompts for o1 pro
In the video, I use meta-prompting to generate a well-structured prompt for o1 pro, following guidance I read about on Twitter and in a [*Latent Space* blog post](https://www.latent.space/p/o1-skill-issue). This method emphasizes creating prompts with a clear:  
- **Goal:** What you want the model to achieve.  
- **Return Format:** The specific format you expect in the output.  
- **Warnings:** Instructions on what the model should avoid.  
- **Context Dump:** As much relevant information as possible to guide the model.  

Unlike earlier models, which benefited from iterative back-and-forth conversations, o1 pro already has chain-of-thought reasoning embedded. This means it performs best when you front-load all the necessary context into the prompt. The video walks through how I applied this structured approach.

---

Be sure to check out the *Latent Space* blog post for more details on prompting o1 pro, as well as the demo videos on Repo Prompt available on their website and from users posting on Twitter. Both resources are incredibly helpful if you’re trying to understand how to get the most out of o1 pro or even to figure out what it’s best suited for.