---
layout: single
title: "How I Prototype Agentic Workflows Before Writing Agent Code"
excerpt: "An approach for prototyping agentic workflows interactively in Claude Code before committing to a framework."
category: "Building with LLMs"
tags: ["claude-code", "agentic-workflows", "workflow", "ai-tools", "prototyping"]
---

The conventional wisdom for agentic workflows is to set up a framework upfront - figure out the context engineering, build a retrieval pipeline, define your tools. But for many tasks, there's a faster way.

I've been using this approach for document generation: I have source documents that need to be synthesized into a structured report following a specific template. The naive approach would be to throw everything into context and hope for a good answer. But often there's too much information, or the task requires multiple passes - distilling first, then refining, then structuring. That's how you'd do it manually, and it's more amenable to an agentic workflow.

What I've found is that you can prototype the workflow interactively in Claude Code, and the work isn't throwaway - it becomes the foundation for automation later.

## Start with Data in Folders

Here's how I've been approaching it. First, get the data you need and organize it in folders on your local machine. You can pull it down from an API, manually download files, or even use Claude Code to write the retrieval code for you. It doesn't matter how you get it there. The point is to not overthink it - just get the raw material in place.

Once the data is in place, open Claude Code in plan mode and describe what you're trying to accomplish. For the document synthesis example: "I have source documents in this folder. I need to produce a report that follows this template. The report should pull specific information from each source and synthesize it into these sections." Then let it go.

Claude Code can search the file system, run bash tools, read files, and make decisions about what to do next. It has everything it needs to inspect the documents and figure out how to reach the goal you described. It can search for specific terms, read files sequentially, try different approaches - building intuition about what works without you having to commit to infrastructure upfront.

You can also nudge it with strategies if you already have intuition about what works. Sometimes I'll record myself talking through how I'd approach the problem manually, then use that transcript as input to help Claude Code understand my process. If you know certain search patterns work well for the problem, just tell it.

## Converting Conversations to Slash Commands

Once Claude Code generates a report you're happy with, you can ask it to turn the interactive conversation you just had into a slash command - a markdown file with instructions that Claude Code loads when you type the command name. It packages up the context from your back-and-forth into something you can rerun.

The quality of the slash command depends on how clean your conversation was. If you had a lot of false starts - Claude Code did something wrong, you corrected it, it tried again - that steering clutters the conversation history and ends up in the slash command. Use /rewind to roll back messages that didn't work. Each rewind removes that exchange from the history, so by the time you ask Claude Code to generate the slash command, it's working from a clean conversation where each step succeeded. The goal is an interactive session that looks like a straight path to a good output.

The slash command captures the specific guidance from the conversation: how to search the files, what to extract from each source, how to structure the output. Once you have it, clear your context, delete the output document, and run the command. If you have some decent luck, it should get close to re-producing what you just did interactively.

## Iterating on the Slash Command

The first version of the slash command usually needs work. I run it, look at the outputs, and write down what's wrong - maybe it extracted the wrong fields, or the structure doesn't match the template, or it missed information that was in the source documents.

Then I clear the session to give Claude Code a fresh context window and tell it: "You used this slash command with this data to generate these outputs. Here's my feedback on how those outputs need to improve. Please come up with a plan to improve the slash command." It updates the command, I run it again, evaluate, provide more feedback. Each iteration should get you closer.

A caveat here: there's a danger of overfitting if you're only working with one set of documents. The slash command might get too specific to that example. I try to give feedback about patterns rather than individual outputs - "the summary section is too long" rather than "this particular summary should mention X."

## The Path to Production

Claude Code has an SDK. Once the slash command is working well, you can 'port it' into the format the SDK expects and run it programmatically. I've done this, and I've also ported workflows to other agent frameworks like Agno, based on the learnings from the interactive session. The point is that you've validated you can do something 'agentically' before committing to building the actual agent and tools.

This won't work for every problem. Some tasks need more sophisticated orchestration from the start, or retrieval pipelines you can't easily prototype with file system access. But for many tasks, it's quick to validate an approach interactively before committing to infrastructure - and the work isn't throwaway.