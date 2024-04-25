---
layout: post
title: Product smells and sniff tests
---

**Thoughts on ‘Product strategy means saying NO’**

Des Traynor wrote a post recently on how [‘Product strategy means saying NO’](http://insideintercom.io/product-strategy-means-saying-no) It’s a really great post which enumerates scenarios when you should say no to adding features to your product. As an Engineer, some of these scenarios resonated with me because I’ve been burned by them before.

After sharing the post with friends, I had a thought that continued to surface: I’ve also violated several of these reasons to not add a feature in the past (sometimes reluctantly), and it turned out OK, sometimes great. I still largely agree with the items listed in Des’ post but I don’t think it’s the end of the story.

In the end, you need to say yes to something, or else you have nothing. You have no product or business. There’s no algorithm for what to say no to and what to say yes to. If there were, then we would let computers do all the work. Instead, we humans have to do it. To maintain our sanity, we create ‘best practices’ to make sense of the decisions we face. Best practices aren’t cut-and-dry regulations or rules and sometimes they need to be broken.

I see Des’ scenarios as a list of anti-best-practices. They are the things you typically should not do. In software design we have a similar concept. It’s called a [code smell](http://en.wikipedia.org/wiki/Code_smell). A code smell is a pattern in your code that normally indicates a deeper problem. Your code may still work as expected, but it has a weak, fragile design — something that can cause bigger problems later on. A code smell is a heuristic and is subjective, it is not a rule. Code that I think smells may not necessarily be smelly to someone else.

When we find code smells, we don’t throw away the code, we try to dig deeper into the problem. We discuss it with our peers. We ask questions about it. We change the code in small steps in attempt to find clarity. We add, delete, and edit. We call it re-factoring.

For me, Des is providing a list of ‘sniff tests’ — heuristics to use that are normally indicative of a product smell. Just like code smells, product smells sometimes just mean you have to dig deeper into the problem, not necessary delete the idea. You have to ask the right questions to understand why or why not this might be a good thing to do. You need to add, delete, and edit. Re-factoring takes time.

As I’ve worked on a product, there’s been a constant battle between trying to answer the ‘what and the why’ of the product, and the inherent need to make progress and move forward. The ‘what and the why’ is sometimes very hard to answer — it’s unclear, subjective, and has no ‘formula’ to figure it out. This uncertainty can make you anxious to move forward with something, *anything —* because being stagnant is such an uncomfortable feeling. There is a balance. You have to answer the what and the why in a disciplined manner, but you also can’t be stagnant.

For me, Des is providing us with reasons for the ‘what and the why’ that have proven to be bad in the past. I agree with them because I’ve experienced them too. But does that mean we should use them as a definitive set of rules that stand alone? Should we take each possible feature addition and make sure that it hasn’t violated any of these reasons before pursuing it? No, I don’t think so. In fact, I think that would be dangerous. I’m also a bit worried that some Engineers would use that exact strategy. So, my fellow Engineers, please keep this in context. These are sniff-tests, not rules. They are sometimes just indications to dig deeper and to re-factor the idea, not to delete it.