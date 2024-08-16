---
layout: single
title:  "Inviting AI to the table - Building Software Edition"
---
I’ve written [in the past](/2024/08/12/ai-is-easy-just-get-started.html) on how I love Ethan Mollick’s idea of “always inviting AI to to the table”. He wrote the following in [this post](https://www.oneusefulthing.org/p/doing-stuff-with-ai-opinionated-midyear?utm_source=publication-search):

>*I know this may not seem particularly profound, but “always invite AI to the table” is the principle in my book that people tell me had the biggest impact on them. You won’t know what AI can (and can’t) do for you until you try to use it for everything you do.*

It’s energizing to come across people who are really trying to live this idea — particularly people that are building software. I was speaking with [Alex Bartling](https://www.linkedin.com/in/alex-bartling-993a877b/) recently, and he explained to me a way he and his team are using LLMs to help build software. The software itself is really incredible, and is making a huge positive impact for mental health professionals. It’s an AI-driven scribe tool to help providers optimize and structure the note-taking process. I am not well-versed in this space, but based on the customer-testimonials I’ve learned about, it is an incredible product. It fundamentally changes how a mental health professional can spend their time. It allows them to spend more time on the deep activities that really matter with their patients — and less time on operations and overhead. It’s a perfect use-case for Large Language Models.

But Alex and his team have gone far beyond using LLMs for its voice transcription and summarization capabilities. They are using LLMs to help customers adapt the product to their own needs, and are even using LLMs to help understand and categorize their customer’s most desired features. So how are they doing this? In two creative ways:

### Human In The Loop Prompt Feedback / Re-Execution

- When the product uses LLMs and prompting to create an output for the user, there is a step where the user can provide unstructured feedback on that output. The UI gives the user guidance on what feedback is helpful via a few structured examples —  but ultimately, the user can type in whatever they want.
- Then, the prompts are creatively re-run through the LLM with this extra guidance (with some good prompt engineering of course). So basically:
    1. Application has an initial prompt that incorporates the user data (e.g. transcribed audio)
    2. Application generates output via LLM and a chain of prompts
    3. User sees output, and provides feedback on that output via unstructured text with guidance in the UI
    4. Application re-runs prompt --with additional creative prompting and including the user’s guidance -- and updates the output
- You can think of this as allowing the user to behave as the ‘follow-up prompt engineer’ with some additional guardrails.

### Feedback Classification / Clustering via LLMs -> Product Feature Feedback Loop

What's more awesome is this aspect, which truly represents trying to "invite AI to the table." Alex and his team are periodically processing the unstructured feedback (step 3 above) at scale, and clustering it / classifying it using LLMs. From this, they can automatically see patterns in the feedback, and then they modify the software to allow the user to **select this feedback inline** versus having to type it in an unstructured text box. An example here might be clarifying:

1. The software receives 1000s of unstructured chunks of feedback from users. Let's hypothetically say a number of them are as follows:
    1. “I want the final text to be shorter”
    2. “This is too long of a note for section 2 of the document”
    3. “The output is too wordy”
2. The unstructured output is run through a creative prompt that is intended to distill the feedback into a taxonomy of feedback areas, ranked by frequency
3. From this, the LLM recognizes that a new toggle could be added to the UI, which has the label *"Summary Text Length"* and the following options.
    1. Brief
    2. Default
    3. Descriptive
4. The team updates the software with this new toggle, and ships the new version. Now the user can just click a button to provide the feedback next time (or even **select it before** the LLM runs the first time)

### What Alex Had To Say

Amazing stuff. If you have that background thread running of ‘how might AI help me here?’ you can discover some really cool things. I asked Alex to describe how he thinks about these concepts. I consider him to be on the leading edge of building software that uses AI and LLMs. Here’s what he told me below (I think he might have used ChatGPT to help him clarify his thinking — he is deep down the rabbit hole 🙂)

> The concept of “human in the loop” influences how users interact with AI-powered software. Unlike traditional software with heavily parameterized options, AI allows for unbounded, natural language instructions. However, this new interaction style can be confusing. Initially, when we provided a textbox for users to input additional context, they found it unfamiliar. To help, we introduced example prompts, which users often relied on at first. Over time, they realized they could say anything, creating a liberating and magical experience. 
>
> It’s interesting because, naturally, you start to collect all this unstructured feedback, which previously would have been challenging to make sense of. With AI, we can analyze and classify the text, extracting the most common “settings” to present to users in the UI.
>
> The role of a software engineer in the age of AI has evolved. Even before AI, it was never just about sitting at a desk and cranking out code—it was always about solving problems. The code is just the tool; the real value has always been in understanding the problem and finding innovative solutions. Now, with AI, that value lies even more in being a visionary, a shepherd guiding the potential of this transformative technology. It’s about collaborating with domain experts to solve their toughest challenges. Many don’t yet grasp the true capabilities of AI, and it’s our responsibility to illuminate that path.
>
> When I joined my current company, no one was tapping into AI. But as people started to see what I was doing with it, the enthusiasm became infectious, and gradually more began to adopt it. This is vital because when a team embraces an AI-first mindset, you get a richer diversity of perspectives. People begin to discover new possibilities and share their insights, creating a cycle of innovation. The mindset shifts from ‘how can we do this?’ to ’how can we leverage AI to do this?’—and that’s where real breakthroughs happen.

### Final Thoughts 

I love how Alex thinks about this stuff. Having the background thread running at all times has allowed him and his team to achieve incredible results with a small number of people in a short amount of time. I think this is the future of building. What are you or your company trying to build? How are you using LLMs? What are you or your team most curious about or where do you need help? I’d love to hear from you: mattstockton@gmail.com