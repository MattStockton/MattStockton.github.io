---
layout: post
title: Applying Amdahl's Law to Your Life
---
Ok, I admit it...this may qualify as the nerdiest / lamest name for a blog post...ever...in the history of the blogosphere...but hear me out on this one, because I'm going to make a point that might help you focus your energies in work and life to achieve more with the same amount of effort.

I recently started the 7th course in my Masters - Computer Science Program through the [University of Illnois'](http://cs.uiuc.edu) distance learning program. I didn't plan very well, and I'm down to my final 2 required courses...of course I save the most dreaded courses for last. I'm a Software guy, so the prospect of taking Computer System Organization is a bit scary - and that is what I am taking this semester. I'm not completely lost yet (but it is only the 3rd week of class, so there's still time), and the material actually is quite interesting so far.

In the last class, we learned about [Amdahl's Law](http://en.wikipedia.org/wiki/Amdahl%27s_law), which is essentially a formula that allows you to calculate the expected benefit of making a specific performance optimization to a computer system.

As a quick example, lets say you have a system and you want to make it faster. You determine that you can make 50% of the system work 2 times faster. According to Amdahl's law, this improvement will improve the overall efficiency of the system by about 33%.&nbsp; The formula for the performance improvement is:

Speedup = 1 / [ (1 - p) + (p / s)]

Where p represents the percentage of the process you sped up (50% in our example), and s represents how many times faster you made that percentage of the process (2 in our example).

Amdahl's law at it's basics is a very simple rule that can give you a good picture of how much you can improve a process - It can guide you in understanding if improving the process by a certain factor is worth the effort. What is interesting is what happens when you look at cases where you focus on optimizing portions of a process to a very high level - for example, making 10% of the process work 100 times faster. Let's quickly run this calculation:

Speedup = 1 / [(1-0.1) + (0.1/100)] = 10.99% improvement

To go even further, what if we make 10% of the process work 1 million times faster?:

Speedup (with 1 million times faster for 10% of the process) = 1 / [(1-0.1) + (0.1/1000000)] = 11.11% improvement

Really? So we spent all the effort in making it 1 million times faster instead of 100 times faster, and all we got was making the total process *just 0.12% better*? Seems kind of pointless to make all that effort huh?

What if, instead of trying to optimize the heck out of 10% of the process, we tried to slightly optimize 15% of the process. So, we will try to speed up 15% of the process by just 5 times. What does that give us?

Speedup (with 5 times faster for 15% of the process) = 1 / [(1-0.15) + (0.15/5)] = __13.64%__

Whoa...so we were able to get a better overall improvement by focusing on 15% of the process instead of 10% of the process, even though we only improved that 15% of the process by 5 times (compared to 1 million times for 10% of the process).&nbsp; What this is telling me is that in CS, __it is better to focus on improving a larger section of a process by a smaller amount then it is to focus on improving a smaller section of a process by a much much larger amount.__

Interesting stuff, but maybe not that interesting unless you're trying to optimize some piece of hardware or software, which you probably are not. But I believe that this same idea can potentially help you be more productive / more efficient in your life.

Being a perfectionist is often considered to be a good trait to have in the business world...but there is a limit. Time is valuable, and if you spend too much time making some specific thing 'too perfect'&nbsp; (in Amdahl's law, optimizing a very small portion of the process to a very high degree), then you lose time that you could potentially spend adding value to something else (in Amdahl's law, focusing on another chunk of the overall process). I'm not arguing here that you should give a half-hearted effort on your tasks...I'm just saying that sometimes 90% on task A is good enough, and your time is better spent moving on to task B.

If you're anything like me, it is all too easy to fall into the mindset that it must be '100% perfect' (or 'completely optimized') before you stop working and move on to the next task - next time you find yourself falling into this trap, remember the simple formula above - sometimes it's best to accept the 90% and move on to the next task ...&nbsp; squeezing the last bit of value out of the almost-perfectly optimized / completed task is a deceiving --- it may not be as valuable as it may seem!