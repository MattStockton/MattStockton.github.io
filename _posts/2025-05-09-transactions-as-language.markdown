---
layout: single
title: "Transactions as Language"
excerpt: "Stripe's approach to fraud detection made me rethink how we use transformers. What looks like a row in a table might actually be a sequence. And once you model it that way, a lot of things get simpler."
category: "Building with LLMs"
tags: ["transformers", "fraud-detection", "stripe", "embeddings", "sequence-modeling"]
---

Stripe recently [shared a post](https://x.com/thegautam/status/1920198569308664169) about improving fraud detection using a transformer-based model. On paper, it's a technical win. They improved detection of card testing attacks from 59% to 97%. But the part that really stayed with me wasn’t the number. It was the shift in how they approached the problem.

Instead of training a separate model for each task like fraud, disputes, or authorizations, they started by asking a different question: could they first learn the structure of how transactions behave, before trying to solve anything specific?

They trained a transformer on billions of payment streams. Not just isolated rows, but sequences of transactions—the same card, the same user, the same device—happening over time. The model learned to represent each transaction as a dense vector that captures what it is and how it fits into the surrounding pattern.

If you’ve worked with language models, the setup might sound familiar. A payment stream becomes a sentence. Each transaction is a token. The meaning of each one depends on the context around it.

That framing shifted something for me. Payments feel like structured data. If you'd handed me this problem, I would have engineered features, trained a classifier, and refined it over time. That approach still works and had already worked well for Stripe. But they took a different path. They let the model learn its own representation of each transaction, then reused those embeddings across multiple tasks.

That also meant they no longer had to build a separate set of hand-tuned features for each new problem. Once they had the embeddings, all they needed was a small downstream classifier trained on the labeled data they already had. That’s a huge simplification. When you consider the time it takes to iterate on features, track drift, and maintain model pipelines, the productivity impact is significant.

This changed how I think about modeling problems. I would have ruled out transformers here because payments look static. But once you think of them as behavior happening over time, you realize that the structure was always there—it just hadn’t been modeled that way.

I’ve been thinking about where else this might apply. Not just payments. Maybe logistics. Support systems. Claims. Anywhere events happen in sequence and build on each other. Once you look at the data through that lens, new patterns start to feel possible.