---
layout: post
title:  "Development Environment"
date:   2014-10-01
author: Carmen Cordis
categories: carmen
---

Yesterday, I was very proud of my achievement in making my first ever Bugzilla comment seeking support in working on my very first bug.  Yay!

I had a thoroughly developed idea of what I was going to do, how I was going to set up my development environment, and what changes I would make in the code to fix the bug.  The bug is about sorting an add-on to make it more easy to read.

Today, I was thrilled to see some comments about the bug, encouraging me to join the IRC discussion at #amo on irc.mozilla.org and problem solve about how to fix the bug.  It seems to be a relatively small change.

The bug report itself is [here](https://bugzilla.mozilla.org/show_bug.cgi?id=593634).

First, I found the helpful source-code links in the bug comments at the GitHub repo for Olympia, or addons.mozilla.org .

I began reading the instructions on how to set up a development environment for Olympia.  I figured it would be challenging but possible, because we've set up development environments already in Ascend!

Then, I encountered a blockade to my progress.

According to this page on [Installing Olympia](http://olympia.readthedocs.org/en/latest/topics/install-olympia/installation.html) I need several files upon which my development environment will depend.

These include:

+ Python
+ Node
+ MySQL
+ libxml2

My first question to myself was "How do I get Python?"  I mean, I know it's a language, and I even learned how to write a bit of code in Python via [Codecademy](http://www.codecademy.com/), but I didn't know if I had it on my Ascend laptop.  I guess I figured that "getting Python" was something only attempted by programmers who'd been programming for 30 years.

I fretted for a few minutes trying to figure out how to determine what's on my computer.

Then, I got some wonderful advice from Kronda!

Typing "which python" into my Terminal will show me exactly where Python "lives" on my machine, if I have Python installed.

I typed "which python" and found the file path for Python on my Ascend laptop!  Awesome!

I have a vague memory of installing Python during Ascend, but I am not sure when we did.  We installed so many things at once that I kind of got lost in the flow.

Then I wanted 