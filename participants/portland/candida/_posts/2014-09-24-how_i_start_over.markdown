---
layout: post
title:  "How I Start Over: Notes on Recovering from Bad Code"
author: Candida Haynes
date:   2014-09-24
categories: candida

---


I have known for a long time that I can learn anything. One of my goals in the Ascend Project is to gain more confidence that my code will do what I want it to do.

I started learning Python by breaking things in the command line. For example, to find out if my Python 3 syntax was correct, I would type what I thought I remembered and see if it yielded the result I expected. If I did not get an error message, I raised my arms in the air to whoop up my victory. That was one route towards confidence, but I was not actually finished because I did not always understand why my code worked. I was fine with that until I started learning GitHub. I needed more.

Most people tout the way that GitHub allows a developer to track errors and find your way back to what you did to break your code. Since I am still learning to navigate the terminal and even comprehend help, I find that GitHub forces me to know more before I do anything. It puts a lot of pressure on me to get it right the first time, which complicates my journey to learn by breaking all the things… okay, maybe not all the things, but you know what I mean. I break this less now because I know more, and recovering takes a different set of steps. For example, if I delete two files while I think I am moving them into a new folder, I cannot just reassign a variable or change the syntax (as I do in Python). My changes have more baggage.

My Error: I made changes to my local repository before doing a ‘git pull.’ I was about to overwrite several minutes worth of work. Yikes! Then…

Magic words to the rescue!

Coding is a superpower, and these are magic words that you can use to recover from changes that you have not yet staged or committed in Git.

$ git stash
$ git pull folder name repo_branch_name
$ git stash pop
[Then resume with the normal push process]
$ git add .
$ git commit -m “Stashed the changes I made to local repo, pulled the newest version of the working branch, added, committed, pushed again.”
$git push

To commit the changes that I had rescued, I used pop then the normal push process (git add. , etc.) and followed the pull request process on Github.

There is a caveat to this blog post: As with real life, I have to make mistakes publicly because my inner circle is not always equipped to offer the help I need. If there is anything wrong with these steps, feel free to suggest the changes you believe I need to make.I may push for more information if I need to understand better, but I welcome constructive feedback.

There is more information about this item on [this site](http://git-scm.com/docs/git-stash).

