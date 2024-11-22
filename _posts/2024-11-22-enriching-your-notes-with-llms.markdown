---
layout: single
title: "Learning with LLMs: Using Quick Notes to Guide Better Summaries"
---

In my [previous post](/2024/11/22/self-guided-learning-with-llms.html), I shared how I use LLMs for self-directed learning. Here's an example that shows a different approach: using rough notes to guide an LLM in summarizing what you find most interesting from a larger text. While my previous post focused on summarizing technical topics, this time I used brief notes to help guide the model to extract and organize precisely what I wanted from a long interview.

The same Lex Fridman podcast included an interview with [Amanda Askell](https://askell.io/), a philosopher at Anthropic. While she covered many topics, I was drawn to her insights around effectively prompting LLMs. As someone who has had more conversations with Claude than perhaps anyone else at Anthropic, her insights on prompting caught my attention. Here's how I captured / processed this information:

1. Given this was a lengthy podcast, I listened to it across several runs. While running, I would jot down things I found interesting on my phone. These notes were rough and abbreviated — barely legible given I was in motion. They weren't comprehensive, just quick captures of key ideas that stood out. For example, one note read "Ask the model - why did you do that?" — a shorthand reminder of Amanda's point about questioning model responses.

2. After my run, I realized my notes weren't organized or legible. Rather than trying to decipher them or refine them myself, I tried a different approach using an LLM.

3. I located Amanda Askell's segment from the podcast transcript and saved it to a text file.

4. Using Gemini 1121 (Google's latest version released this week), I asked it to create an organized summary of the interview — specifically focused on topics from my terse, unintelligible bullet points. This way, the summary would be structured around what I found interesting, even though my original notes were rough.

5. The LLM did a nice job creating an organized summary that focused on the key points I cared about.

6. Amanda's interview was rich with prompting suggestions throughout the discussion - I wanted to extract these into actionable advice. Using the previous summary as a base, I asked the model to distill her insights into a concise list, with each recommendation limited to 2-3 clear sentences.

The result was what I needed — a clear list of prompting techniques that I can reference when working with LLMs. With very little prompting effort, I ended up with the format and content I wanted. The final output was significantly more useful than my original notes while still reflecting what I found interesting about the discussion.

The key takeaway here is the flexibility of these tools — you can remix and adapt them to work for you, and they don't need much input to get started. The essential ingredients are iteration, curiosity, and simply getting started. There's no single "right way" to use them for learning.

You can find the LLM-generated (but Matt-guided) summary of Amanda's interview [here (PDF)](/docs/assets/pdfs/podcast_summary_anthropic.pdf). Below are the key prompting techniques the LLM distilled as well:

### Prompting Techniques

*Iterate and Refine:* Prompting is an iterative process. Test, analyze, and refine prompts repeatedly based on model responses until the desired behavior is achieved. Don't expect perfection on the first try.

*Empathize with the Model:* Consider the prompt from the model's perspective, anticipating ambiguities. Imagine reading the prompt for the first time and ask, "Would this make sense to me?"

*Define Clearly, Philosophically*: For subjective or complex tasks, adopt a philosophical approach to prompting. Define concepts precisely, specifying criteria for desired behaviors, especially for nuanced concepts like "rudeness" or "politeness."

*Consider Edge Cases:* Explore the boundaries of the desired behavior. Test edge cases to ensure proper generalization and incorporate successful examples into the prompt.

*Leverage Advanced Techniques:* Generate prompts with prompts. Ask the model directly for suggestions on prompt improvement, creating a dynamic feedback loop.

*Balance Prompting and RLHF:* Understand the interplay of prompting and RLHF. Prompting elicits specific behaviors while RLHF shapes broader model behavior based on human preferences. Use both strategically.

*Be Mindful of Trade-offs:* Prompt adjustments change the error profile of the model. Emphasizing politeness might reduce bluntness but increase apologies. Carefully consider these trade-offs.

*Unlock Creativity with Explicit Prompts:* For creative tasks, move beyond basic requests. Explicitly prompt for creativity, expression, and originality to unlock the model's full potential, avoiding generic or "average" outputs. Encourage the model to "think outside the box."

*Provide Context and Examples:* Whenever possible, enrich prompts with relevant context and concrete examples of desired outputs. This helps guide the model towards the intended behavior and reduces ambiguity.

*Experiment with Different Prompting Styles:* Don't be afraid to experiment. Try various prompting styles – more instructive, more conversational, more suggestive – to find what works best for eliciting the desired response from the specific model you are using.

---

*Note: I specifically chose to use Gemini for this task as part of my ongoing experimentation with different AI models. Each model has its strengths, and part of effective learning is figuring out which tools work best for different tasks.*