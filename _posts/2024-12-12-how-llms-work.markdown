---
layout: single
title: "How Large Language Models Work at a High Level"
---

Recently, I watched a fantastic [3Blue1Brown video](https://www.youtube.com/watch?v=LPZh9BOjkQs) on large language models that does an excellent job of demystifying the technology. The video is under 10 minutes and well worth your time.

I’ve always found that when I understand a tool more deeply, I not only feel more confident using it but also have a clearer sense of how to apply it effectively. This video provides just enough insight to help you understand how LLMs work, which can guide you on how they can and should be used.

I’ll briefly explain some key points here, but the video does a much better job. It’s packed with neat visualizations and walks through the concepts step by step in an engaging and easy-to-understand way. If you want a clear picture of how these tools work without getting bogged down in technical details, watching it is the best place to start.

### 1. At Their Core, They Predict the Next Word

Large language models are sophisticated “guess the next word” machines. You give them some text, and they predict what comes next. For example, if you type “The cat sat on the,” it might predict “mat” as the most likely word to follow.

### 2. Learning from Massive Text Datasets

These models are trained on enormous amounts of text — imagine reading thousands of lifetimes' worth of books, articles, and more. If you read everything that ever existed and were asked to predict the next word in a sentence, you’d probably get it "right". This is essentially what large language models are doing, refining their predictions through exposure to massive datasets.

### 3. Context Makes Them Smart

These models use the *transformer architecture*. You can think of it as the model being able to look at all the words in a set of sentences at the same time instead of processing one word at a time. This breakthrough allows the model to better understand how words relate to one another in context. For example, it can determine whether "bank" means a riverbank or a financial institution by considering the surrounding words. This ability to grasp context is one of the main reasons large language models are so effective at next-word prediction. Their ability to understand language context makes their predictions better.

### 4. Fine-Tuning to Be More Helpful

After the initial training, humans evaluate the model’s outputs. They label responses as good or bad based on how helpful or accurate they are. These labels are then used to refine the model through a process called reinforcement learning. It’s like giving the model a scorecard for its responses and teaching it to improve. 

This feedback process still happens during the training phase — not while you’re using the model. When you interact with the model, it isn’t analyzing or learning from your inputs. Some models, however, have policies about whether your data can be used for future training. This is something to keep in mind when choosing which models to use.

### 5. Why They Sometimes Make Mistakes

Large language models are designed to predict the next word in a sequence based on patterns in their training data. While their responses often sound natural and fluent, they can still produce mistakes, such as hallucinations — when the model confidently generates something untrue. This happens because the model isn’t built to verify facts; it’s focused on generating text based on probabilities, not truth.

One way to improve the reliability of their responses is by carefully structuring the input you provide. Models use a context window, which is the portion of input text they consider when generating their output. You can use this to guide the model, for example, by including a specific document or instructions and telling it to focus only on that information. This approach helps direct the model’s responses and can reduce errors, especially in tasks where accuracy is critical.

### Why This Matters

When people grasp that large language models are advanced predictors, it becomes clearer what types of tasks they are well-suited for, what to avoid, and how to use them effectively. The video is an excellent introduction, and you should absolutely watch it.