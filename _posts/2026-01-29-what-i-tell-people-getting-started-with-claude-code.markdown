---
layout: single
title: "What I Tell People Getting Started with Claude Code"
excerpt: "Plan mode, work logging, the interrogation pattern - habits that make Claude Code useful whether you write code or not."
category: "Getting Started with AI"
tags: ["claude-code", "workflow", "productivity", "ai-tools", "knowledge-work"]
---

I recently spent an hour walking a friend through how I use [Claude Code](https://www.anthropic.com/claude-code). He's not a developer - he manages a portfolio of 90+ companies and does a lot of knowledge work: newsletters, performance reports, meeting notes. He'd heard me talk about these tools and wanted to see what was possible.

It was a good conversation. Pairing on this together - actually trying things instead of just describing them - worked better than I expected. He could see things in action and ask questions as we went. Afterwards I wanted to write down some of the takeaways, some of which I've [written about before](/2026/01/07/claude-code-for-non-technical-work.html).

Most of these are habits rather than features - ways of working with the tool that make everything else easier.

## Plan Mode

Claude Code has a "plan mode" - a thinking mode before execution. When you put Claude in plan mode, it won't take any actions. It thinks through what you're asking for and asks clarifying questions. Type `/plan` or press shift-tab before describing what you want.

I told my friend: always be in plan mode for anything non-trivial. Plan mode lets you explore without committing to anything. You can describe a vague idea, let Claude ask questions, refine your thinking, and only then decide whether to proceed. If you jump straight to execution, Claude might start creating files or making changes before you've fully figured out what you want. When planning is complete, Claude will ask if you want to clear the context and execute. Clear the context - it prevents the model from getting confused by all the back-and-forth exploration that happened during planning. You keep the plan, lose the noise.

You're never committing to anything until you've seen Claude's proposed approach and explicitly approved it.

## The Interrogation Pattern

You don't need 100% clarity on what you want before you start. You can use Claude to pull it out of you.

Tell Claude to "ask me questions exhaustively" or "use AskUserQuestion exhaustively to understand what I want." Claude will keep asking clarifying questions until you tell it to stop. It pulls information out of you that you didn't know you needed to provide. It asks about edge cases you hadn't considered. It catches assumptions you didn't realize you were making.

You don't need to be precise upfront. You don't need to know the right terminology or anticipate what Claude needs to know. Just describe your goal and let Claude figure out what questions to ask. It helps to know how to instruct the model, but you don't need to be perfect at it - you can iterate, and answering questions is easier than crafting the perfect prompt.

## Work Logging and Compounding

Claude Code loves files. It can read them, search them, reference them later. So store information about your work in files - work logs, commit messages, meeting notes, project summaries. Be verbose. You can always trim it down later, but you can't recover context you didn't capture.

When Claude can read what you've done before, it produces better outputs. You're not starting from zero every session. I can ask Claude to look at my git commits and summarize what I worked on last week. I can point it at meeting notes and have it draft a follow-up. None of this happens if you're using Claude as a chat interface that forgets everything between sessions.

Automate the capture where you can. You can get Claude Code to log its own work by setting up good CLAUDE.md files and skills - and you can use plan mode and the interrogation pattern to build those. Tell Claude what you want to track, let it ask questions, and have it create the instructions for itself. You're not going to get it right the first time. But as you figure out patterns for storing what you've learned, things just keep getting better. That's how I put it to my friend: "things just magically get better" as context accumulates.

## Git Repository Backing

This is probably the biggest technical hurdle for folks who aren't technical. But I do think it's necessary, and it's achievable - Claude Code can help you get it set up.

A git repository is just a folder where changes are tracked over time. Every time you save a checkpoint (called a "commit"), git remembers what changed and lets you add a note about why.

Files need history - not just for version control, but so the system itself can reference what changed and when. I have a skill that looks at uncommitted changes, figures out what I did based on the changes and session context, adds an entry to my work log, and creates a detailed git commit. When I need to know what I worked on, I ask Claude to look at the git commits since a certain date and give me a summary. It looks at the changes in each commit and tells me what I did.

History gives Claude something to work with beyond just the current state of your files.

## The Slot Machine Mentality

Bias toward action and iteration rather than reviewing everything upfront. Work happens fast enough now that you can throw things away - if something isn't working or heads in the wrong direction, scrap it and start over.

I've gotten more comfortable not reading every detail of what Claude plans to do. I just let it execute. Because first, it's probably right. And second, if it's not right - pull the slot machine again. It's lower cost to iterate than to review everything upfront.

You don't need to understand every line of what Claude produces. You need to understand the output and whether it matches what you wanted. If it doesn't, try again. Describe what's wrong and let Claude fix it. If a session goes off the rails, type `/rewind` to backtrack to an earlier point in the conversation.

Plan mode, git, and `/rewind` all let you back out of mistakes. Don't let the desire for certainty slow you down.

## Building Skills Through Doing

Skills are saved instructions that tell Claude how to do a specific task. They're markdown files that describe what Claude should do, what questions to ask, and how to format the output. I have skills for summarizing meetings, committing changes with work log updates, turning transcripts into blog posts. Once you have a skill, you type a command and Claude follows those instructions.

I wouldn't try to create skills before you've done the task manually at least once. Work through a real task with Claude - post a transcript, describe a document you need, iterate until you get something you like. Then tell Claude to turn that conversation into a skill you can run next time.

You don't even need to read the skill Claude creates. Just trust that it captured what worked. Next time you have a similar task, invoke the skill. If the situation is slightly different, just tell Claude - it adapts. You figure out what works through doing, then codify it.

## Getting Started

People are often hesitant to start because they're not sure how. But there's not much downside here. You can explore without committing, revert when things go wrong, start without knowing exactly what you want. If something breaks, you try again.

The skills that matter most for using Claude Code are non-technical: curiosity, persistence, clear thinking, confidence. It helps to understand concepts like git and file organization, but Claude Code can help you learn those too - if you keep trying things. After our session, my friend said what helped most was actually seeing what this looks like in practice. That's hard to get from reading. You have to try it.

If you're already using Claude Code and have patterns that work for you, I'd like to hear about them.
