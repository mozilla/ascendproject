---
layout: post
title:  "Week Two Updates"
date:   2014-09-19
author: Carmen Cordis
categories: carmen
---

Week Two of the Ascend Project has been intense, thrilling, frustrating, and uplifting at times.  I've definitely learned this week that computers will "only do what you tell them to"!  We've learned a lot of new programs and commands for our terminals in such a short time.  The learning process is slow and steady, but we're getting there.

I'm still not caught up on all the Mozilla profiles and social media profiles I've created for the project!  

It's been a while since I've engaged so much in social media, and the "tech community" (if it can even be described with only one term) is so vast that I barely know where to begin.

As part of my goals for Ascend, I need to make an ongoing list of each of my profiles, in order to keep current with updates, and in order to track my ongoing contributions.  The more I learn, the more I can contribute.

I need to refine the little website I built last week with Webmaker.  It's colorful, but simple, and perhaps it could use more spacing between the text.  I would also like to link the Ascend Project's pages!

This week, we focused our energies on **running tests**, **checking on bugs**, and **helping to reproduce bugs** found by other contributors.  We had a lot of fun calling each other on our computer screens by using the video call features in Aurora!  It was rather humorous to talk to someone sitting across the table, and hear them echoing from my computer.

Running the calls in Aurora helped us to identify some bugs, and to explore what it's like to test individual features of a program.   We wanted to make sure they're running the way they were intended to run, and the way we would like them to run.

Here are some Mozilla resources we used to help us identify, report, and reproduce bugs:

+	[MozTrap](https://moztrap.mozilla.org) can show you a list of tests you can run in your own Firefox browser.  When you specify your build and browser version, you can mark each specific test as passing or failing.  If the instructions are unclear, you can even write in comments to ask for clarity.  MozTrap is a great starting point to get an idea of what a test looks like.  The site helped us understand how a "bug" is a specific browser activity that's not working correctly.

+	[Mozmill](https://developer.mozilla.org/en-US/docs/Mozilla/QA/Mozmill_tests) helped us set up our own automated testing!  We mostly chose to work in Git for this.  We each had interesting discussions about how to write the most accurate code lines in our terminals to get the automated testing to work.

It took several tries for me to finally understand how the file-path worked, and I wondered if I was the only person who really didn't understand.  When it finally became clear how to make the code line work, I felt so relieved.  I'm thankful for the Ascenders who stuck with me to help me understand.  Then, I got to help another person understand, too!

Some Ascenders are making tutorials in how to run Mozmill tests.  Check them out!  We were able to make our Nightly browsers open a bunch of tabs, download test files, and dance all around, without even having to touch the keyboard!  All of these tests were designed to catch bugs.

Here's a lovely link to show the results of my automated Mozmill tests in the Nightly browser:

[Carmen's Mozmill tests!](http://mozmill-crowd.blargon7.com/#/functional/report/2f982f72826307fed840a3b11c3bce2e)

+	[Bugzilla](https://bugzilla.mozilla.org/) (also called BMO) is the main venue where Mozillians talk to each other about possible bugs, confirmed bugs, bugs that have been assigned to specific people as their personal projects, and bugs that have been fixed.

Often times, people will report a bug that's actually a duplicate of another report.  When I filed my first few bugs, some of these were marked as duplicates.  I felt a little disheartened by the duplication, but, at the same time, I realized that multiple reports about the same bug will bring attention to the need for the bug to be fixed.

Bugzilla has resources for sorting bugs, searching for bugs to help with, and contributing patches to fix the code.

The Whiteboard tag [good first bug] means that someone reviewing the bug believes that a new contributor could fix it, with enough research, context, and time.

Different bugs are in different programming languages, so people with varying experience levels can all help.

We also searched for bugs with the designation "steps wanted", which means that a team of people are working to reproduce the bug, so that it can be fixed through trial and error.

+	There's also a helpful page about [making contributions to Mozilla](http://whatcanidoformozilla.org) where you can review various ways to help out!