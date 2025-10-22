---
layout: single
title: "Building Dashboards with AI"
excerpt: "A workflow for translating business requirements into working dashboards using AI coding tools."
category: "Building with LLMs"
tags: ["data-analysis", "ai-tools", "product-development", "workflow"]
---

I've been building dashboards with AI lately and it's changed how I think about the self-service analytics vs. custom dashboards tradeoff.

I've done both approaches multiple times over my career. Self-service analytics sounds great until you build it and nobody uses it, or you end up with a mess the data team has to manage anyway. Custom dashboards solve the adoption problem but create a maintenance nightmare with a long tail of code to maintain.

The distance between fuzzy requirements from a business partner and working code is now short enough that you don't need to choose between these options anymore. You can just build the dashboard they need in a few hours.

## How AI coding tools change this

You can build elaborate dashboards in several hours now with tools like Claude Code. Multiple filtered views, time-series visualizations, aggregations across different dimensions, drill-downs into details.

There's a lot of Python and Pandas and Streamlit code in the training data for these models, which makes it straightforward to build dashboards assuming the underlying data is available and clean. You can also hook up an MCP server to Claude Code if your database has one. This lets it introspect the data structure, which helps it understand how to structure SQL queries and write code to get at what you're trying to do. You can host these dashboards on services like Modal very easily.

I've used this strategy a number of times now across different projects.

## The workflow

Here's a basic pattern that gets you moving. This is broad strokes and obviously missing some steps, but it's a starting point:

1. Have a meeting with your business partner and have them talk through what they're looking for. How do they want to visualize the data? What are they trying to understand about it? You're figuring out the views and ways they want to shape and work with the data. Ideally, you'll take really good notes or record this meeting and then transcribe it later and distill that information using a large language model.

2. Get your coding agent access to the database schema. You can export the schema and use it as context for your coding agent, or you can hook your coding agent up to an MCP server for the database so it can introspect the tables, schema, and data within the database. There are MCP servers now that connect to common databases.

3. Process the interview into technical instructions. You're translating what they said into more technical terms and turning it into bullet points that describe what they actually want. You still need to translate it, but the point is you're writing it in plain language versus writing Pandas or Streamlit code yourself.

4. Use Claude Code to build a Streamlit app that queries the database and displays the data. The value here is that Pandas and Streamlit code is often hard to write but easy to check. If you're an experienced engineer, you can look at what it generates and validate it's doing what you want.

What makes this work is the distance between fuzzy business requirements and working code is much shorter now. You translate their needs into plain language instructions instead of writing code yourself. The AI tool handles turning those instructions into Pandas and Streamlit code. That's the shift that makes this approach practical.

## When this makes sense

For smaller scope dashboards or when you need to answer just a handful of questions, I think this approach makes a lot more sense now. With AI tools, you can build purpose-built dashboards directly without all the overhead of setting up self-service infrastructure.

The dashboards you build with Streamlit are often more interactive than what you can build with self-service analytics platforms anyway. There's so much Streamlit content in the training data that these models know how to build filtering, searching, and dynamic interactions that make the dashboards feel polished.

This works best for scrappy needs where you need to visualize data quickly, or when a small data team is building focused dashboards for specific teams. The overhead of setting up full self-service platforms often isn't worth it for these use cases.

This isn't for everyone. If you need centralized metric definitions across dozens of dashboards, you still need a semantic layer and metrics layer to ensure everyone agrees on what "revenue" or "active users" means. But even with that foundation in place, there's still a place to build custom dashboards on top of it using AI coding tools. The tradeoffs don't fully go away for larger analytics platforms serving many different use cases, but I think the tradeoffs are different now.

## For the skeptical reader

If you're reading this and thinking about all the ways this can go wrong, I get it. Querying production databases and locking them up. Ignoring data quality. Pandas code that chokes on real data volumes. Disposable dashboards that become mission-critical with no documentation. Recreating the shadow IT problem we spent years trying to solve.

If you need data quality validation, complex security models, or you're querying massive datasets that need careful optimization, you need proper data infrastructure and BI platforms. If you're building dozens of dashboards that need consistent metric definitions, you need a semantic layer. There's a time and place for doing things the rigorous way.

But when you need to quickly understand what a business partner actually wants, when you're working with reasonably clean data at manageable scale, when a small data team is building focused dashboards for specific needs, this approach gives you options you didn't have before. You still need to query a replica or data warehouse, not production. You still need to validate your numbers. You still need to document what you build and understand the joins and business logic.

This doesn't replace proper data engineering. There's a middle ground between spending three months setting up a self-service platform and just exporting to Excel. That middle ground is more accessible now.

I've built dashboards this way a number of times now. The workflow is repeatable. If you're in this space, just try it out. Even if you just have a CSV file or a database you're playing with, try the workflow above and see how far you get. You might be surprised what you can build in an afternoon.
