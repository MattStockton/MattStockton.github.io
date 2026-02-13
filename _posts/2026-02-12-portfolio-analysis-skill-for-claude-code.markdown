---
layout: single
title: "I Published My Portfolio Analysis Workflow - Try It Yourself"
excerpt: "People asked me to share the portfolio optimization workflow from my last post. I turned it into a Claude Code skill you can install and try with your own brokerage data."
category: "Finance & Investing"
tags: ["personal-finance", "ai-tools", "claude-code", "portfolio-analysis", "workflow"]
---

I recently wrote about [using Claude Code to build a portfolio optimization plan](/2026/02/10/building-a-portfolio-optimization-plan-with-claude-code.html) - I fed it our brokerage CSV exports, described our goals, and iterated over several sessions until it produced a phased action plan with tax impact analysis and fund recommendations. That post ended with a section called "If You Want to Try This" with tips on how to do it yourself from scratch. After it went up, a few people asked if I could just share the workflow so they didn't have to start from zero.

So I did: [MattStockton/portfolio-analysis](https://github.com/MattStockton/portfolio-analysis).

If you haven't used [Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview) skills before - a skill is basically a set of instructions you give Claude so it knows how to do something specific. It's not code or a traditional app. It's markdown files that describe a workflow, and Claude follows them when you ask it to do that thing. Because it's just text, it's not locked to Claude Code either. You could drop these files into a Claude project on claude.ai, use them with another AI tool, or just read them and adapt the approach yourself.

## What I Changed to Make It Reusable

My original project was built around my specific situation. The parsers only handled the brokerage formats I happened to use. The fund classifications were built up one session at a time as Claude encountered my specific holdings. My tax calculations were hardcoded to my bracket. My allocation targets were baked into the project context. All of that worked great for me but wasn't useful to anyone else.

To generalize it, I had Claude help me work through each of those pieces. The parsing logic now reads whatever headers are in your file and writes a parser on the fly instead of expecting my specific column layouts. I pulled the fund classifications into a reference database of 190+ funds across eight brokerages, with keyword matching for anything not in the database. Tax calculations got their own reference file covering federal and state brackets. And the allocation targets are now a set of seven templates (or custom) you can pick from or ignore entirely and define your own.

The other big thing was the workflow itself. In my original project, I wrote a long goal prompt and then iterated with Claude over several sessions. That worked because I was willing to put in the time and I knew what I was looking for. For someone picking this up cold, that's a lot to figure out. So the skill breaks it into six steps with structured questions at each one - you're picking from options instead of writing freeform prompts.

The goal was to get people 80% of what I got without having to do all the upfront work I did. The other 20% comes from the back-and-forth - clarifying your specific constraints, pushing back on recommendations, iterating until the plan fits your situation.

## What You Get Out of It

You provide CSV exports from your brokerage accounts and the skill handles parsing them - Fidelity, Schwab, Vanguard, E\*TRADE, Merrill, or whatever else. It reads the headers and figures out the format.

From there it classifies your holdings, runs a gap analysis against your targets, checks for tax-inefficient placements (like bonds in taxable accounts or cash sitting in Roth space), and looks at whether your recurring contributions are closing gaps or making them worse.

Then it puts together a phased action plan. Free moves in retirement accounts first, then low-tax fixes, then contribution changes, then long-term hold-and-dilute strategies. Each recommendation includes the specific fund, amount, account, tax cost, and rationale.

## Try It

You need CSV exports from your brokerage accounts - most brokerages have a "Download" or "Export" button on the positions page. When you export, look for options to include extra fields like cost basis, Morningstar category, expense ratio, and fund ratings. The skill can figure a lot of this out from the fund symbol alone, but having it in the export gives it better data to work with. The [repo README](https://github.com/MattStockton/portfolio-analysis) has setup instructions. I built it as a Claude Code skill, but you don't need Claude Code specifically. The skill files are just markdown - if you upload them to claude.ai, ChatGPT, or any other AI tool that lets you provide reference files, it should pick up the workflow and do its best with it.

**Privacy:** The skill is just markdown files - it doesn't collect or send anything anywhere. Your brokerage data goes to your LLM provider as part of the conversation, same as anything else you share in these tools.

**Limitations:** US tax system only. Tax brackets are based on 2025 law. Default templates lean toward index funds but it supports active and blended approaches. Not financial advice.

## Last Thing

Your situation is different from mine and you'll probably want to modify things. The skill is just markdown files - you can change the instructions, add your own constraints, or take it somewhere I didn't. How far you get depends on how much effort you put into the back-and-forth.

Beyond the portfolio stuff, I think the more interesting idea is that this pattern works for any domain. If you've built up a good workflow with an AI tool over multiple sessions, you can probably extract it into a skill that other people can pick up and run with.

If you try it, let me know how it goes. Open an issue on the [repo](https://github.com/MattStockton/portfolio-analysis) if something doesn't work or if your brokerage format trips it up.
