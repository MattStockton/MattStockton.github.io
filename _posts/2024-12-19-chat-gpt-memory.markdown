---
layout: single
title: "A Thought Experiment with ChatGPT's Memory"
excerpt: "I tested ChatGPT's memory with prompts designed to uncover hidden narratives, sparking questions about how it generalizes insights. This post explores the experiment, potential uses for memory embeddings, and how o1 pro helped brainstorm new ways to analyze patterns in stored interactions."
category: "Building with LLMs"
tags: ["chatgpt-memory", "experiments", "embeddings", "o1-pro", "ai-behavior"]
---

One corner of AI Twitter that’s been catching my attention is where people share prompts designed to get ChatGPT to reflect on specific things about you. These prompts go beyond simple questions, often aiming to uncover deeper insights or patterns. An example that stood out to me was a prompt asking ChatGPT to find your “hidden narrative” or “subtext.” It instructed ChatGPT to dig deeper, unpacking layers until there was nothing left to uncover. You can see the [full prompt here](https://x.com/heyalexfriedman/status/1866175362813595944).

I tried it. I wont share the results, but they were compelling and made me think about myself and the technology. The answer it gave felt deeper than just a reflection of the entries in my ChatGPT memory log. It made me consider how things might work under the hood. While memory likely played a role, some of the perceived depth may come from the model’s ability to generalize and extrapolate patterns.

## What’s Happening Behind the Scenes?

My guess is that ChatGPT’s memory function plays a central role in how this works. When memory is enabled, ChatGPT stores a running list of distilled facts and observations about you. I haven’t dug into the technical details, but it's likely the system retrieves these “memory sentences” and uses them as context when crafting responses.

When I checked my memory log, it had ~100 entries. Some were straightforward facts:

- *“Has worked at two hedge funds, including a global macro fund, where they built out data infrastructure.”*

Others were observational:

- *“Believes in the concept of the data flywheel, where the data collected by a product or application is used in smart, transparent, and easy ways to improve the large language model.”*

Then there were casual ones:

- *“Was just shark tooth hunting near Wilmington, North Carolina beaches.”*

These entries seem to be synthesized into concise representations of who I am — or at least what ChatGPT has inferred about me. But the response to the “hidden narrative” prompt felt like it went beyond this. It didn’t just seem like a regurgitation of memory entries, which made me wonder whether there’s something more complex happening. It’s possible this depth came from the model’s broader ability to recognize patterns and generate insights based on its training, rather than something specific about the memory mechanism.

## What Could You Do with These Memory Sentences?

This led me to a thought experiment: what if we took these memory sentences, summarized or distilled them further, and turned them into sentence embeddings (numerical representations of meaning)? What could you do with them? Something like this likely wouldn’t ever be a publicly facing thing — people would understandably be uncomfortable with the idea of embeddings generated from personal data being analyzed or compared across users. But as a hypothetical exercise, it’s interesting to consider.

You might:

1. Compare embeddings to identify similarities or contrasts between individuals.  
2. Group or cluster embeddings to discover shared patterns or themes.  
3. Explore relationships by manipulating vectors — adding or subtracting embeddings to see how different attributes interact.

While this is entirely hypothetical, it’s worth emphasizing that even in a research setting, implementing something like this would come with significant ethical and technical challenges. Beyond privacy concerns, it may not be straightforward to analyze embeddings in a way that’s meaningful without potentially introducing biases or misinterpretations.

## Brainstorming with o1

For exploring rabbit holes like this, I find it’s fun to throw ideas at a language model. Unlike people, it doesn’t dismiss concepts as unrealistic or unfeasible — it just works with you, building on what you suggest. With this in mind, I started playing around with the idea with o1.

The prompt was essentially:

- ChatGPT keeps memory entries — distilled sentences summarizing user interactions.  
- What if these were turned into embeddings?  
- How might combining, comparing, or analyzing these embeddings across users unlock new insights?

The ideas that came out ranged from silly to surprisingly thoughtful. Some were impractical, but others sparked new ways of thinking about embeddings and their potential applications. For example, one suggestion involved creating a kind of “group fingerprint” from aggregated memory embeddings, which could then be compared to other groups.

I made a few follow-up prompts and iterated a bit as well.

It's fun to use an LLM like this to augment the creative process. The language model acts as a brainstorming partner that builds on your thoughts without judgment, and that’s what makes it so valuable for exploring ideas like this.

## Reflections

This experiment reinforced two things for me. First, prompts like “tell me about me” aren’t just interesting for their answers — they hint at the ways systems like ChatGPT build and use memory. Second, using a language model as a brainstorming partner can unlock creative ideas that might not surface otherwise. Even with wild or impractical concepts, the process itself keeps the creativity flywheel turning.

If you’re curious, the list of use-cases o1 generated is below. Even as a hypothetical exercise, it’s worth exploring what these systems might be capable of.

## o1's Ideas For Using The Embeddings

1.	“Conceptual Mashups” for Inspiration:
By taking embeddings from distinct users or different conversation topics and blending them, you could create entirely new, synthetic “user personas” or thematic intersections. For example, combining embeddings of a user deeply interested in astrophysics with those of a user focused on ancient mythology might produce a novel perspective to generate creative sci-fi story ideas or interdisciplinary insights.

2.	Archetype Prototyping for Product Development:
Instead of building personas the traditional way, you could use these embeddings to form data-driven archetypes that represent extreme or niche user segments. Product teams could then stress-test their features against these unconventional user archetypes to discover blind spots in design, marketing approaches, or user support strategies.

3.	Detecting Latent Cognitive Biases Over Time:
If a user’s embeddings steadily shift to cluster around certain hot-button terms or conceptual frames, it might hint at emerging biases or echo-chamber effects. The system could flag these subtle shifts in conceptual orientation, gently prompting the user to encounter counter-arguments or neutral resources to maintain a more balanced understanding.

4.	Generating “Inverse Queries” for Self-Reflection:
By taking a user’s embedding and applying vector arithmetic to find a conceptually opposite or orthogonal embedding space, you can synthesize “inverse queries”—questions or topics the user would never normally ask. Presenting these inverse queries might spark new lines of thinking, helping users break out of cognitive ruts or expand their intellectual horizons.

5.	Embedding-Driven “What-If” Scenarios:
Using embedding manipulation, you could answer hypothetical queries like, “How would this conversation have evolved if the user approached the topic from a completely different angle?” By subtracting the user’s current conceptual cluster from another user’s cluster (or from a known reference embedding), you can produce alternative explanations or answers that simulate a parallel reality—allowing the user to glimpse how changing assumptions would alter outcomes.

6.	Subtly Adaptive Tutoring Paths Based on Micro-Shifts:
Instead of waiting for overt signals of confusion, the system could track micro-shifts in embeddings to detect when a learner’s conceptual framework starts to wobble. If slight deviations are detected, the system can intervene early with targeted analogies, re-explanations, or incremental exercises, preventing misunderstandings from solidifying.

7.	Cross-User “Cultural Exchange” Programs:
In a multilingual or cross-cultural setting, embeddings could highlight where two sets of users converge or diverge in conceptual understanding. Facilitating direct exchanges—like pairing a user strong in “eastern philosophical concepts” with a user well-versed in “western scientific reasoning”—could yield enlightening dialogues, bridging conceptual gaps and fostering mutual understanding.

8.	Creative Prompt Generation for Brainstorming Sessions:
For creative professionals or teams, embeddings can be strategically combined or perturbed to generate “jolts” of inspiration. For instance, identifying embeddings that are far from the user’s comfort zone can produce prompts that kickstart ideation sessions, helping break creative blocks by nudging the user into unexplored conceptual territory.

9.	Highlighting “Forgotten Paths” in Long-Term Interactions:
Over months or years of user interactions, certain once-important concepts might drift away as the user’s interests move on. By analyzing the user’s historical embedding space, the system can periodically resurface these “lost threads”—old concepts that once engaged the user, prompting reflection on how their perspective has changed and whether revisiting old interests might be fruitful now.

10.	Dynamic Group Brainstorms with Embedding Synergies:
In collaborative environments, the system could detect when two or more participants’ embeddings would produce an unusually productive synergy if combined. The system might suggest pairing User A (who excels at strategic thinking) with User B (who is conceptually strong in tactical detail) and User C (with a knack for metaphorical bridging) to tackle complex interdisciplinary problems, essentially using embeddings to engineer high-performing teams on the fly.