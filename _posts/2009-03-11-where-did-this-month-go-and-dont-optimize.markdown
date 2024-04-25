---
layout: post
title: Where did this month go? And don't optimize!
---
People have told me that it isn't easy to keep up a blog. Now I know what they mean! Somehow, I've gone an entire month without posting anything --- time seems to have flown by! I will try to be better at this, and post here at least 1 time a week (2 may have been a bit of an ambitious start)

I'm already halfway through this semester's UIUC course ([CS 433 - Computer System Organization](http://www.cs.uiuc.edu/class/sp09/cs433/)), and that has been taking up a bunch of my time - I wasn't too crazy about taking the course (given that I am more of a software guy), but it is a requirement for graduation.

Needless to say, the class has been awesome so far! The material is both interesting and challenging. Currently, we are learning about different software and hardware solutions to improve processors -- there's some really interesting stuff in this domain!

At a high level, the course has brought me to two conclusions with regards to developing software:
* Choose clarity over optimization, because the lower levels will help you with the optimization anyway - Here, I am talking about the 'small' optimizations that people tend to make in code that can make the code very unclear (large scale optimizations involving architecture, etc. are still absolutely necessary). One of my least favorites of this is caching a calculated value when the calculation takes a very short amount of time. If the calculation is easy, just do it every time in a method! The overhead of managing the cached value, knowing when it is stale, etc. is not worth it!
* The impact of optimization from single Processor improvements (Pipelining optimizations, dual issue, Branch predication schemes, clock speed, etc.) is slowly fading, as is evidenced by the recent explosion of multi-core systems.  Squeezing in a few more instructions in a clock cycle is not going to cut it anymore. This is quite interesting, as now the burden for optimization will __shift to the developer__.  We will have to spend some effort to plan our software such that we are effectively utilizing the multiple available processors! This could mean a paradigm shift in how software is developed to run on the multi-cores.

There's actually some pretty good quotes out there with regards to Software Optimization that I'll leave you with. Print these, put them in your cube, and look at them next time you want to do something stupid for optimization's sake:

*"Rule 1: Don't do it..... Rule 2: (for experts only) Don't do it yet"* - M.A. Jackson

*"More computing sins are committed in the name of efficiency (without necessarily achieving it) than for any other single reason - including blind stupidity.”*- W.A. Wulf  

*"Optimization is non-optimal"* - Me

Anyway, that's it for now.  For my next blog article, I am thinking about discussing the pitfalls of unit testing. Sound interesting?
