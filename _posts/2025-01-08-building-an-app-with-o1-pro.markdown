---
layout: single
title: "Building a Self-Guided Learning App with O1 Pro"
excerpt: "I used OpenAI’s o1 pro to build a self-guided learning app — generating a PRD, writing code, and creating a working prototype in no time. This post walks through the process, showing how AI can streamline development and make building more accessible than ever."
---

<img src="/docs/assets/images/o1-pro-app/1.png"/>

I experimented with OpenAI’s o1 Pro model to prototype a self-guided learning app, and it turned out to be a fascinating process. o1 Pro, OpenAI’s latest and most advanced model, is designed for tasks like complex problem-solving, coding, and research. What sets it apart is its ability to explore multiple paths during inference, making it a bit slower but also more thorough than simpler next-token models. I wanted to see how well it could handle the end-to-end development of a tool that creates personalized educational content based on preferences like learning style, existing background knowledge, and age.

To start, I specifically asked o1 Pro to generate a product requirements document (PRD) before writing any code. From my reading, this intermediate step can help the model produce better code later by first focusing on a detailed understanding of the task. I narrated my idea aloud — freeform thoughts about what the app should do — and used the transcript as input. o1 Pro generated a detailed PRD, outlining the app’s features, goals, and functional requirements. From there, I asked it to write the code, leveraging Streamlit for a simple, interactive interface. The model delivered everything I needed in a short amount of time: a working prototype, complete with setup instructions, scripts for handling prompts, and the main application itself.

When I tested the app, it worked surprisingly well. You type in a topic, choose your preferences, and it generates tailored educational content. For instance, when I asked it to create storytelling-style lessons about US History for a 10-year-old, it delivered engaging narratives. Switching to a conversational tone for advanced probability and statistics produced concise, practical explanations. While the app isn’t perfect — there’s room to improve speed and add features — it’s a solid prototype that shows what’s possible in a short amount of time. I didn't write any of the code at all.

What struck me most about this experiment was how accessible the process felt. o1 Pro’s ability to quickly translate an idea into a working application makes it a powerful tool for anyone experimenting with AI. This wasn’t about building a polished product — it was about seeing how far I could go with minimal effort. The result? A functional app that adapts to how people learn, built with ease and efficiency. It's awesome how much more accessible building has become with tools like this. What are you going to build?

---

### Demo Video 

<iframe width="560" height="315" src="https://www.youtube.com/embed/wEvpn_576V8?si=EPjLy1C7ekuDLUj_" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### More Screen-Shots

<img src="/docs/assets/images/o1-pro-app/2.png"/>

<img src="/docs/assets/images/o1-pro-app/3.png"/>
