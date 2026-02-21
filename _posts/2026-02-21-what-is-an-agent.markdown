---
layout: single
title: "What Is An Agent?"
excerpt: "My attempt to describe what an agent is and why it's so incredible, yet simple."
category: "Software Engineering"
tags: ["ai-tools", "agents", "llm", "software-engineering"]
---

This is my attempt to describe what an agent is and why it's so incredible, yet simple. I'm not going to edit this and I'm not going to run this through an LLM. I'm also going to try to do this in five minutes or less. Let me know how I did, and what I missed that you think is important.

- An agent is simply an LLM that can call tools
- A tool is a computer application or a piece of code. For example, opening a file is a tool. Searching for a word in a file is a combination of tools.
- Command line tools have been in existence on computers for a very long time.
- These tools are composable and can solve almost any problem as it relates to files that are on the computer.
- As an example, this 'tool':

```
cat notes/*.txt | tr '[:upper:]' '[:lower:]' | grep -oE '\b[a-z]{4,}\b' | sort | uniq -c | sort -nr | head
```

- Takes all your text notes, normalizes the text, pulls out some words, counts them, and then shows the most common words.
- The tool as read may make no sense to you if you're not an experienced engineer, but the models know exactly how to 'do this' - meaning 'generate that text and do it'
- With a written instruction like 'Find the most common topics in my notes.' - The model has been tuned enough so that it can generate the above tool call.
- Any computer application on your computer is a tool. Excel? It's a tool. Slack? It's a tool. Web Browser? Same
- So if you blur your eyes, an agent is something that can simply control your computer. Pretty much any aspect of it.
- So what if a tool doesn't exist that does what you need the agent to do?
- The agent has a tool that lets it write computer code. This tool is one of the best tools that it has because the foundation labs have spent a lot of time making sure this tool works well.
- And computer code can solve almost any problem.
- So you can have an instruction like: 'Write me some code that analyzes this image and gives me the exact coordinates of where the red balloon is.'
- Coding agents like Claude Code will see this and then try to write you some code that does that. It will often use other tools in the code itself. So it might download some libraries that it can use or some other techniques that it knows to be able to compose some software to solve the above problem.
- Using a tool like Claude Code, eventually you'll be able to build some code that solves the problem you're talking about.
- So what do you have now?
- You have a new tool called the Find the Red Balloon tool.
- And now you can give that tool to the agent so it can just use it next time.
- Basically, you use an agent to build a tool that you can hand to another agent and it can use that tool whenever it needs to.
- So now you can just say, "Find the red balloon in the image." And the agent will use the tool to do that.
- If the tool works, then it's going to get it right. You can build deterministic tools that the agent can use. Even though LLMs are at their core, non-deterministic, you can bake in lots of determinism.
- This is the magic, but also the simplicity of agents.
- It's just an LLM using a computer.
- But it is incredibly flexible, incredibly generalizable, and incredibly composable. So basically you can solve almost any problem.
- The other important thing here is the file system.
- Most systems rely on data to provide any value.
- It turns out if you put data in the right place in a file system, meaning folders on a computer, and you organize that well, the agent can just use tools to find what it needs.
- So basically, agents come down to tools and file systems.
- But those things can be assembled in so many different ways that you can solve incredibly hard problems that truly weren't solvable before

Hope you found this interesting. There are obviously many other details around what agents are. But I really wanted to capture the core essence as I see it in a way that's accessible to folks. Let me know how I did and how you think about it.
