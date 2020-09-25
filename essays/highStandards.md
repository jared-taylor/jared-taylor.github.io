---
layout: essay
type: essay
title: High Standards
# All dates must be YYYY-MM-DD format!
date: 2020-09-24
labels:
  - Standards
  - Coding
  - Javascript
---

## Clear and Concise

In a previous essay, I shared how I enjoy writing code in as few lines as possible, something that as been made easier than ever before with the introduction of the Underscore library. I've been greatly enjoying the personal challenge I set for myself to write functions in a single line of code whenever possible. However, another perspective on writing code I was taught that challenged that mindset was to prioritize clarity over brevity so another person looking at a block of code for the first time can easily decipher what a function is meant to accoplish and how to implement it. I do believe having code that is easy to understand can be really helpful, especially when collaborating with a team developers. But even more important, in the scope of collaborative programming, is the adherence to a set standard for how the code is written. When looking at thousands of lines of code, a very realistic scenario that can be found in various repositories on Github, consistency in format can vastly enhance the readability. This in turn makes the whole project much more valuable. However, ensuring that one's own code also adheres to some set of standards takes extra effort and time. Luckily, there are tools that exist to make that task easier.

## ESLint

Using ESLint was like a love at first sight experience for me. While not as easy to use in the Windows environment I use (I always have issues with the command line implementation), being able to see all the style issues at once eases the task of adhering to standards tremendously. It's usefulness goes far beyond the tiny details of spacing, indentation, and missing characters. Errors about unused functions or variables are a great warning that I'm probably forgetting a crucial line of code, without which my whole project could fail to work as expected. More than once, an error related to a declared variable for use as an index in a loop has clued my into why the loop didn't work, or saved me from declaring it in a way that would curely cost me several minutes in troubleshooting later on. The fact that it can be reconfigured to work with any custom set of standards makes it worth every cent (just kidding, its free!).

I also enjoy using it in combination with a full-featured IDE, which is IntelliJ in my case. IntelliJ circumvents the issues I otherwise have in getting the code analysis to run, while also providing a much more readable interface for showing where the errors are and how to fix them. Even better, being able to use one hot key to instantly implement all the suggested fixes for style issues frees up so much brainpower and precious minutes when time is short. I love that I'm also able to get warnings about code that could be condensed, which almost feels like cheating in my quest to write one-line functions. 

## Cost benefit analysis

The question is, is it worth it? And my answer is a resounding yes. While i find it taxing to manually check code for tiny details that don't strictly enhance functionality, automating the process makes it so easy that there should be no question of whether or not to hold yourself to a standard for code quality. While there was significant time required in the one-time setup, the time saved in the end will more than make up for it in the long run.
