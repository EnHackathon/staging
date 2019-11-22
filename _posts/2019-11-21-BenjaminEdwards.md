---
layout: post
title:  "EnHackathon - Whipping Subinterpreters into shape"
date:   2019-11-21
author: Benjamin Edwards
---

Over the past couple of days I have been busy completing the markups to my Pull Request for my changes to [Get Type Hints]() and learning lots about subinterpreters (including that its not subinterpretors). After helping Lewis debug and test his code for `channel_list_interpreters()` I set out to find another issue in the module to work on. 


# Threads vs Interpreters

One of the more interesting things I learnt while talking to Phil is the relationship between threads and interpreters. I had been assuming up to now that there was a kind of hierarchical structure where processes > intepreters > threads. By this I mean you have processes which are what is seen by the outside system. Within processes you have intepreters, which run the python code. And within interpreters you can have different threads running simultaneously. But boy was I wrong.

What is actually going is actually a bit more subtle. Within a Process you will have threads which are seperate instances of the C code. As there are different instances of C code it means they can run on different cores of the prcoessor at the same time. Then you have interpreters, which are completely orthogonal to threads and are used to run the Python code. So each interpreter runs its own bit of Python code with its own state seperate from other interpreters. This means you can have two interpreters on one thread leading to two bits of Python code runni gon seperate states but having to take turns over the processer. Or you can have two threads on one interpreter so there are two bits of Python code running simultaneously but having to share state. 


# Conclusion

I'm very happy with progress I have made over the past couple days. I have managed to merge down my second Pull Request, which was all down to the quick responses I got when i requested a code review. I am also enjoying learning more about the sub-intepreters project and look forward to contributing further.