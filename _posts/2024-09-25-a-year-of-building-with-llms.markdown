---
layout: single
title: "A Year Of Building With LLMs - The Paper You Need To Read"
excerpt: "If you’re serious about building with LLMs, read 'What We’ve Learned From A Year of Building with LLMs.' It’s packed with lessons on prompting, retrieval, evaluations, and real-world deployment. My notes summarize key takeaways, but the full paper is worth your time."
---

If you have an hour, click the below link and then just close out my website. If you don't have an hour, you can read below, but it wont be as good.

[What We’ve Learned From A Year of Building with LLMs](https://applied-llms.org/)

The above paper is such a fantastic paper that I am almost hesitant to post my summary notes. It’s well-worth your time to read the paper itself, and you’ll get much less value from my very rough bullet-points below. But I’ve found I get a lot more personal value and information recall when I take notes, and if I have the notes — why not share them here?

I am grateful to all of the authors of this paper for sharing their hard-won insights for free, in public. This paper is super-approachable, yet only takes an hour or so to read. If you’re technical and looking for a hook to dig into LLMs more deeply, this is the way.

### Take-aways

- Learn how to prompt effectively. If you learn anything, learn about “N-shot prompting” (which is really just providing examples inline), and “Chain Of Thought” (which is really just providing a detailed list of steps you want the LLM to take, sort of like you would to a brand new college grad at your company)
- Structure and label your prompts. Typing a big paragraph wont work as well as labeling different parts of your query. Providing some background information and then a source document? Label it as such using headers within your prompt
- Keep prompts small, focused on one task. Just like in traditional software, break things into chunks that do one thing. If your prompt is doing a lot of things, break it into multiple prompts
- There’s this famous quote that I just looked up. I hope it’s correct. It’s good advice for writing prompts. Just because it’s a computer, doesn’t mean it wants all your extra fluff: *Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away*
- There are some really naive ways to do RAG, and you shouldn’t ignore tried-and-true retrieval techniques like keyword-based search, even if it’s really ‘old’ technology. Vector embeddings are really cool and useful, but have their failure modes, and are best used *along with* techniques like BM25, not as a replacement for it.
- Fine-tuning is useful, and is getting easier and cheaper to do — but really refining your prompts, attempting RAG, and checking different models — is usually a better place to start. Also, you need to have a systematic way to evaluate your prompt’s effectiveness. Don’t just type stuff into the UI, look at the outputs, and assume it’s going to work well for all cases.
- Long context windows are really cool, but it’s not an excuse to be diligent about what you put in the window. Just because you add more stuff doesn’t mean the result is going to be better. Also, stuffing the context full is going to make things slow at inference time.
- This is a bit of a repeat, but it’s really good advice. Break problems down into units, and design your system around those units. I loved this quote from the paper:
    
    > The most successful agent builders may be those with strong experience managing junior engineers because the process of generating plans is similar to how we instruct and manage juniors. We give juniors clear goals and concrete plans, instead of vague open-ended directions, and we should do the same for our agents too.
    > 
- You need to test your prompts. The baseline is sample inputs and outputs, with unit-test-like assertions. Just because the output is unstructured text doesn’t mean you cant build meaningful assertions and automate their execution.
- LLMs can be used for testing as well (e.g. feed the inputs / outputs of a prompt into another prompt that ‘judges’ how good the output was). This is a valid approach, but there’s some diligence you need to apply to the judge prompt, and you should dig into the valid techniques here.
- LLMs seem like magic, but they aren’t. If you’re asking it to do something that an intern couldn’t do with the data you gave it, then you might need to revise your approach.
- Feedback loops in your system are an absolute necessity. Figure out a way to get your users to label and provide feedback on your outputs. Also, having a user compare two things (e.g is A better than B?) is more reliable than asking them to rate something (e.g. rate A on a scale of 1-5)
- LLMs will almost never say no, even when we want them to. This is where you can get into the most trouble with them making stuff up, so test your systems accordingly. Build it into the evals.
- Log your prompt inputs and outputs - You’re going to want to look at your data, and you need the lowest-level data  - so orchestrate your system such that you have easy access to the actual API inputs and outputs - and then look at it.
- Look at your data - This is almost a meme at this point. But it’s true. It’s not always fun, but — look at your data, see what looks good, see what looks bad — stare at it for a while, and then figure out what’s going wrong and what you need to change.
- There are some really good ways to get models to return structured outputs like JSON. [Instructor](https://github.com/jxnl/instructor) is an awesome library to do this, and it’s really easy to integrate
- You can’t just change models, even if it’s a model upgrade. Things break. Stuff that used to work breaks, and vice-versa. This is why you need a systematic way to test your prompts. You should be able to swap out the model, and then have a quantitative view on *how* this new model affects your specific use-cases’ performance. If you don’t have that, you gotta get there. There are some really light-weight tools that are easy to start with for Evals, like [PromptFoo](https://www.promptfoo.dev/)
- Inference is getting cheaper, but it’s not free. It’s worth experimenting with the smallest model that gets the job done.
- You cant just let LLMs go wild, they need some help from people. The best experience right now is a Human In The Loop approach. This means that you find the most seamless, least friction, most valuable way to integrate the LLM capabilities into the user’s application experience. Without duplicating a bunch of stuff here, [this part of the paper gives a great example](https://applied-llms.org/#design-your-ux-for-human-in-the-loop)
- Like anything you’re building, you gotta know what your priorities are. You can’t have everything, and if you think you can — you’re gonna build a bad product. Interesting priority dimensions to consider for LLM products are: Reliability, Harmlessness, Factual Consistency, Usefulness, Scalability, Cost
- Process over Tools - There are like 1000 new tools being launched every day in this space. So many shiny objects. But what are you really trying to do? What problem do you need to solve? Ignore the shiny objects and solve the problems, in the most pragmatic way possible.
- Experimentation is more necessary than ever. We’re all still figuring out how a lot of these models really work — so sometimes you need to go wide to figure out the best approach. The best way to do this is to have systematic ways to test your experiments (got evals? or no?  go get them…)
- Get everyone involved across the entire org. Domain expertise has never been more valuable. Now that the form factor for instructing computers is just english, many more people at your company can do it. Show them the way, don’t gate-keep. This is how your team will win.
- Don’t build something that is everything to everyone - it’ll be nothing to no one instead. Find a niche and crush that niche first - I think this is true for any software product, but probably more true for LLMs, because if you reduce the quality of the response by expanding the target use-cases, it becomes apparent very quickly. Focus is everything. Find your beach-head first, and make it awesome.
- Look for tools you can assemble, don’t build them yourselves - There are so many great building blocks in this space - treat them like legos — don’t become a lego factory. What’s your core value proposition or defensible moat? Make sure you’re building that, not a thing someone else is better at building. Just use their stuff.
- Prompting and Evals and In-Application Data Flywheels - This is where to focus your time.