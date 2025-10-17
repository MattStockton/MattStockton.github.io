---
layout: single
title: "Claude Skills: Better Organization for Agent Instructions"
excerpt: "Skills gives me a better framework for organizing Claude Code instructions that have been growing unwieldy in CLAUDE.md files."
---

Anthropic announced [Claude Skills](https://www.anthropic.com/news/skills) yesterday, and my first reaction was that this solves some real problems I've been dealing with.

I've been using Claude Code heavily for my consulting work, and the more I use it, the more I find myself wrestling with how to organize instructions. My CLAUDE.md files keep growing and drifting across projects. I spend time trimming them down, but they balloon back up. It's been a challenge to keep things organized as my usage has evolved.

Skills gives me a better framework for thinking about this organization problem.

## What Are Skills (and Claude Code)?

For those unfamiliar: Claude Code is a command-line tool that lets Claude work directly with your files. It can read your code, create documents, run commands, and basically act as an AI assistant that has full access to your local environment.

Skills are folders containing instructions, scripts, and reference materials. Each skill has a short description that Claude sees up front, and when it determines a skill is relevant, it loads the full content. This progressive disclosure approach means Claude only loads what it needs when it needs it. So when I'm working on code, Claude sees "code-review skill" in the list but doesn't load all my review guidelines and tools until I actually ask for a review.

I've been patching together similar patterns using CLAUDE.md files and custom tools, but the skills abstraction puts explicit packaging around it that feels really elegant. The [engineering post](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) does a good job explaining the technical rationale.

## The Problem with CLAUDE.md Files

Here's what I've been experiencing over the past few months.

My CLAUDE.md files have grown to 1000+ lines in some repositories. They accumulate instructions over time: document templates, meeting notes, code review guidelines, email formatting, git commit patterns, and more. I periodically trim them down, but they inevitably grow back.

I also want consistent writing style and document structure across multiple projects. But keeping CLAUDE.md files in sync across repositories is tedious, and honestly, I haven't done it. They drift, and then I'm left with slightly different instructions in each project.

I've tried using nested CLAUDE.md files to separate concerns, which helps, but then you're locked into a specific directory structure that doesn't always align with the instructions you want to organize. The file system hierarchy ends up dictating how you structure your agent capabilities, which feels backwards.

I've also noticed Claude compacting more frequently lately. Compacting is when Claude summarizes earlier parts of the conversation to save context space. My hypothesis is that large CLAUDE.md files are eating up context, leaving less room for actual work. Skills should help here.

## Why This Approach Appeals to Me

What appeals to me most is the composability. I could build a repository of skills and share them across different projects. Version control them like code, see how they evolve over time, and even run Claude Code on the skills repository itself to help manage and refine them. This would solve the drift problem much better than manually syncing CLAUDE.md files.

Skills and MCP (Model Context Protocol) solve adjacent problems, but Skills covers a lot of ground I'd otherwise use MCP for with native capabilities and small scripts. It's also more accessible to non-technical people who are good at articulating what they want.

Take code reviews as an example. I often make large changesets and want Claude to review them using specific guidelines and tools. Right now that's all embedded in my CLAUDE.md file, mixed in with everything else. As a skill, it would be discrete: review instructions, specific tools to run, formatting preferences, all in one place.

The organizational structure should push you toward better compartmentalization, which I think would be healthy. My CLAUDE.md files have gotten messy over time, with instructions at different levels of detail for different purposes all mixed together. Skills encourage single-purpose capabilities. One skill, one job.

You also get a useful feedback loop. When you run Claude Code, you can see which skills it's using for a given task. If it picks the wrong skill, or if one skill keeps getting used for multiple unrelated tasks, that tells you something. The skill is probably too broad and should be split up.

## What I'm Planning to Do

I wrote about [using Claude Code as a knowledge management system](https://mattstockton.com/2025/09/19/how-claude-code-became-my-knowledge-management-system.html) a few months ago, where I built out a fairly comprehensive set of instructions living in nested CLAUDE.md files.

I'm planning to convert parts of that system into skills in a separate repository. Right now these capabilities are either sections in CLAUDE.md or scattered across folders, but they'd fit naturally as discrete skills.

I'll report back on how well this works in practice.

If you're using Claude Code and running into similar organizational challenges, this might be worth exploring. If you haven't tried agentic systems yet, Skills is a good entry point. Start with one capability you use frequently and see how it feels as a standalone skill. I'm planning to start with my code review workflow and go from there.
