---
layout: single
title: "AI Coding Tools: Why I Use Claude Code"
excerpt: "After trying RepoPrompt, Cline, and others, I found the AI coding tool that finally clicked. Here's what I learned about choosing tools, avoiding the shiny object trap, and why the command line interface makes all the difference."
---

Six months of experimenting with AI coding tools taught me that the "best" tool is the one that aligns with how you actually work. I tried [RepoPrompt](https://repoprompt.com/), [Cline](https://cline.bot/), and others before settling on [Claude Code](https://www.anthropic.com/claude-code). Here's what makes it click for experienced engineers - and why trying any of these tools beats endlessly evaluating them.

## The Evolution: From RepoPrompt to Claude Code

I started with **RepoPrompt** when OpenAI's O1 Pro first came out. At the time, there was no API for O1 Pro, so you couldn't connect it to leading AI agent tools like Cursor. You had to use the chat interface. O1 Pro was astoundingly good at code generation when it first came out compared to other models, which is why I was drawn to RepoPrompt.

**RepoPrompt's key differentiator:** It's built for big, deliberate changes. The file selector lets you choose exactly what context to send to the model, and it forces intentionality because you're crafting structured prompts for complex, multi-file updates. RepoPrompt has since expanded its feature set with much more agentic behavior. This is definitely a power tool for power users - people who master RepoPrompt likely see astounding productivity increases.

I tried **[Cline](https://cline.bot/)** for a while, especially when [Gemini 2.5 Pro](https://deepmind.google/technologies/gemini/) was the hot new model. The agentic workflows were interesting, and the iteration loop was faster than RepoPrompt.

**Cline's key differentiator:** It's an autonomous agent that runs in VS Code. It can execute terminal commands, browse the web, and make multi-file changes while you approve each step. The plan versus apply mode gave you control over what changes actually got made. But I found the autonomous workflow sometimes went off in directions I didn't want.

I even experimented with **[Taskmaster](https://www.task-master.dev/)** in my Cline workflow. Very interesting tool, but I didn't want to invest the time to understand all the ins and outs. I felt like you had to lock in the plan ahead of time, which I'm sure isn't exactly the case once you really understand the tool. But after trying it a few times, I realized I'd rather own the iteration loop and define tasks iteratively versus all up front.

That's when I made a decision that's served me well: **stop spending so much time learning tools and do more real work.** There's a real danger here of continuous tool evaluation without ever building anything meaningful.

## Why Claude Code Finally Clicked

About a month ago, I started using **Claude Code** and immediately knew this was the right UX for me. The quality seemed higher, and the interface felt like it was designed for how I actually work.

**Claude Code's key differentiator:** It lives in your terminal and understands your entire codebase without you having to manually select files. It's built for iterative, collaborative work where you stay in control of each step, but it handles the context management automatically. It also has excellent tools for searching your files and the web using simple command-line tools, and it's very effective at building its own context agentically when you provide clear instructions.

Here's what makes it different:

**Clean terminal interface.** No browser tabs or IDE sidebars. The terminal limits distractions and forces you to focus exclusively on the code. It strikes an almost perfect balance between purely batch updating and purely agentic approaches.

**Exceptional inline diffs.** Shows exactly what it wants to change before applying anything. You can review, approve, or correct in real-time.

**Systematic task breakdown.** Complex requests get broken into discrete tasks that you can see and intervene on.

**Valuable clarifying questions.** When you tell it to ask questions upfront, they're almost always worth answering. Helps you think through edge cases you might have missed.

**High hit rate.** Much more likely to produce working code on the first try compared to other tools. Part of this is that Claude models are extremely good at code, and the fact that Claude built a purpose-built tool using their models exclusively probably gives them an edge versus tools like RepoPrompt and Cline that can use models flexibly.

I've had extreme success with it for tasks that are "hard to make but easy to check." Recently, I needed to build a classification model to predict an outcome with proper cross-validation and feature engineering. Manually, this would have taken me 3-4 hours of careful pandas work to get the data splits right and avoid leakage. With Claude Code, I spent time curating and distilling my requirements into clear written specifications, then worked with it iteratively to build the pipeline. The whole process took about an hour, but I could quickly scan each iteration, suggest tweaks, and end up with working code that I trusted.

That's the pattern I see repeatedly - tasks that require careful attention to detail but follow known patterns. Claude Code handles the implementation while I focus on the correctness.

**Multi-file editing intelligence.** Claude Code understands your codebase and dependencies well enough to make complex changes across multiple files that actually work together.

**Planning mode for complex tasks.** Claude Code has a planning mode (Shift+Tab twice) where it will lay out what it's going to do before executing. Especially useful for multi-step tasks where you want to review the approach first.

**Works beyond coding too.** I've used it to build slide decks for workshop content with [Marp](https://marp.app/) and I'm even using it to help curate and write blog posts. I'm actually using it right now to help structure this post.

## Practical Insights That Made the Difference

Through trial and error, I've learned a few workflow patterns that significantly improve results:

**Start fresh, stay incremental.** Restart conversations instead of resuming them - though sometimes it is valuable to resume tasks, especially if you're in the middle of an iteration. You have to get a feel for when it's better to resume versus start new. The biggest mistakes happen when I try to compress multiple iterations into one large request.

This is especially true with complex notebooks for data analysis. When I've tried to make bigger changes without incrementing, Claude Code sometimes goes off the rails and starts overcomplicating things. The solution is always the same: restart the conversation, break down the task even more, and don't be afraid to abandon a path that isn't working.

**Voice input is a productivity multiplier.** About 80% of my interactions with Claude Code are voice-based. Speaking your requirements feels more natural than typing, and it's much faster for complex explanations.

**Configure your rules files.** Every AI coding tool works better when you give it context about your preferences, coding standards, and project structure. I don't write these from scratch - I pull ideas from examples people share online, record myself talking about what I care about, and use an LLM to turn that into structured rules.

Early example of why this matters: I got stuck in a loop where Claude Code kept trying to write and run tests for a project where I was just trying to vibe and prototype quickly. An hour in, I realized I should modify my rules to say "don't write or run tests right now." That simple change completely fixed the workflow.

For Python projects, I include specific coding preferences like "use type hints for all function parameters and return values" or "prefer list comprehensions over loops when readable." These kinds of specific style preferences guide the output toward code I actually want to work with.

There's even a project called [Ruler](https://github.com/intellectronica/ruler) that acts as middleware for rules files - you maintain one source of truth and it distributes your rules to whatever format each tool expects. Solves the problem of having to adapt your instructions to every single tool.

## Key Lessons

**Just get started.** The only way to figure out how to use these tools is to dive in. Don't just read my words about what's good and bad - go try it and you'll quickly figure it out for yourself.

**Choose one tool and master it.** Every day there's a new tool in this space. You could spend all your time experimenting and never get real work done.

**Focus on problems that are hard to make but easy to check.** As an experienced engineer, you can quickly evaluate whether code output is approximately correct. This is where these tools provide the most leverage.

**Don't skip the foundational work.** Rules files and clear requirements make the difference between a tool that occasionally helps and one that consistently delivers value.

## Final Thoughts

Claude Code worked for me because it fits how I actually work - terminal-based, incremental, with enough intelligence to handle context automatically but enough control to stay in the driver's seat. It might not be the right fit for you. Maybe you prefer VS Code integrations, or you need different model access, or your workflow is completely different. That's fine.

The point isn't that Claude Code is perfect - it's that these tools genuinely amplify what you can already do when you find one that aligns with how you think.

If you're skeptical or just haven't had time to experiment, pick one and spend a week with it. You'll learn more from hands-on use than from reading about them. If you want to try Claude Code, spending 30 minutes with the [documentation](https://docs.anthropic.com/en/docs/claude-code) or this [detailed workflow guide](https://spiess.dev/blog/how-i-use-claude-code) will get you started.

Engineers who learn to work effectively with AI tools will have a significant advantage - not because AI will replace programming, but because it amplifies what experienced engineers can accomplish.

Six months ago, I was spending more time evaluating tools than using them. Now I'm focused on building. That's the real win - not finding the perfect tool, but finding one that works and sticking with it long enough to get good at it.

If you try it out, I'd love to hear what you discover. We're all still figuring this out together.