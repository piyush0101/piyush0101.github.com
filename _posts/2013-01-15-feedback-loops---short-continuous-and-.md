---
layout: post
title: "Feedback Loops - Short, Continuous and ?"
description: ""
category: 
tags: [feedback loops, feedback]
---
{% include JB/setup %}

I was working one friday afternoon at the **Thought**Works Dallas office, remoting into the machine at the client site and pairing with a fellow developer. Internet connection speeds here in the United States are pretty amazing and it did not take long to connect to the remote machine and start coding in eclipse. This has happened to me before but I never thought much about it. Even the slightest of lag between a keystroke and the letter appearing on the display is slow feedback. I personally am not a very accurate typist, I make errors while typing but constantly looking on the screen to see what I typed, getting instantaneous feedback on whether it was correct or not helps me in fixing the problem quickly. Imagine if there was a delay of a second in this scenrio i.e when you hit a key and when the letter appeared on the screen. How inconvenient would that have been. 

I am just curious and intrigued about the importance of efficient, streamlined feedback loops in our lives and professions. As a software developer, I have seen so many practises - [fail fast][FF] systems, fail fast techniques, fail fast language features, [continuous integration][CI], [continuos delivery][CD] and deployment, all of which have one common theme that they strive towards. Short and continuous feedbacks. Figuring out problems sooner than later, finding issues in smaller deltas rather than mining them in a sea of changes. Similar to software development, other activities in our daily lives become much less stressful and streamlined if we consider involving short, continuous and honest feedbacks. How? I know it sounds preposterous but I will explain all of it below.

[FF]: http://en.wikipedia.org/wiki/Fail-fast
[CI]: http://martinfowler.com/articles/continuousIntegration.html
[CD]: http://en.wikipedia.org/wiki/Continuous_delivery

Since my profession is developing software and I do not know the nits and grits of other fields, I will take a plunge into software development and then discuss some stuff related to other activities pertaining to our daily lives. 

## Software Development

[Kent Beck][Kent], who is the pioneer of the [Test Driven Development][TDD] technique and inventor of the [JUnit][junit] framework says that he just rediscovered the idea. **"The original description of TDD was in an ancient book about programming. It said you take the input tape, manually type in the output tape you expect, then program until the actual output tape matches the expected output"**. The most modest of man that he is, I would still say that real innovations come from smart people making the most obvious decisions. What I always feel is having a formal name for the technique and having a structure around it always helps the wider community to understand and follow it. It looks like TDD had been around but having a formal name, techniques and tools around it helped the software development community see the real benefits of it. 

[TDD]: http://en.wikipedia.org/wiki/Test-driven_development
[Kent]: http://en.wikipedia.org/wiki/Kent_Beck
[junit]: https://github.com/KentBeck/junit

There are several ideas that evolve while developing software with TDD. I just want to lay an emphasis on the feedbacks. TDD is an amazing technique to enable short and continuous feedback loops. It helps you evolve your design in a non legacy manner, gives you instant feedback on the algorithms that you are writing and makes sure that as you evolve your software to a more complex beast, you are not breaking the existing pieces. So far so good! However, TDD alone is not good enough to have honest feedback. I would say that TDD is a core technique which still requires tools around it to make it more effective and powerful. Since I am working these days on a [legacy][legacy] codebase, the first example that comes to my mind is about doing TDD with legacy code. Couple of days back, I was fixing a minor defect. I wanted to have a few tests around the culprit method. After writing a few tests with my pair, we thought we were done. We have covered this method and are good to refactor. I did not feel safe for two reasons, (i) I don't understand the domain completely, (ii) our assertions were all green but  I still don't know if we missed something. I wanted a quick feedback to feel free and safe. I remembered using an integrated code coverage tool with IntelliJ and wished there was something similar for eclipse. Fortunately, there are [Emma][emma] and [Cobertura][cobertura] plugins for eclipse. Here's how we benefitted from it. Quick, continuous feedbacks (though emma eclipse plugin takes much longer to gather coverage statistics than the integrated IntelliJ coverage tools). Still, it was short enough.

[emma]: http://emma.sourceforge.net/
[cobertura]: http://cobertura.sourceforge.net/
[legacy]: http://hackerboss.com/legacy-code/

Starting with a short example and then I will show a more complex scenario when these kinds of feedbacks are immensely useful.

![partial line coverage][partial]

[partial]: ../../../../assets/images/partial-line-coverage.png

Please don't mind the typo wigglies ;). Green is for 'full line coverage' while Yellow is for 'partial line coverage'. There's one line in the code above that is marked as yellow. It is not difficult to figure out why that line is partially covered. There is a branch in the code and it looks like that in our tests, we have covered only one branch. This screenshot is from IntelliJ using the built in IntelliJ code coverage tool. The emma eclipse plugin clearly said "1 branch out of 2 missed" along with highlighting the yellow line. In this particular instance, it does not look like an instant feedback is providing anything other than just **Staring** at you and asking to be fixed. "Sometimes staring at the code is better than using anything else".

Here is a slightly more complex example.  
