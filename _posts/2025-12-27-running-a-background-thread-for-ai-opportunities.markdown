---
layout: single
title: "Running a Background Thread for AI Opportunities"
excerpt: "Tedious tasks with clear inputs and outputs are now trivially automatable. The hard part is remembering to ask."
category: "Building with LLMs"
tags: ["claude-code", "ai-tools", "workflow", "automation", "productivity"]
---

I enrolled my kids in 8 rec department classes and got 8 confirmation emails. Each needed to go into Google Calendar - different dates, times, recurrence patterns, skip weeks. I almost started clicking through the calendar UI before realizing Claude Code could handle it in a couple minutes.

I've been running a background thread for this - a constant awareness asking "could this be automated?" I keep underestimating what's worth handing off.

## The Task

Each enrollment email looked like this:

> Enrollment in Level 3 Swim: Stroke Development, 11:00 am (# 5497)
> Enrollment Effective Date: December 9, 2025
> Meeting Dates: From Mar 8, 2026 to Apr 26, 2026
> Each Sunday from 11am to 11:30am
> Except the following dates:
> Sunday, March 29, 2026
> Sunday, April 5, 2026

I opened [Claude Code](https://claude.ai/code) and pasted in the email thread:

"Can you create clickable Google Calendar links for all of these events?"

It generated 8 links. Then I asked:

"Can you add this person to all the invites and then regenerate the links?" (my wife's email)

It modified all 8 links. Then:

"Can you open all of these links in the browser so I can accept them?"

Claude Code used Bash to open each link in my browser.

![Claude Code opening calendar links in the browser](/docs/assets/images/background-thread/opening_links.png)

One click per event to add it to the calendar. For the ones with skip dates that couldn't be encoded in the invite link, I asked:

"Which ones do I have to manually delete because they have skip dates? Just give me a list."

It gave me the list. I manually deleted those specific occurrences. Done.

It worked on the first try.

## Easy for the Model, Tedious for Humans

Doing this manually means opening Google Calendar, clicking through the UI 8 times, entering dates and times, setting up recurrence patterns, adding my wife as a guest - that's 15+ minutes of tedious clicking. The kind of work where you fat-finger the time on event 6 because you're bored.

This isn't a task I would have innately thought to reach for AI on. It's not coding. It's not writing. It's just administrative tedium. But AI handles it easily.

## The Path to Automation

After finishing the task, I asked Claude Code to create a slash command based on our conversation:

"Please make me a slash command so that I can repeat this workflow in the future"

Slash commands are markdown files with instructions that Claude Code loads when you type the command name - you can write them from scratch, but in this case I had Claude Code generate one from the workflow we just walked through together.

Here's an excerpt from the generated command:

![Excerpt from the generated slash command](/docs/assets/images/background-thread/slash_command.png)

I tested it with the same email content. It worked.

This is step one toward fully automating the workflow. The [Claude Agent SDK](https://platform.claude.com/docs/en/agent-sdk/overview) lets you take a working slash command and run it programmatically. I've [written more about this approach](/2025/11/25/how-i-prototype-agentic-workflows.html) - prototyping interactively in Claude Code, then porting to the SDK once you've validated the workflow works.

The work isn't throwaway. Prototyping an agentic workflow interactively is a bulk of the effort toward having a working agent. You figure out what works in a tight feedback loop before committing to infrastructure.

## The Failure Mode

This calendar example is actually trivial for current models. They can do much more sophisticated tasks than parsing emails and generating calendar links.

The failure mode is not being ambitious enough. If you're only using AI for tasks you're confident it can handle, you're probably underestimating what's possible.

This works best for tasks with clear inputs and outputs - structured data, defined formats, repeatable workflows. It's not magic for ambiguous problems where the hard part is figuring out what you actually want. But a surprising amount of tedious work fits the pattern.

## What I'm Doing About It

A lot of the work across businesses - parsing receipts into expense reports, pulling info from emails into spreadsheets, reformatting data between systems, turning meeting notes into action items - is now automatable with a conversation and some decent prompts. Not with custom software or expensive integrations. Just a background thread noticing the opportunity and the willingness to try. The people who figure this out first are going to have a real edge.

I'm continuing to look for these patterns in my own work and for clients. If you have a business with tasks that might fit this mold, I'd be interested to chat. Or just try it yourself - next time you're about to do something tedious, pause and ask whether you should be doing it at all.
