---
layout: single
title: "Tool Calling and File Access: When AI Can Run Commands on Your Actual Files"
excerpt: "Instead of uploading files to a chat window, give the model access to your file system and let it run commands directly. Here's what that looks like in practice."
category: "Building with LLMs"
tags: ["tool-calling", "claude-code", "ai-tools", "workflow", "productivity"]
featured: true
---

When people want AI to work on their files, they usually upload them to a chat window. There's another way: give the model access to your file system and let it run commands directly.

This is tool calling combined with file access. I've [written about tool calling before](/2025/11/24/tool-calling-and-the-value-of-understanding-ai-more-deeply.html) - this post goes deeper to show why file access matters.

The example: splitting a 500+ page PDF into dozens of separate documents for a client project. The PDF contained dozens of merged files - some scanned, some text-based, all concatenated together. The challenge is finding where one document ends and the next begins, then splitting at those boundaries. But the pattern works for any problem where you'd describe rules to a person and have them apply those rules across many files.

## How Would a Person Do This?

I start most of these projects by asking: how would a person solve this? You'd open the PDF, scan through it, and look for where one document ends and the next begins. You'd identify patterns - title pages, page numbers that restart, specific keywords, formatting differences, appendix markers.

Different documents have different tells. Maybe title pages have a specific header. Maybe there's a "Table of Contents" at the start of each document. Maybe page numbers reset to 1. You'd build a mental rule set: "when I see X, that's probably a new document starting."

That's the first part - figuring out the rules. Then you have to apply them across thousands of pages.

## What Tool Calling Makes Possible

Tool calling means the model has been trained to output tokens that trigger actions instead of just generating text. The simplest example: you type "list all the files in this folder" and the model runs `ls` - a built-in command on your computer that lists files in a directory. You describe what you want, the model figures out the command and runs it.

For the PDF problem, the model needs text to search. Tools like [Azure Document Intelligence](https://azure.microsoft.com/en-us/products/ai-services/ai-document-intelligence) or [Docling](https://github.com/DS4SD/docling) handle this as a pre-processing step - they extract text from PDFs while preserving formatting like headers and structure. You end up with a large text file or Markdown.

Once you have text, the model can search it using `grep` - a command that finds patterns in files. There's also the concept of regular expressions, which are generic ways to represent text patterns. These tools have existed for decades and they work.

You don't need to know how grep works or how to write regular expressions. You describe the patterns you're looking for in plain language. For a document splitting problem, these might be things like:

- "The first page of each embedded document has a header with the word 'TITLE'"
- "Page numbers restart at 1 for each new document"
- "Each document ends with an appendix section"

The model takes your descriptions and turns them into actual commands. You say "find lines with APPENDIX in all caps" and it runs:

```bash
grep -n "APPENDIX" document.md
```

You describe "find where page numbers restart at 1" and it builds a regular expression:

```bash
grep -E "Page 1 of [0-9]+" document.md
```

The `-n` flag returns line numbers so the model knows where in the document each match occurs. The `-E` flag enables extended regex for pattern matching. You don't need to know any of this - you describe what you're looking for, the model figures out the syntax.

Once you've identified the boundaries, standard Python libraries like PyPDF2 can split the actual PDF file at those page numbers. The model can write this code for you too.

## Why This Beats Dumping Everything into the Model

Why not just load the entire PDF into the model and ask it to split the documents? Context management. LLMs can only pay attention to a certain amount of text at once (the "context window"). You've probably noticed that long conversations in ChatGPT sometimes go off the rails. The model degrades with longer context.

A 1000-page document would likely exceed the context window. Even if you could fit it, the model's performance would suffer. And you'd pay for every token.

Tool calling solves this. Instead of loading the entire document, the model searches it. It might run grep to find lines containing "APPENDIX" - which returns 50 results. It looks at those 50 results, decides what to search for next, and pieces together the document structure.

The model inspects the document without loading everything into context. Cheaper, faster, more accurate.

## Let the Model Find the Patterns

You can also go the other direction. Instead of you identifying the patterns, have the model figure them out.

Go through the document manually and label the boundaries. Document 1 is pages 1-79. Document 2 is pages 80-100. Document 3 is pages 101-107. You create a "golden set" of correct boundaries.

Then give the model file system access and describe what you need. Here's roughly how I started:

> "I have a markdown file at /documents/combined.md that contains multiple documents merged together. Document 1 is pages 1-79, document 2 is pages 80-100, document 3 is pages 101-107. Look at the content around these boundaries and tell me what patterns indicate where one document ends and the next begins. I need patterns that grep or a simple script could find."

The model examines the content around your labeled boundaries and proposes rules.

The risk here is overfitting. If you only look at one document, the rules might be too specific to generalize. You need to work with the model iteratively - refining rules, testing on other documents, adjusting for edge cases. It's not one-and-done.

PDFs are messy. Scanned documents have OCR errors. Some documents won't have consistent patterns at all. You'll hit edge cases where the rules fail. That's expected - the goal is to handle the common cases automatically and flag the exceptions for manual review.

## Write Tests

Whatever rules you end up with, test them. You have that golden set of labeled boundaries. Run your rules against the document and check: did it find the right splits?

You verify the system does what you think it does. And you can safely change the system later. New model comes out? Extended rule set needed? You can modify your prompts and re-run tests to make sure you didn't break what already worked.

This part gets technical, but the point is important: you need a way to verify your system works and catch regressions when you change it. Basic unit testing frameworks like pytest work fine. A test might assert that document 1 ends at page 79 and document 2 starts at page 80 - exactly matching your golden set. The model can help you write these tests. Add multiple documents to your test cases as you encounter them.

## The Same Pattern Works for Many Problems

Document splitting is one example, but the broader approach - giving a model tools to inspect and search your files - works for a lot of different problems:

- Pulling action items and owners from a folder of meeting transcripts
- Categorizing hundreds of customer support tickets by issue type
- Extracting vendor names and amounts from a year of expense receipts
- Finding every mention of a feature across months of Slack exports
- Cleaning up a messy CSV where dates are in five different formats

Any problem where you'd describe a pattern to a person and have them apply it systematically - tool calling with file system access can help.

## Try It on a Real Problem

If you haven't used a tool like [Claude Code](https://www.anthropic.com/claude-code) that gives models file system access and tool calling, start there. Point it at files you need to process, searches you need to run.

Web-based chat interfaces can't do this. They're useful, but they can't inspect your files, run commands, or build tools on the fly. The combination of tool calling and local file access is where I spend most of my time now - and I think it's where this whole space is heading.

Once you get a workflow working, you can save it as a slash command or skill to reuse later. And if you want to fully automate it, the [Claude Agent SDK](https://platform.claude.com/docs/en/agent-sdk/overview) lets you run these workflows programmatically. I'll write more about that in a future post.

A tool called "Claude Code" might sound like it's only for programmers, but don't let that stop you. Pull it down, point it at a real problem, and try some things. You'll quickly see how powerful this is.
